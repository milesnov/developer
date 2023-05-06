# Use Oracle Database, OCI Vision AI Text Detection and Open AI Chat

## Introduction

This lab will show you how to use Oracle Database, OCI Vision AI Text Detection and Open AI Chat
The use case involves the interpretation health test results and recommended steps for everyday individuals.

Estimated Time:  10 minutes

### Objectives

-   Use Oracle Database, OCI Vision AI Text Detection and Open AI Chat

### Prerequisites

- Completion of Setup lab

## Task 1: Execute an Open AI query and save the results in the database

1.    Build the src code project that was downloaded in the

```
    <copy>docker pull container-registry.oracle.com/database/free</copy>
   ```
- Blood sugar test result image is fed to OCI Vision Text Detection / Document AI which gives back raw text
      - Raw text is fed to OpenAI asking “explain these test results in simple terms” and “what should I do to get better results?”

You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
