# WindowsTools
[![License](https://img.shields.io/github/license/CongresoCDMX/WindowsTools)](https://www.gnu.org/licenses/gpl-3.0.en.html)
[![Release](https://img.shields.io/github/v/release/CongresoCDMX/WindowsTools?include_prereleases&sort=semver)](https://github.com/CongresoCDMX/WindowsTools/releases)

CLI tools, scripts and binaries for Windows administration



## Installation

### Prerequisites
Before you’re able to run PowerShell scripts on your machine, you need to set your local ExecutionPolicy to RemoteSigned (Basically anything except Undefined and Restricted). If you choose AllSigned instead of RemoteSigned, also local scripts (your own) need to be digitally signed in order to be executed. With RemoteSigned, only Scripts having the "ZoneIdentifier" set to Internet (were downloaded from the web) need to be signed, others not. If you’re an administrator and want to set it for all Users on that machine, use "-Scope LocalMachine". If you’re a normal user, without administrative rights, you can use "-Scope CurrentUser" to set it only for you.
```powershell
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
```

### PowerShell Gallery
If you have at least PowerShell 5 or PowerShell 4 with PackageManagement installed, you can use the package manager to install posh-git for you.
```powershell
Install-Module posh-git -Scope CurrentUser -Force
Install-Module posh-git -Scope CurrentUser -AllowPrerelease -Force
```

### Update PowerShell Prompt
To include git information in your prompt, the posh-git module needs to be imported. To have posh-git imported every time PowerShell starts, execute the Add-PoshGitToProfile command which will add the import statement into you $profile script. This script is executed everytime you open a new PowerShell console. Keep in mind, that there are multiple $profile scripts. E. g. one for the console and a separate one for the ISE.
```powershell
Import-Module posh-git
Add-PoshGitToProfile -AllHosts
```

### Clone this repository
```powershell
git clone git://github.com/CongresoCDMX/WindowsTools
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
