# Configure Azure resources with tools
## Scenario
Azure Administrators use tools to interact with the cloud environment and complete such as as:
* Deploying dozens or hundreds of resources at a time
* Configuring individual services using scripts
* Viewing rich reports across usage, health, costs and more
## Use Azure Cloud Shell
**Azure Cloud Shell** is an interactive, browser-accessible shell for managing Azure resources. Linux users can opt for a Bash experience, while Windows users can opt for Powershell.
## Azure Cloud Shell Features
* Temporary and requires a new or existing Azure Files share to be mounted
* Authenticates automatically for instant access to your resources.
* Runs on a temp host
* Persists $HOME using a 5-GB image held in your file share.
* Permissions are set as a regular Linux user in Bash.
## Use Azure Powershell
Azure PowerShell is a module that you add to enable you to connect to your Azure subscription and manage resources. For example, `New-AzVm` creates a virtual machine inside your Azure subscription.
```
New-AzVm `
	-ResourceGroupName "CrmTestingResourceGroup" `
	-Name "CrmUnitTests" `
	-Image "UbuntuLTS" `
...
```
### Az Module
Az is the formal name for the Azure PowerShell module containing cmdlets to work with Azure features.
* Resource Groups
* Storage
* VMs
* Microsoft Entra ID
* Containers
* Machine Learning
## Lab: Using Azure Powershell
### Launching PowerShell in Azure Portal
1. Click on **Cloud Shell**
2. Select Powershell
3. Show advanced settings
4. Provide name to Storage Account and File Share
5. Click **Create Storage**
### Create a resource group and an Azure managed disk by using Azure PowerShell
Run the following commands to create a resource group.
`$location = (Get-AzResourceGroup -Name az104-03b-rg1-68127).Location`
`$rgName = 'az104-03c-rg1-681427'
`New-AzResourceGroup -Name $rgName -Location $location`
To retrieve the properties of the newly created resource group, run the command as shown.
`Get-AzResourceGroup -Name $rgName`
```
$diskConfig = NewAzDiskConfig `
	-Location $location `
	-CreateOption Empty `
	-DiskSizeGB 32 `
	-Sku Standard_LRS
```
`$diskName = 'az104-03c-disk1'`
```
New-AzDisk `
	-ResourceGroup $rgName `
	-DiskName $diskName `
	-Disk $diskConfig `
```
Retrieve the properties of the newly created disk
`Get-AzDisk -ResourceGroupName $rgName -Name $diskName`
### Configure the managed disk by using Azure PowerShell
To increase the size of the Azure managed disk to 64 GB, run the command:
`New-AzDiskUpdateConfig -DiskSizeGB 64 | Update-AzDisk -ResourceGroupName $rgName -DiskName $diskName`
Verify that the change took effect:
`Get-AzDisk -ResourceGroupName $rgName -Name $diskName`
Verify the current SKU as Standard_LRS
`Get-AzDisk -ResourceGroupName $rgName -Name $diskName).Sku`
## Use Azure CLI
* Azure CLI is a command-line program to connect to Azure and execute administrative commands on Azure resources.
* Example: To restart a VM, you would use a command such as the following:
```
az vm restart -g MyResourceGroup -n MyVm
```
* If you want to find commands that might help you manage a storage blob:
```
az find blob
```
* To get a list of subgroups and commands for managing blob storage
```
az storage blob --help
```
## Lab: Azure CLI
### Tasks
1. Start a Bash session in Azure Cloud Shell
2. Create a resource group and an Azure managed disk by using Azure CLI
3. Configure the managed disk by using Azure CLI
### Task 1: Start a Bash Session in Azure Cloud Shell
1. Click Cloud Shell in the portal
2. Click dropdown, select Bash then confirm option
### Task 2: Create a resource group and an Azure managed disk by using Azure CLI
