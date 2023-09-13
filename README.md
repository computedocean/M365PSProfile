# M365PSProfile

If you're an Microsoft 365 Administrator, you need to have several PowerShell Modules for Managing an M365 Environement..

We've created a flexible Module, that simplifies the Installation and Updatemanagement of these Modules.

## ToDo
### Andres
- Initiales Readme erstellen > done 13.09.2023
- Nachfolger PowerShellGet
- Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process

### Fabrice
- Funktionen Parametriesieren
- ModuleFast Youtube Video anschauen
- Microsoft.Graph Module Depenency paralellisierung 
```pwsh
# 	$Module = Find-Module Microsoft.graph
# 	$Module.Dependencies
```


## Goals
- Simple One-Liner in the [PowerShell Profile](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7.3)
- No Admin Rights required
- Support for PowerShell 5 and 7 (Install in CurrentUser)
- Parameter for Modules that should be installed and updated
- Fast and configurable
- Today the installation of AZ and Microsoft.Graph takes a long time.
  - Maybe try to analyze the dependency
  - Can the Installation be paralellized?

## Installation

You need to install the Module

```pwsh
Install-Module M365PSProfile
```

## Usage

Open the PowerShell Profile add the following Line

```
#Current user, Current Host
#Windows - $HOME\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
#Linux - ~/.config/powershell/Microsoft.PowerShell_profile.ps1
#macOS - ~/.config/powershell/Microsoft.PowerShell_profile.ps1
```

> Note:  Command might still Change

```pwsh
Update-ModuleCustom -Modules @("MSOnline", "AzureADPreview", "ExchangeOnlineManagement", "Icewolf.EXO.SpamAnalyze", "MicrosoftTeams", "Microsoft.Online.SharePoint.PowerShell", "PnP.PowerShell" , "ORCA", "O365CentralizedAddInDeployment", "MSCommerce", "WhiteboardAdmin", "Microsoft.Graph", "Microsoft.Graph.Beta", "MSAL.PS", "MSIdentityTools" )
```



## Modules 

| Module | Description |
| --- | --- |
| MSOnline | AzureAD / Entra ID Module > Depreciated 30.03.2024 |
| AzureADPreview | AzureAD / Entra ID Module > Depreciated 30.03.2024 |
| ExchangeOnlineManagement | Exchange Online |
| Icewolf.EXO.SpamAnalyze | Exchange Online Message Tracking / SpamAnalyze | 
| MicrosoftTeams | Microsoft Teams |
| Microsoft.Online.SharePoint.PowerShell | Microsoft Sharepoint | 
| PnP.PowerShell | SharePoint / Microsoft Teams |
| ORCA | Defender for Office 365 Recommended Configuration Analyzer |
| O365CentralizedAddInDeployment | Deploy Office Add-Ins | 
| MSCommerce | Manage M365 SelfServicePurchase | 
| WhiteboardAdmin | Manage Whiteboards |
| Microsoft.Graph | Microsoft.Graph Modules https://graph.microsoft.com/v1.0 | 
| Microsoft.Graph.Beta | Microsoft.Graph Modules https://graph.microsoft.com/beta |
| MSAL.PS | Microsoft Authentication Library | 
| MSIdentityTools | Additional Functions for Identity |

## Contribution
How can you contribute?

- Create an Issue
- Fork the Repo and create a Pull Request

## Maintainer
- Fabrice Reiser [@fabrisodotps1](https://twitter.com/fabrisodotps1)
- Andres Bohren [@andresbohren](https://twitter.com/andresbohren)
