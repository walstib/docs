---
description: >-
  This article describes how to use the Azure Cloud Shell when using Cloud Share
  labs
---

# Azure Cloud Shell in Cloud Share

When you attempt to create storage for some labs you may receive an error that you do not have permission.  Cloud Share is designed to restrict users from carrying out certain actions.

In order to open the Cloud Shell you will need to create storage in a pre-provisioned Resource Group.  This is an easy process and takes just a few seconds.

Launch the Azure Cloud Shell.

Select either Bash or PowerShell.

Click **Show advanced settings**.  


![](../../../.gitbook/assets/image%20%2851%29.png)

Select the **East US** region.  Select **Use existing** Resource group and select the pre-provisioned resource group for the lab.

![](../../../.gitbook/assets/image%20%2827%29.png)

Enter a name for the storage account \(this must be unique\) and type **"**clouldshell" as the name of the File share then click **Create Storage.**

![](../../../.gitbook/assets/image%20%2810%29.png)

Your Cloud Shell will now launch.

