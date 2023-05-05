# Setup

## Introduction

In this lab, we will provision an Oracle Database and OCI Cloud Account and download the source code for the workshop

Estimated Time: 15 minutes

### Objectives

* Provision 
* Clone the setup and microservices code
* Execute setup

### Prerequisites

- This workshop assumes you have an Oracle cloud account and have signed in to the account.
- The workshop also requires Always Free 21c ATP instances and so is limited to the following regions: Ashburn (IAD), Phoenix (PHX), Frankfurt (FRA) and London (LHR) regions

## Task 1: Provision 2 ATP 21c PDBs

1. From the drop-down menu in the upper left of the OCI Console, select `Oracle Databases` and then `Autonomous Transaction Processing`

   ![Open DB Menu](images/dbhamburgermenu.png " ")


## Task 2: Launch Cloud Shell and make a clone of the workshop source code in your home directory

Cloud Shell is a small virtual machine running a "bash" shell which you access through the Oracle Cloud Console. Cloud Shell comes with a pre-authenticated command line interface in the tenancy region. It also provides up-to-date tools and utilities.

1. Click the Cloud Shell icon in the top-right corner of the Console.

  ![Open Cloud Shell](images/open-cloud-shell.png " ")

  NOTE: Cloud Shell uses websockets to communicate between your browser and the service. If your browser has websockets disabled or uses a corporate proxy that has websockets disabled you will see an error message ("An unexpected error occurred") when attempting to start Cloud Shell from the console. You also can change the browser cookies settings for a specific site to allow the traffic from *.oracle.com

2. Clone from the GitHub repository using the following command.  

    ```
    <copy>git clone -b 22.1.4 --single-branch https://github.com/oracle/microservices-datadriven.git</copy>
    ```

   You should now see the directory `microservices-datadriven` in the home directory.

You may now **proceed to the next lab.**.

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, December 2023
