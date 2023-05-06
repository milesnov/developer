# Setup

## Introduction

In this lab, we will provision an Oracle Database and OCI Cloud Account and download the source code for the workshop

Estimated Time: 15 minutes

### Objectives

* Provision an Oracle Database 
* Install SQlCl client for convenient administration
* Clone workshop code
* Execute setup

### Prerequisites

- This workshop assumes you have an Oracle cloud account and have signed in to the account.
- The workshop also requires Always Free 21c ATP instances and so is limited to the following regions: Ashburn (IAD), Phoenix (PHX), Frankfurt (FRA) and London (LHR) regions


## Task 1: Download or clone the workshop source code

1.    Go to https://github.com/paulparkinson/openai-and-oracle-for-good and either download or `git clone https://github.com/paulparkinson/openai-and-oracle-for-good.git` the source.
      We will refer to the root directory of this repos as `[AI_WORKSHOP_SRC_ROOT]` .


## Task 2: Obtain and Start an Oracle Free 23c Database

1.    There are a number of ways to go about this which can be found here: https://www.oracle.com/database/free/get-started/
      
      Here we will use the docker container. Simply issue the following commands, replacing `yourpassword` with your compliant password such as `Welcome12345`

   ```
    <copy>docker pull container-registry.oracle.com/database/free</copy>
   ```

   ```
    <copy>docker run -d -p 1521:1521 -e ORACLE_PASSWORD=yourpassword container-registry.oracle.com/database/free</copy>
   ```


Optionally, add the `-v oracle-volume:/somedirectory` parameter if you would like data persisted and specific an actual directory (otherwise data is lost across database container restarts)

   ```
    <copy>docker run -d -p 1521:1521 -e ORACLE_PASSWORD=yourpassword -v oracle-volume:/somedirectory container-registry.oracle.com/database/free</copy>
   ```

Should you wish to reset the sys password, you can do so by issuing docker ps -al to get the image id and then issue the `resetPassword` as shown here.

```
    <copy>docker ps -al</copy>
```

```
    <copy>docker exec [IMAGE_ID] resetPassword yournewpassword</copy>
```

## Task 3: Download SQLcl and initialize the database with user, tables and JSON Duality views

1.    Download and install from this location https://www.oracle.com/database/sqldeveloper/technologies/sqlcl/download/ 
      This will provide in a `[SQLcl_INSTALL_DIR]/bin/sql` executable that we will use to administer the database.

2.    Login  replacing `[SQLcl_INSTALL_DIR]` with the location of your SQLcl 
      and replacing `yourpassword` with the one you provided as `ORACLE_PASSWORD` when creating the database.

```
    <copy>[SQLcl_INSTALL_DIR]/bin/sql  sys/yourpassword@//localhost:1521/freepdb1 as sysdba</copy>
```


3.    At the SQLcl prompt execute the following scripts to create a user with appropriate privileges, switch to that user, and  
      (The script also enables REST endpoints on the database, though we don't actually use them in this workshop)

```
    <copy>@[AI_WORKSHOP_SRC_ROOT]/sql/create_user_enable_rest.sql</copy>
```


You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
