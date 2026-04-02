# Automate Azure Virtual Machine Deployment with Terraform

## Overview
This repository contains Infrastructure as Code (IaC) using Terraform to automate the deployment of a Windows Virtual Machine in Microsoft Azure. The project demonstrates how to provision and manage cloud infrastructure programmatically, ensuring repeatable and consistent environments.

## Objectives
- Use Terraform to define and provision Azure infrastructure.
- Automate the creation of a Resource Group, Virtual Network, Subnet, and Public IP.
- Deploy a Windows Server 2022 Datacenter Virtual Machine.
- Understand and resolve common Azure deployment limitations such as updating Basic SKU Public IPs to Standard SKU.

## Technologies Used
- **Infrastructure as Code (IaC):** Terraform v1.14.8
- **Cloud Provider:** Microsoft Azure
- **Command Line Tools:** Azure CLI v2.84.0
- **Editor:** Visual Studio Code
- **Compute:** Azure Virtual Machines (Windows Server 2022 Datacenter)
- **Networking:** Azure Virtual Network, Subnet, Public IP (Standard SKU), Network Interface

## Project Architecture
The Terraform configuration (main.tf) provisions the following 6 resources in Azure:

| # | Resource | Name |
|---|---|---|
| 1 | Resource Group | TF-VM-ResourceGroup |
| 2 | Virtual Network | tf-vm-vnet (10.0.0.0/16) |
| 3 | Subnet | tf-vm-subnet (10.0.1.0/24) |
| 4 | Public IP Address | tf-vm-publicip (Static, Standard SKU) |
| 5 | Network Interface | tf-vm-nic |
| 6 | Windows Virtual Machine | tf-windows-vm (Standard_B1s) |

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
cd C:\terraform\azure-vm

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

## Troubleshooting
During this project the following error was encountered and resolved:

Error: IPv4BasicSkuPublicIpCountLimitReached - Cannot create more than 0 IPv4 Basic SKU public IP addresses for this subscription in this region.

Fix: Updated the Public IP resource in main.tf from Dynamic allocation with Basic SKU to Static allocation with Standard SKU:

resource "azurerm_public_ip" "vm_pip" {
  name                = "tf-vm-publicip"
  location            = azurerm_resource_group.vm_rg.location
  resource_group_name = azurerm_resource_group.vm_rg.name
  allocation_method   = "Static"
  sku                 = "Standard"
}

## Key Learnings
- Transitioning from manual Azure Portal deployments to automated Infrastructure as Code deployments using Terraform.
- Understanding the full Terraform workflow: init, plan, apply, and destroy.
- Diagnosing and resolving Azure API errors by updating Terraform configurations to meet current Azure provider requirements.
- Adding C:\terraform to the Windows system PATH for easier command execution.

---
This project was completed as part of hands-on cloud automation and DevOps practice.
