---
description: >-
  This article outlines the considerations and recommendations for ARM templates
  as part of a Cloud Sharing feature on the go deploy platform.
---

# ARM Template Best Practices

This article outlines the considerations and recommendations for those who wish to use Azure ARM templates as part of a Cloud Sharing deployment.  This guidance is no substitute for thorough testing, and all templates should be fully tested before release and on a regular basis see [Testing Arm Templates](testing-arm-templates.md). Azure frequently changes, and changes may have an impact on existing labs or deployments.

### Preparing an ARM Template for Cloud Sharing. <a id="preparing-an-arm-template-for-deployment-in-cloud-slice"></a>

A cloud share lab may contain one or more resource groups, in fact, up to the limit of Azure which is currently 980.   However, by reaching this limit means you will need multiple subscriptions in a subscription pool for multiple users to be able to launch a lab.

Each resource group can consist of one or more ARM templates deployed concurrently. A cloud share lab will, by default, contain one user account, but can have multiple user accounts deployed. User accounts can be assigned access to resource groups based on the build-in roles of Contributor, Owner, and Reader.

The recommended process for building and testing an ARM template for use with Cloud Sharing is as follows.

1. Log into your Azure Subscription and create a new RG.
2. Create and configure the resources that you want deployed for students within your RG.
3. Once you have your resources the way you want, use Azure to view/export the script. Take note of any messages related to resources/config that are not applied to the RG -- these will require either manual updates to the ARM template.
4. Save both the ARM script and the parameters to disk.
5. Test deployment of your ARM template into a new RG in the same subscription, in the region where you want the resources deployed, from outside of Azure, using a user account that only has Contributor access to that RG \(no subscription level access\) see [Testing Arm Templates](testing-arm-templates.md)
6. Once you confirm your ARM template deploys successfully, delete the RG and its contents.
7. Modify your ARM template so that any resources requiring unique names \(either unique across a subscription or globally unique\) are appropriately randomized so that no matter how many students launch the lab, their deployments will all succeed. This requires using ARM template functions and/or replacement tokens in the ARM template. Refer to details in the Recommendations and Best Practices section, below, for guidance on name randomization.
8. Test deployment of your updated ARM template, into a new, empty RG in the same fashion that you did in step 6. Ensure that all resources are created in the same region as your RG. Once it is working, delete the RG and its contents.
9. Copy and paste your template directly into a new Cloud Share Lab.
10. Launch the lab, and make sure everything from the template is deployed with the expected results. 
11. Now launch the lab twice, as two separate users, and make sure that both labs launch successfully. This verifies that resource naming is properly configured. This must be done in a Cloud Share Subscription Pool containing a single subscription. If the first launch succeeds but you get errors on deployment of the second launch, then from experience, this is due to resources not having a unique name and conflicts exist.

### Valid ARM Templates <a id="valid-arm-templates"></a>

Any valid Azure ARM template can be used as the basis of a Cloud Share lab providing it meets the following criteria.

1. Uses Resource Group deployments unless you have enough Azure subscriptions to allocate one to each user.  go deploy will remove any associated/deployed resources to either subscription or Resource Groups once a lab is ended.   
2. Has no dependencies on other templates – All templates are deployed concurrently.  For a lab to be considered deployed, all templates must successfully deploy. Any dependent resources should be contained within a single template.
3. Ensure only relative reference ID's are included – Templates generated from deployed Azure resources can contain fixed references to resources in subscriptions. These must be removed or generalized prior to deployment to ensure the template does not contain dependencies on objects that may not exist in the subscription targeted for deployment.

### Recommendations and Best Practices <a id="recommendations-and-best-practices"></a>

1. Avoid referencing templates from public repositories that you do not control. These templates may and will change without notice and break your lab.
2. The region for where your lab will be deployed is controlled by the Cloud Sharing platform and therefore does not need to be referenced in your template.  This can be easily changed at any time.
3. For any object requiring a unique name, use "\[concat\(',uniquestring\(resourceGroup\(\).id\)\]" where is some value relevant to your lab, such as MyRG.
4. Do not hard-code usernames and passwords in the template, instead use template parameters such as adminUsername and adminPassword to enable credentials to be set at lab design time, and allow different labs using the same template.  This saves repetitive work.
5. If the lab template deploys virtual machines, the sizing of the virtual machine should be captured in a template parameter. This enables sizing information to be easily changed if the deployment region changes, and the currently configured size is not available in the new region.



