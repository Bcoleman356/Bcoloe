Host a Static Website on Azure Cloud Storage

Overview

This repository documents the process of deploying and hosting a static website using Microsoft Azure Blob Storage. The project demonstrates a cost-effective and highly scalable method for serving HTML, CSS, and JavaScript content without the need to provision or manage web servers.

Objectives

•
Create an Azure Storage Account.

•
Enable the Static Website hosting feature.

•
Upload web assets (HTML, CSS, JS) to the $web container.

•
Access the live website via the primary endpoint URL.

Technologies Used

•
Cloud Provider: Microsoft Azure

•
Storage Service: Azure Blob Storage

•
Feature: Static Website Hosting

•
Web Technologies: HTML, CSS, JavaScript

Project Steps

1. Creating the Storage Account

1.
Logged into the Azure Portal.

2.
Navigated to Storage accounts and clicked Create.

3.
Configured the Basics tab:

•
Selected an existing or created a new Resource Group.

•
Provided a globally unique Storage account name.

•
Selected an appropriate region.

•
Chose Standard performance and an appropriate redundancy option (e.g., Locally-redundant storage - LRS).



4.
Clicked Review + create, validated the settings, and clicked Create.

2. Enabling Static Website Hosting

1.
Once the deployment was complete, navigated to the new Storage Account.

2.
In the left-hand menu, under Data management, selected Static website.

3.
Toggled the setting to Enabled.

4.
Configured the default document names:

•
Index document name: index.html

•
Error document path: 404.html (optional)



5.
Clicked Save.

6.
Copied the generated Primary endpoint URL (this is the public URL for the website).

3. Uploading Web Content

1.
Navigated to the Containers section under Data storage.

2.
Opened the newly created $web container.

3.
Clicked Upload and selected the static website files (e.g., index.html, style.css, script.js) from the local machine.

4.
Ensured the files were successfully uploaded to the container.

4. Verification and Access

•
Opened a web browser and navigated to the Primary endpoint URL copied earlier.

•
Verified that the static website loaded correctly and displayed the uploaded content.

•
(Optional) To secure the site with a custom domain and HTTPS, Azure Content Delivery Network (CDN) can be configured in front of the storage account.

Key Learnings

•
Utilizing Azure Blob Storage for cost-effective static content delivery.

•
Understanding the difference between server-based hosting and serverless storage hosting.

•
Managing Azure Storage containers and blobs.




This project was completed as part of hands-on cloud computing practice.

