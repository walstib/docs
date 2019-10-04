---
description: This page describes Enhanced Mode (Full Screen / Sound)
---

# Enhanced Mode

Enhanced Mode enables Virtual Machines to fill the Virtual Machine screen area.  It also enables audio to be played on your local machines directly through the web browser.

Enhanced Mode should be turned on once the virtual machines have booted into the Ctrl + Alt + Delete screen and will only work with Windows 8.1 / Server 2012 R2 VMs onwards.  VMs with older releases of the operating system will remain functioning in the legacy mode but resolution can still be changed manually.

Changing the volume within the virtual machine will not produce any sound output but any audio sounds from applications \(such as Skype for Business or Outlook\) will function correctly.

{% hint style="danger" %}
**Note**: Enhanced mode will not work for users who are not a member of the Remote Desktop Users group on the virtual machine.  To change the resolution of the virtual machine console view, see this article: [Virtual Machine Resolution](virtual-machine-resolution.md)
{% endhint %}

**Note the following:**

1. If the lab has a virtual machine that is installing Windows \(ie the Windows PE\) or a VM running Linux / Windows 7 etc, you will see Enhanced Mode will be turned off as it is not supported in those Operating Systems.  You will need to turn Enhanced Mode back on when you change to a supported VM.
2. When you switch between Virtual Machines you will be promoted for the Password each time, this is expected.  Simply use the password paste feature.

