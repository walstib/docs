# PowerShell - Module Install issue

**This is a fast release article.**

When install PowerShell modules you may receive an error similar to the below:  
  
`PackageManagement\Install-PackageProvider : No match was found for the specified search criteria for the provider  
 'NuGet'. The package provider requires 'PackageManagement' and 'Provider' tags. Please check if the specified package  
 has the tags.  
 At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:7294 char:21  
 + ...     $null = PackageManagement\Install-PackageProvider -Name $script:N ...  
 +                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~  
     + CategoryInfo          : InvalidArgument: (Microsoft.Power...PackageProvider:InstallPackageProvider) [Install-Pac  
    kageProvider], Exception  
     + FullyQualifiedErrorId : NoMatchFoundForProvider,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackagePro  
    vider`

To work around this issue, run the following command:

`[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12`

Once this command has been ran, attempt to install the module again.

