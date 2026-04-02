# Automate Azure Static Website Deployment with Terraform

## Overview
This repository contains Infrastructure as Code (IaC) using Terraform to automate the deployment of a static website hosted on Microsoft Azure Blob Storage. The project demonstrates how to provision storage resources, configure static website hosting, and upload web content programmatically without relying on the Azure Portal interface.

## Objectives
- Use Terraform to define and provision Azure Storage infrastructure.
- Automate the creation of a Resource Group and a Storage Account.
- Enable the Static Website hosting feature on the Storage Account.
- Programmatically upload an index.html file to the $web container.

## Technologies Used
- **Infrastructure as Code (IaC):** Terraform v1.14.8
- **Cloud Provider:** Microsoft Azure
- **Command Line Tools:** Azure CLI v2.84.0
- **Editor:** Visual Studio Code
- **Storage Service:** Azure Blob Storage
- **Web Technologies:** HTML

## Project Architecture
The Terraform configuration (main.tf) provisions the following resources in Azure:

| # | Resource | Name / Configuration |
|---|---|---|
| 1 | Resource Group | TF-Storage-ResourceGroup (East US) |
| 2 | Storage Account | tfstorageacct2026 (Standard LRS) |
| 3 | Static Website | Enabled (Index document: index.html) |
| 4 | Storage Blob | index.html uploaded to the $web container |

## Prerequisites
- Terraform downloaded and placed in C:\terraform
- Azure CLI installed
- An active Microsoft Azure subscription
- Visual Studio Code (recommended editor)

## Deployment Steps

### Step 1 - Authenticate with Azure
Open a terminal and log in to your Azure account:
az login --tenant <your-tenant-id>

### Step 2 - Navigate to the Project Folder
cd C:\terraform\azure-storage

### Step 3 - Initialize Terraform
Downloads the required Azure provider plugins:
C:\terraform\terraform.exe init

### Step 4 - Preview the Execution Plan
Shows all resources that will be created without making any changes:
C:\terraform\terraform.exe plan

### Step 5 - Deploy to Azure
Provisions all resources in Azure. Type yes when prompted:
C:\terraform\terraform.exe apply

### Step 6 - Clean Up Resources (Optional)
Destroys all resources created by Terraform to avoid unnecessary charges:
C:\terraform\terraform.exe destroy

## Key Learnings
- Deploying and configuring serverless web hosting entirely through code.
- Managing Azure Blob Storage containers ($web) and uploading files programmatically using Terraform's azurerm_storage_blob resource.
- Understanding how to read and safely ignore deprecation warnings such as the static_website block warning in the Azure provider.

---
This project was completed as part of hands-on cloud automation and DevOps practice.
