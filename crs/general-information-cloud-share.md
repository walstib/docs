---
description: >-
  This article outlines some general information regarding the go deploy Cloud
  Share feature.
---

# General Information - Cloud Share

### **Azure Credentials**

When using labs that require Azure and are leveraging our Cloud Sharing feature, you will see the Azure credentials allocated on the Home tab of the lab environment.

### ‌**How do I complete the labs?**

‌You will be presented with a pre provisioned Resource Group which will allow you to create the resources as prescribed in the lab. There are no permissions to create Resource Groups or resources outside those required to complete the lab.

### ‌**Saving**

‌Labs cannot be saved. The labs must be completed within the lab session. Once the lab timer reaches 15 minutes remaining you will be able to extend the time of the lab by 1 hour using the pop-up box.

### ‌**Permissions errors**

‌When completing labs, you may find you receive an error regarding permissions. This will generally be caused by an incorrect/mistyping of a command. In the example below the first command completes successfully whereas the second command fails due to the Resource Group name having an additional "a" character at the start.

![](../.gitbook/assets/image%20%281%29.png)

### Deployment failures

Deployments will fail is lab instructions are not followed correctly.  For example, in the screenshot below you can see a deployment has failed due to a policy restriction.  Policies are set in place to stop resources from being created that are not required for the lab.  Attempting to create 512gb Virtual Machine when actually, you only need a 2gb Virtual Machine will fail.  This is by design and is not an error but a warning to state go check the deployment to ensure the lab steps have been carried out correctly.

![](../.gitbook/assets/image%20%2813%29.png)

