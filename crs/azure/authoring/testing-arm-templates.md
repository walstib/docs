---
description: >-
  This article will show you how you can test and deploy your ARM template using
  several different tools.
---

# Testing ARM Templates

There are other options available to test ARM templates prior to using them on the Cloud Sharing platform.  Many of these methods can be used locally.  In this article we will look at different tools that can help you with testing ARM templates.

### Using Visual studio code ARM extension

Using [Visual Studio Code](https://code.visualstudio.com/) for your development means you can use the free ARM Tools extension.  You can almost let the extension write the ARM templates for you. As authoring templates is outside the scope of this article and we are concentrating on testing, the extension will tell you when errors exist in your deployment or when you are not following best practices. It will even connect parameter files to check if your parameters are valid.

Here is an example:

![\(Figure 1\)](../../../.gitbook/assets/image%20%2890%29.png)

In Figure 1, a property is missing from the template. There is a small yellow line that asks for your attention. If you hover your mouse over it, it displays the problem.

In the next example \(Figure 2\), a variable in the template has not been defined. The extension finds this issue and warns you.

![\(Figure 2\)](../../../.gitbook/assets/image%20%2891%29.png)

You can download the extension [here](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools).

### Validation check

When deploying with [PowerShell](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-powershell?view=azps-4.5.0) or [Azure CLI](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli), there is a built in validation check. This checks if the ARM template is in a valid format. It can also identify errors that will prevent your deployment from working.  
In PowerShell, you would use the same syntax as _`New-AzResourceGroupDeployment`_, but replace New with Test.

In the example in Figure 3 shows an error for a template with a storage account name that is not permitted.

![](../../../.gitbook/assets/image%20%2889%29.png)

 With the Azure CLI, you  use _`az deployment group validate`_ 

![](../../../.gitbook/assets/image%20%2887%29.png)

### PowerShell: What if

The PowerShell What-if is a relatively new option that is currently in Preview.  This enables you to check your ARM template against your subscription. It will show you if resources will be created, modified or removed. This is most useful to identify of you have made a typo somewhere.

To use WhatIf, you need to make sure you are running a preview version of the Azure Resources module.  
The cmdlet is like this:

`$Parameters = @{   
      ResourcegroupName = "ARMTesting"   
      Templatefile = ".\azuredeploy.json"   
      StorageAccountPrefix = "arm"   
      Mode = 'Incremental'   
}   
New-AzResourceGroupDeployment @Parameters -WhatIf`

The result:

![](../../../.gitbook/assets/image%20%2888%29.png)

### ARM-TTK

The Azure Resource Manager Template Toolkit \(arm-ttk\) is a set of **best practices** that you can run against your ARM templates.  **Note**:  It does not validate or check your template works, but rather checks if it is written in a clean and efficient way which ensures resources are deployed much faster for students.  For example, this tool is used to test the templates in the[ Azure Quickstart templates](https://github.com/Azure/azure-quickstart-templates) that Microsoft provide.

You can directly install the ARM toolkit from the GitHub repository, or clone the repository to your local computer. You can find the repository on [GitHub](https://github.com/Azure/arm-ttk/).

Once you have downloaded the files to your local machine, import the module to your session by using import-module

| `Import-Module .\arm-ttk.psd1` |
| :--- |


Once complete you can test your template\(s\) with the following cmdlet

| `Test-AzTemplate -TemplatePath .\azuredeploy.json` |
| :--- |


![Testing ARM templates with AZTKT](https://4bes.nl/wp-content/uploads/2020/08/TestARM05.png)

We hope this article gives you some hints and tips which will benefit the authoring of your labs.

_Credit to_ [_https://4bes.nl/_](https://4bes.nl/) _for the majority of this article and screenshots._

