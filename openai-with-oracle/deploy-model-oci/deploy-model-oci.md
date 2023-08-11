# Deploy your own Chat GPT model on OCI

## Introduction

*Describe the lab in one or two sentences, for example:* This lab walks you through the steps to ...

Estimated Time: 30 minutes

### Objectives

In this lab, you will:
* Create a compute instance on OCI
* Connect your SSH client to your compute instance
* Create a Conda environment to install python dependencies
* Download the Groovy model
* Download the GitHub repository with the examples

### Prerequisites

This lab assumes you have:
* An Oracle Cloud account


## Task 1: Create a compute instance on OCI

1. Open the navigation menu and click Compute. Under Compute, click Instances.

	<!-- ![Image alt text](images/sample1.png) -->

	> **Note:** Use this format for notes, hints, and tips. Only use one "Note" at a time in a step.

2. Click Create instance.

  <!-- ![Image alt text](images/sample1.png) -->

3. Enter a name for the instance.

4. Select the compartment to create the instance in.

5. In the Image and shape section, choose the image for the instance:

   By default, an Oracle Linux image is used to boot the instance. To select a different image or a boot volume, in the Image section, click Change image. Then, select the Marketplace as the image source.

	 Select the Partner images option, and then select an either of the data science images below.

    - AI 'all-in-one' Data Science Image Intel/AMD
		- AI 'all-in-one' Data Science Image for GPU

   Alternatively, you may select Ubuntu as the image source and use either of the images below:

    - Canonical Ubuntu 20.04
		- Canonical Ubuntu 22.04

6. In the Image and shape section, choose the image for the instance:

   For the data science images, select Virtual machine as the Instance type, AMD or Intel processors as the shape series, and VM.Standard3.Flex as the shape name. The number of OCPUs and amount of memory may be left as the defaults.

7. In the Networking section, configure the network details for the instance:

   Create new virtual cloud network: If you want to create a new VCN, make the following selections:

    - New virtual cloud network name: A friendly name for the network. Avoid entering confidential information.
    - Create in compartment: The compartment where you want to put the new network.
    - Create new public subnet: A subnet within the cloud network to attach the instance to. The subnets are either public or private. Private means the instances in that subnet can't have public IP addresses. See Access to the Internet. Subnets are either specific to an availability domain or regional (regional ones have "regional" after the name). We recommend using regional subnets.

   Enter the following information:

    - New subnet name: A friendly name for the subnet. It doesn't have to be unique, and it can be changed later. Avoid entering confidential information.
    - Create in compartment: The compartment where you want to put the subnet.
    - CIDR block: A single, contiguous CIDR block for the subnet (for example, 172.16.0.0/24). Make sure it's within the cloud network's CIDR block and doesn't overlap with any other subnets. You cannot change this value later. See Allowed VCN Size and Address Ranges. For reference, here's a CIDR calculator.
    - Enter subnet OCID: If you want to provide an existing subnet's OCID, for Subnet OCID, enter the subnet OCID.

8. Linux instances:In the Add SSH keys section, generate an SSH key pair or upload your own public key. Select one of the following options:

    - Generate a key pair for me: Oracle Cloud Infrastructure generates an RSA key pair for the instance. Click Save Private Key, and then save the private key on your computer. Optionally, click Save Public Key and then save the public key.
    - Upload public key files (.pub): Upload the public key portion of your key pair. Either browse to the key file that you want to upload, or drag and drop the file into the box. To provide multiple keys, press and hold down the Command key (on Mac) or the Ctrl key (on Windows) while selecting files.
    - Paste public keys: Paste the public key portion of your key pair in the box.

9. In the Boot volume section, configure the size and encryption options for the instance's boot volume:

   To specify a custom size for the boot volume, select the Specify a custom boot volume size check box. Then, enter 100 as the boot volume size (GB).

10. Click Create.

## Task 2: Connect your SSH client to your compute instance

1. Step 1 - tables sample

  Use tables sparingly:

  | Column 1 | Column 2 | Column 3 |
  | --- | --- | --- |
  | 1 | Some text or a link | More text  |
  | 2 |Some text or a link | More text |
  | 3 | Some text or a link | More text |

2. You can also include bulleted lists - make sure to indent 4 spaces:

    - List item 1
    - List item 2

3. Code examples

    ```
    Adding code examples
  	Indentation is important for the code example to appear inside the step
    Multiple lines of code
  	<copy>Enclose the text you want to copy in <copy></copy>.</copy>
    ```

4. Code examples that include variables

	```
  <copy>ssh -i <ssh-key-file></copy>
  ```


## Task 3: Create a Conda environment to install python dependencies

1. Step 1

2. Step 2

## Task 4: Download the Groovy model

1. Step 1

2. Step 2

## Task 5: Download the github repository with the examples

1. Step 1

2. Step 2

## Learn More

*(optional - include links to docs, white papers, blogs, etc)*

* [URL text 1](http://docs.oracle.com)
* [URL text 2](http://docs.oracle.com)

## Acknowledgements
* **Author** - <Name, Title, Group>
* **Contributors** -  <Name, Group> -- optional
* **Last Updated By/Date** - <Name, Month Year>
