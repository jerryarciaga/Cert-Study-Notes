# Introduction to Azure Resource Manager
* **Azure Resource Manager (ARM)** is a service that allows you to **manage** Azure resources.
* ARM is a collection of services in the Azure Portal so you can't simply type in "Azure Resources Manager".
* It is a management layer that allows you to:
	* Create, Update, Delete Resources
	* Apply Management features eg, Access Controls, Locks, Tags
	* Writing Infrastructure as Code (IaC) via JSON templates
* Features include:
	* Subscriptions
	* Management Groups
	* Resource Groups
	* Resource Providers
	* Resource Locks
	* Azure Blueprints
	* Resource Tags
	* Access Control (IAM)
	* Role-Based Access Controls (RBAC)
	* Azure Policies
	* Azure Templates
# Use Case
Think of Azure Resource Managere (ARM) as a **gate keeper**. All requests flow through ARM and it decides whether that request can be performed on a **resource**.
# Scoping
Scope is a **boundary of control** for Azure resources. It is a way to govern your resource by placing resources
* within a logical grouping
* and also applying logical restrictions in the form of rules
Some terminology regarding scoping:
* **Management Groups** a logical grouping of multiple subscriptions
* **Subscriptions** grants you access to Azure services based on a billing and support agreement
* **Resource Groups** A logical grouping of multiple resources
* **Resources** Azure service eg Azure VMs
# Subscriptions
Before you can do anything in your Azure account. You'll need to have a subscription. An Azure Account can have **multiple subscriptions** and the most common three are:
* Free Trial
* Pay-As-You-Go
* Azure for Students
* Developer Support
At the subscription level you'll have the ability to set:
* Resource Tags
* Access Controls
* Resources Groups and more
# Azure Management Groups
* Managing multiple subscriptions (accounts) into a hierarchical structure.
* Each directory is given a single top-level management group called the "Root" management group
* All subscriptions within a management group automatically inherit the conditions applied to the management group.
# Resource Groups
**Resource Group** a container that holds related resources for an Azure solution
**Resource** a manageable item that is available through Azure
**Resource Provider** A service that supplies Azure resources
# Resource Providers
* In order to use Azure resources you have to **register Resource Providers**. Many Resource Providers are registered by default for you with your subscription.
# Resource Tags
* Tag - key and value pair that you can assign to Azure resources
* Tags allow you to organize your resources in the following ways"
	* **Resource management** specific workloads, environments eg Developer Environments
	* **Cost management and optimization** Cost tracking, budgets, alerts
	* **Operations management** Business commitments and SLA operations eg, Mission-Critical Services
	* **Security** Classification of data and security impact
	* **Governance and Regulatory Compliance**
	* **Automation**
	* **Workload optimization**
# Resource Locks
As an admin, you may need to **lock a subscription, resource group, or resource** to **prevent other users from accidentally deleting or modifying critical resources.**
In the **Azure Portal** you can set the following lock levels:
* **CanNotDelete (Delete)** - Authorized users can still read and modify a resource, but they can't delete the resource
* **ReadOnly (Read-Only)** - Authorized users can read a resource, but they can't delete or update the resource
# Azure Blueprints