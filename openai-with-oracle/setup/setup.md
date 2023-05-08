# Setup

## Introduction

In this lab, we will provision and setup everything that is needed to run all of the labs in the workshop

Estimated Time: 15 minutes

### Objectives

* Clone workshop code
* Provision an Oracle Database 
* Install SQLcl client for convenient administration of database
* Run scripts in SQLcl to setup database user, tables, and JSON duality views, as well as JavaScript
* Configure access to Oracle Cloud services including keys and config file
* Obtain an OpenAI account and token
* Build the workshop code so that it is ready for later labs

### Prerequisites

- This workshop assumes you have an Oracle cloud account and have signed in to the account.

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

## Task 3: Download SQLcl and initialize the database with user, tables, JSON Duality views, and JavaScript code

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

## Task 4: Configure access to Oracle Cloud services including keys and config file


   
1. First create a location to store the keys and config file which is generally `~/.oci`

```
    <copy>mkdir ~/.oci</copy>
```

2. Next, create a key_file and use it to obtain a finger print as describe here: Full instructions can be found here: https://docs.oracle.com/en-us/iaas/Content/API/Concepts/apisigningkey.htm#apisigningkey_topic_How_to_Generate_an_API_Signing_Key_Console


3. Finally, Full instructions for creating the `config` file (generally placed in `~/.oci`) can be found here: https://docs.oracle.com/en-us/iaas/Content/API/Concepts/sdkconfig.htm#SDK_and_CLI_Configuration_File
  However, in short, you can create the `config` file manually and simply fill in the appropriate information.

```
    [DEFAULT]
      user=ocid1.user.oc1..<unique_ID>
      fingerprint=<your_fingerprint>
      key_file=~/.oci/oci_api_key.pem
      tenancy=ocid1.tenancy.oc1..<unique_ID>
      region=us-ashburn-1
```

https://docs.oracle.com/en-us/iaas/Content/API/Concepts/apisigningkey.htm#apisigningkey_topic_How_to_Generate_an_API_Signing_Key_Console

## Task 5: Build the workshop code so that it is ready for later labs

1.    Simply issue the following command, replacing the value of `[AI_WORKSHOP_SRC_ROOT]`, to build and run the Spring Boot Java application that is used for most of the labs in this workshop.

```
    <copy>cd [AI_WORKSHOP_SRC_ROOT] ;  mvn clean package ; java -jar target/oracleai-0.0.1-SNAPSHOT.jar</copy>
```


You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
