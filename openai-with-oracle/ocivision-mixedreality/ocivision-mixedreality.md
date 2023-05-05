# Use Oracle Database Sagas with PL/SQL Microservices

## Introduction

This lab will show you how to use Oracle Database Sagas with PL/SQL Microservices

Estimated Time:  10 minutes

### Objectives

-   Test sagas with PL/SQL participants

### Prerequisites

* An Oracle Cloud paid account or free trial. To sign up for a trial account with $300 in credits for 30 days, click [Sign Up](http://oracle.com/cloud/free).

### Objectives

-   Understand the concepts of Oracle Database Sagas with PL/SQL Microservices

### Prerequisites

- This lab presumes you have already completed the earlier labs.

## Task 1: Obtain an Oracle Database

1.    Enter the Cloud Shell and enter the following command to enter SQLcl
      ```
      <copy>sql /nolog</copy>
      ```

2.    Set config using the following command
      ```
      <copy>set cloudconfig wallet/wallet.zip</copy>
      ```

3.    Enter the following command and then enter your password when prompted to connect to `sagadb1`

    ```
    <copy>connect admin@sagadb1_tp</copy>
    ```  

The output should look similar to the following.

![SQLcl login to sagadb1](images/connectwithSQLcl.png " ")


## Task 2: Login to `sagadb2` database using SQLcl and add Flight, Hotel, and Car participants

1.    Open a new browser tab with another OCI console and enter the Cloud Shell there.

      This is done for convenience so that one tab/Cloud Shell/SQLcl console can be use for saga initiator (TravelAgency) operations and the other for saga participant (Flight, Hotel, and Car) operations.

2.    Repeat steps 1 and 2 in Task 1 in order to enter SQLcl.

3.    Enter the following command and then enter your password when prompted to connect to `sagadb2`

    ```
    <copy>connect admin@sagadb2_tp</copy>
    ```  

The output should look similar to the following.

![SQLcl login to sagadb2](images/connectwithSQLclsaga2.png " ")



You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, December 2023
