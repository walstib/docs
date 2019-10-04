---
description: My virtual machine is running slow.  What can I do?
---

# Virtual Machine running slow

All virtual machines hosted on the go deploy platform are over spec'd to ensure performance isnt impacted within the lab environments.

However, in the unlikely even you are experiencing slow performance of a virtual machine, we recommend firstly that your location meets out [connectivity requirements](../general/connectivity-requirements.md).

If all requiements have been met and you are still expericing slow performance inside your virtual machines, there is a possibility that the Windows Update service is downloading and attepting to install a new update.

This can be stopped by carrying out the following actions:

1. Open the Run command \(Win + R\), in it type: services.msc and press enter
2. From the Services list which appears find the Windows Update service and open it
3. In ‘Startup Type’ \(under the ‘General’ tab\) change it to ‘Disabled’
4. Restart the virtual machine if necessary

![](../.gitbook/assets/image%20%2878%29.png)

