# Export all Azure VM details - with creator Tag 
This Script will just export all VM information together with the Creator Tag:

e.g.
```
CreatedBy user@domain
```

You need to Tag your VMs first before running this script. If you like you can use one of my other scripts for that:

- Automatic Tagging: 
This script is to search for VM creators in the Activity log and Tag each one with the correct creator.
Its build to be schduled via Azure Automtion
https://github.com/msghaleb/azure-automation-tag-vms-with-creators

- Tag and Export:
This script does both, tagging and exporting and it meant to run once initally, however if you want to do this periodically you will need to use the above script for e.g. weekly tagging and the one in this repo for on demand export.
https://github.com/msghaleb/azure-tag-export-vm-creators

After tagging it done this script will export all VMs from all Subscriptions the user has access to in a CSV file.

Each Subscription will have a seperate CSV file 
> Subscription--{Subscription Name}.csv

There will also be a single CSV file with all VMs 
> Subscription--All-VMs.csv

The script should work locally and on Azure Shell

## Install required PowerShell modules if not already installed
### If on Windows 10+
   > Install the latest version of WMF 
   > https://www.microsoft.com/en-us/download/details.aspx?id=54616
   > Then run 'Install-Module PowerShellGet -Force'
### If on Windows previous to 10
   > Install PackageManagement modules
   > http://go.microsoft.com/fwlink/?LinkID=746217
   > Then run 'Install-Module PowerShellGet -Force'

### Feel free to open a pull request if you like to improve this script
