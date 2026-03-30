Create a Linux Virtual Machine in Microsoft Azure

Overview

This repository documents the process of deploying and configuring a Linux Virtual Machine (VM) using the Microsoft Azure Portal. The project focuses on setting up cloud compute resources and securely connecting to a Linux environment using Secure Shell (SSH).

Objectives

•
Provision a Linux Virtual Machine (e.g., Ubuntu) in Azure.

•
Configure networking and security group rules to allow SSH traffic.

•
Generate and use SSH keys for secure authentication.

•
Connect to the VM using an SSH client.

•
Verify the successful deployment of the Linux environment.

Technologies Used

•
Cloud Provider: Microsoft Azure

•
Compute: Azure Virtual Machines

•
Operating System: Linux (e.g., Ubuntu Server 22.04 LTS)

•
Networking: Azure Virtual Network (VNet), Network Security Groups (NSG)

•
Access Protocol: Secure Shell (SSH) on Port 22

Project Steps

1. Provisioning the Virtual Machine

1.
Logged into the Azure Portal.

2.
Navigated to Virtual Machines and selected Create > Azure virtual machine.

3.
Configured the Basics tab:

•
Created a new Resource Group for the project.

•
Assigned a unique Virtual machine name and selected an appropriate region.

•
Chose a Linux image (e.g., Ubuntu Server).

•
Set the Authentication type to SSH public key (recommended for better security over passwords).

•
Provided a Username and chose to generate a new key pair or use an existing one.



4.
Under the Inbound port rules, allowed SSH (22) to enable remote terminal access.

5.
Reviewed the configuration and clicked Create. Downloaded the private key file (.pem) when prompted.

2. Connecting to the VM

1.
Once the deployment was complete, navigated to the VM's overview page.

2.
Copied the Public IP address assigned to the VM.

3.
Opened a local terminal (e.g., Command Prompt, PowerShell, Terminal, or Git Bash).

4.
Set the correct permissions on the downloaded private key file (if on Linux/macOS):

Bash


chmod 400 <path-to-key.pem>





5.
Initiated the SSH connection using the following command:

Bash


ssh -i <path-to-key.pem> azureuser@<public-ip-address>





6.
Accepted the host key fingerprint to establish the secure connection to the Linux terminal.

3. Verification and Cleanup

•
Verified that the Linux Server environment was fully operational by running basic commands (e.g., uname -a, top).

•
(Optional) To prevent incurring unnecessary charges, the VM can be stopped or the resource group deleted when not in use.

Key Learnings

•
Understanding SSH key-based authentication for secure cloud access.

•
Configuring Network Security Groups to securely manage inbound traffic on port 22.

•
Utilizing command-line tools to interact with cloud-hosted Linux environments.




This project was completed as part of hands-on cloud computing practice.

