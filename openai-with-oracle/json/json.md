# Use Oracle Database JavaScript support and JSON features such as JSON Duality

## Introduction

This lab will show you how to use Oracle Database JSON features to story, analyze, etc. your Open AI other data.

Estimated Time:  10 minutes

### Objectives

-   Use Oracle Database JSON features to story, analyze, etc. your Open AI other data.

### Prerequisites

- Completion of Setup lab

## Task 1: Execute an Open AI query and save the results in the database

1.    Build the src code project that was downloaded in the  

```
    <copy>docker pull container-registry.oracle.com/database/free</copy>
   ```

```
    <copy>docker pull container-registry.oracle.com/database/free</copy>
```
    

   ![SQLcl login to sagadb1](images/connectwithSQLcl.png " ")


## Task 2: Query the results in the database using both SQL and JSON queries.

1.    Open a new browser tab with another OCI console and enter the Cloud Shell there. 

       This is done for convenience so that one tab/Cloud Shell/SQLcl console can be use for saga initiator (TravelAgency) operations and the other for saga participant (Flight, Hotel, and Car) operations. 

2.    Repeat steps 1 and 2 in Task 1 in order to enter SQLcl.

3.    Enter the following command and then enter your password when prompted to connect to `sagadb2`

    ```
    <copy>connect admin@sagadb2_tp</copy>
    ```  
   
   The output should look similar to the following.

   ![SQLcl login to sagadb2](images/connectwithSQLclsaga2.png " ")


https://blogs.oracle.com/database/post/json-relational-duality-app-dev

You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
