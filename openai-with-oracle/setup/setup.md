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
      
      Here we will use the docker container. Simply issue the following commands, replacing `Welcome12345` with your compliant password if you like.
      You can either use the container-registry.oracle.com container using the following command(s)...

   ```
    <copy>docker pull gvenzl/oracle-free; docker run --add-host docker.for.mac.host.internal:host-gateway -d -p 1521:1521 -e ORACLE_PASSWORD=Welcome12345 gvenzl/oracle-free</copy>
  
You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
