# HPWarranty PowerShell Module
## As HP has recently split into two different companies, this is a complete rewrite, and is still beta.  Cmdlet names and functionallity may change, I will not be supporting backwards compatibility.

This module can be installed from the [PowerShellGallery](https://www.powershellgallery.com/packages/HPWarranty/).  You need [WMF 5](https://www.microsoft.com/en-us/download/details.aspx?id=44987) to use this feature.
```PowerShell
Install-Module -Name HPWarranty
```

HP has recently split into two divisions, and this a first attempt to support both HP server and workstation warranty via PowerShell.
I currently have no way to check if a machine is a 'Server' or a 'Workstaion', so that falls on you, for now.  I have added the error returned from HP to the errorstream, so you should be able to tell what the issue is more easily.
This is still very beta, so please report any issues.  Thanks.

## HPWarranty Cmdlets

* [Get-HPComputerInformationForWarrantyFromCMDB](https://github.com/dotps1/HPWarranty/wiki/Get-HPComputerInformationForWarrantyFromCMDB)
* [Get-HPIncWarrantyEntitlement](https://github.com/dotps1/HPWarranty/wiki/Get-HPIncWarrantyEntitlement)
* [Get-HPWarrantyEntitlement](https://github.com/dotps1/HPWarranty/wiki/Get-HPWarrantyEntitlement)

Example 1:
```PowerShell
# Execute from local HP workstation.
Get-HPIncWarrantyEntitlement
```

Example 2:
```PowerShell
# Execute against remote HP workstation (must be on).
Get-HPIncWarrantyEntitlement -ComputerName 'MyFriendsHP.ourdomain.org'
```

Example 3:
```PowerShell
# Execute for local HP Server
Get-HPWarrantyEntitlement
```