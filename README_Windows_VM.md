Create a Windows Virtual Machine in Microsoft Azure

Overview

This repository documents the process of deploying and configuring a Windows Virtual Machine (VM) using the Microsoft Azure Portal. The project demonstrates fundamental cloud infrastructure skills, including resource group management, compute provisioning, and secure remote access.

Objectives

•
Provision a Windows Server Virtual Machine in Azure.

•
Configure networking and security group rules to allow RDP traffic.

•
Connect to the VM securely using Remote Desktop Protocol (RDP).

•
Verify the successful deployment of the virtualized environment.

Technologies Used

•
Cloud Provider: Microsoft Azure

•
Compute: Azure Virtual Machines

•
Operating System: Windows Server (e.g., 2022 Datacenter)

•
Networking: Azure Virtual Network (VNet), Network Security Groups (NSG)

•
Access Protocol: Remote Desktop Protocol (RDP) on Port 3389

Project Steps

1. Provisioning the Virtual Machine

1.
Logged into the Azure Portal.

2.
Navigated to Virtual Machines and selected Create > Azure virtual machine.

3.
Configured the Basics tab:

•
Created a new Resource Group to organize project resources logically.

•
Assigned a unique Virtual machine name and selected an appropriate region.

•
Chose the Windows Server image.

•
Set up the Administrator account (username and secure password).



4.
Under the Inbound port rules, allowed RDP (3389) to enable remote connections.

5.
Reviewed the configuration and clicked Create to deploy the VM.

2. Connecting to the VM

1.
Once the deployment was complete, navigated to the VM's overview page.

2.
Copied the Public IP address assigned to the VM.

3.
Clicked Connect > RDP and downloaded the RDP file (or opened the Remote Desktop Connection app locally).

4.
Entered the public IP address and authenticated using the administrator credentials created during setup.

5.
Successfully established a remote session into the Windows Server desktop.

3. Verification and Cleanup

•
Verified that the Windows Server environment was fully operational.

•
(Optional) To prevent incurring unnecessary charges, the VM can be stopped or the resource group deleted when not in use.

Key Learnings

•
Understanding the relationship between Resource Groups, Virtual Networks, and Compute resources in Azure.

•
Configuring Network Security Groups to securely manage inbound traffic.

•
Utilizing RDP to access cloud-hosted Windows environments.




This project was completed as part of hands-on cloud computing practice.

