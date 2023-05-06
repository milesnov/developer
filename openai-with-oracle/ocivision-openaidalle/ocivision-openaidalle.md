# Use Oracle Database, OCI Speech Service, Open AI code and image generation

## Introduction

This lab will show you how to use Oracle Database, OCI Speech Service, Open AI code and image generation
The use case involves the creation webpages and storyboards using only voice commands for individuals with impaired motor control.

Estimated Time:  10 minutes

### Objectives

-   Use Oracle Database, OCI Speech Service, Open AI code and image generation

### Prerequisites

- Completion of Setup lab

## Task 1: Execute an Open AI query and save the results in the database

1.    Build the src code project that was downloaded in the

```
    <copy>docker pull container-registry.oracle.com/database/free</copy>
   ```

O- Voice commands from user of the form “add” + [picture or code description] + to + [page location]” are sent to OCI Speech Service which transcribes them and sends the text back to client application
- The text is sent to Open AI image/DALLE (for picture generation) or conversation/chat (for code generation)
- The client app creates/updates the page according to the information, writes it to file, and loads it for viewing/testing.

You may now **proceed to the next lab.**..

## Acknowledgements

* **Author** - Paul Parkinson, Architect and Developer Evangelist
* **Last Updated By/Date** - Paul Parkinson, 2023
