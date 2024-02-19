# Azure Resources Management Cheat Sheet
**Azure Resource Manager (ARM)** is a service that allows you to **manage** Azure resources.
* It is a management layer that allows you to: Create, Update, Delete Resources.
	* Apply Management features eg. Access Controls, Locks, Tags
	* Writing Infrastructure as Code (IaC) via JSON templates
* ARM is a service layer that **spans multiple features and services**: Subscriptions, Management Groups, Resources Groups, Resource Providers, Resource Locks, Azure Blueprints, Resource Tags, Access Control (IAM), Role-Based Access Controls (RBAC), Azure Policies, ARM Templates
* Think of ARM as **gate keeper**
* **Scope** is a **boundary of control** for azure resources.
* **Management Groups** A logical grouping of multiple subscriptions
	* **Subscriptions** grants you access to Azure services based on billing and support agreement.
	* **Resource Groups** a logical grouping of multiple resources
	* **Resources** an Azure service eg. Azure VMs.
* An Azure Account can have **multiple subscriptions** and the most common three are: Free Trial, Pay-As-You-Go, Azure for Students
* **Resource Providers** A list of possible services with an Azure, some services are *registered* by default and other needs to explicitly registered
* **Resource Tags** is a **key and value pair** that you can assign to Azure resources.
* Resource Locks prevent users from accidentally modifying or deleting resources at the Subscriptions, Resource Group or Resource Scope
	* **CanNotDelete (Delete)** authorized users can still read and modify a  resource, but they can't delete the resource.
	* **ReadOnly (Read-only)** authorized users can read a resource, but they can't delete or update the resource.
* **Blueprints** enable quick creation of **governed subscriptions**.
	* Nearly everything that you want to include for deployment in Azure Blueprints can be accomplished with an ARM Template.
	* Nearly everything that you want to include for deployment in Azure Blueprints can be accomplished with an ARM Template.
	* Relationship between the blueprint definition (what *should* be deployed) and the blueprint assignment (what *was* deployed)