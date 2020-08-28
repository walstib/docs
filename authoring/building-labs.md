---
description: This article describes how to build a lab on the go deploy platform
---

# Building Labs

## Building Lab Images

We have simplified the process of building labs since the sunsetting of our self-service portal.  The two options below enable us to get labs live quickly and efficiently.

Labs can be a single fabric or multiple fabrics.  For example. you can host a cloud only lab such as AWS or have a mix of both AWS and a VM hosted in our datacenter that includes lab files or specific software pre-installed to carry out the lab actions.  See our [Cloud Share](../crs/) section for more information on how to create cloud based resources.

## Option 1 - Supply a Build Guide

The first option is to supply us with a build guide.  This does not need to be a full step by step guide of the entire setup but rather, high level steps stating your build requirements.  We have 100's of pre built templates that can be leveraged.  

For example

<table>
  <thead>
    <tr>
      <th style="text-align:left">VM</th>
      <th style="text-align:left">Details</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">LON-DC1</td>
      <td style="text-align:left">
        <p>Server 2019 Standard
          <br />IP: 172.16.0.10</p>
        <p>Domain Controller (contoso.com domain)</p>
        <p>DHCP (Scope: 172.16.200.1 - 200.99</p>
        <p>DNS</p>
        <p>IIS</p>
        <p>File Share called <b>Files </b>shared with<b> Everyone</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LON-SVR1</td>
      <td style="text-align:left">
        <p>Server 2019 Standard</p>
        <p>IP: 172.16.0.11</p>
        <p>Joined to contoso.com domain</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LON-SVR2</td>
      <td style="text-align:left">
        <p>Server 2019 Standard</p>
        <p>IP: 172.16.0.12</p>
        <p>Joined to contoso.com domain</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LON-CL1</td>
      <td style="text-align:left">
        <p>Windows 10 Enterprise Build 2004</p>
        <p>IP: 172.16.0.20</p>
        <p>Joined to contoso.com domain</p>
        <p>Office 2019</p>
        <p><em>Lab files copied to the Desktop</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LON-CL2</td>
      <td style="text-align:left">
        <p>Windows 10 Enterprise Build 2004</p>
        <p>IP: 172.16.0.21</p>
        <p>Joined to contoso.com domain</p>
        <p>Office 2019</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LON-WAP1</td>
      <td style="text-align:left">
        <p>Server 2019 Standard</p>
        <p>IP: 172.16.0.11</p>
        <p>Joined to contoso.com domain</p>
        <p>Requires a Public IP</p>
      </td>
    </tr>
  </tbody>
</table>

## Option 2 - Create your own VMs

The second option is to create the lab images locally then export them and upload to our storage system for us to import and distribute globally to our storage arrays.

You may download trial/evaluation editions of Microsoft Operating systems [here](https://www.microsoft.com/en-gb/evalcenter/).

Use Hyper-V on your local machine to create the images as required.  Export them and contact our support channel at https://aka.gd/support 

When submitting the creation request you must state the Network Names used for the labs and any other details we should know similar to Option 1.

## How do I configure internet connectivity?

When images are imported, a virtual gateway is configured to grant images internet connectivity.     

In general, these gateways will prohibit illegal content, coupled with sites that are generally unrelated to the goals of technical training. Antivirus, IPS Monitoring and DDoS prevention rules apply to all networks.

You are not required to create any form of gateway virtual machine.

## What features can I use in the build?

The majority of Hyper-V and VMware features can be utilised including:

* Nested Virtualization
* Static MAC Addresses
* MAC Address Spoofing
* Port Mirroring
* DHCP Guard
* Router Guard
* VLAN Tags
* Legacy Network Adapters
* ISO Images
* Virtual Floppy Disks
* Generation 1 or 2 machines
* Multiple Network Adapters
* Secure Boot
* Hide the Virtual Machine from the User
* Time Synchronisation 
* Do not start the VM on launch
* Switching of Network Adapters
* PXE booting
* Public IPs

## How long does this process take and can I change lab build?

Once we are in possession of the required resources to build a lab we aim to have this ready for you as quickly as possible.  We have dedicated resources internally that manage images 24/7.

The table below outlines the timeframes for creation and changes.

| Task | SLA | Average Time |
| :--- | :--- | :--- |
| Option 1 Build | 24 hours | ~ 2 hours |
| Option 2 Build | 48 hours | ~ 24 hours |
| Build Amendments | 8 hours | ~ 2 hours |
| Lab Guide Amendments | 8 hours | ~ 1 hour |

## How do I add Lab Guides?

Again, you have multiple options.  Provide us with lab guides in most formats and our content team can import these for you.  You can write your own using our lab guide editor or use GitHub.  Please see our [Lab Guide Authoring](lab-guide-authoring.md) section.

## Virtual Machine Build Tips

### Build a Windows Virtual Machine <a id="build-a-windows-virtual-machine"></a>

1. For Windows 10 and Server 2016/2019 allocate at least 4Gb of memory and 4 CPUs.  Increasing the specification does increase the cost however it is paramount that the VMs perform as expected.
2. Set screen resolution to **1024x768.**
3. Set the Power Options to **High Performance**, and then disable the **Turn off the display** and **Put the computer to sleep** settings otherwise VMs will go to sleep after 10 minutes by default and display a black screen in the lab environment.
4. In Advanced System settings, select **Adjust for best Performance**, and then check **Smooth Edges of Screen Fonts**.
5. In the Action Center, in Security and Maintenance, **disable all notifications**.
6. For security/cyber labs disable Windows Defender or create exceptions.
7. In Screen Saver, select **Turn Off**.
8. In Background, **select a solid colour or use BG Info**.
9. In Windows Firewall, select **Turn Off** \(if appropriate\).
10. Set the homepage of the browser to **`about:blank`**.
11. Clear any browser history.
12. Clear the **Recycle Bin**.
13. Disable Password Expiration \(Local and/or Domain\) for the Administrator account and any other account\(s\) that may be used.
14. Ensure that security certificates will not expire during the life of the lab.
15. Clear the Start menu history.
16. Empty the event logs.
17. Ensure that all virtual machines are set to a uniform time zone and are synchronised with each other.
18. Ensure that all software used on your virtual machine is properly licensed.
19. Disable the Windows Updates service and then set the Startup Type to Disabled.  
20. For Windows 10 machines, open `gpedit.msc` and navigate to **Computer Configuration &gt; Administrative Templates &gt; Windows Components &gt; Windows Updates &gt; Do not connect to any Windows Update Internet Locations.**  Set this to **Enabled**.  Failure to do this will result in the Windows 10 machine enabling the Windows Update service and having a significant impact on the performance. 

### Domain Controllers <a id="configure-a-virtual-machine-that-is-a-domain-controller"></a>

1. If there are multiple domain controllers in the lab environment, in Active Directory, increase the tombstone value to 1,000 days.
2. Where DNS is installed ensure forwarders are created for internet connectivity pointing to 8.8.8.8 and 9.9.9.9
3. Ensure you set the domain administrator account has disable password expiration set. Do the same for any other accounts that may be used.

### Configure Office 2013 or Later in a Virtual Machine <a id="configure-office-2013-or-later-in-a-virtual-machine"></a>

**Rearm Office**

1. Search for **OSPPREARM.EXE** for the version of Office installed, and then run **OSPPREARM.EXE** as an Administrator.

   > As an example, the default location for OSPPREARM.EXE in Office 2016 is **C:\Program Files \(x86\)\Microsoft Office\Office16**.

### Rearm Windows <a id="rearm-windows"></a>

1. At an elevated command prompt, run **`slmgr -rearm`**
2. Shut down the virtual machine.  Do not restart the machine.  This will require you to rearm the machine again.  Windows has a limit of 3 rearms.  You may wish to wait until the lab has been fully tested or let go deploy do this for you.



