# Introduction to Azure Policies
**Azure Policy** enforce organizational standards and to assess **compliance** at-scale
* Policies **do not restrict access**, they only observe for compliance
* **Policy Definitions** A policy definition is a JSON file used to describe business rules to control access to resources
* **Policy Assignment** The scope of a policy can effect. Assigned to a user, a resource group or a management group
* **Policy Parameters** Values you can pass into your Policy definition so your Policies are more flexible for re-use.
* **Initiative Definitions** An initiative definition is a collection of policy definitions, that you can assign. Example: A group of policies to enforce **PCI-DSS Compliance**
# Non-Compliant Resources
Once a policy is assigned it will evaluate for the compliance state periodically
# Azure Policy Definition File
## Anatomy of an Azure Policy Definition File
* **Display Name** Identifies the policy
* **Type**
	* Built-in - maintained by Microsoft
	* Custom - created by you
	* Static - Microsoft Owned, regulatory like HIPAA
* **Description** Provides the context of the policy
* **Metadata** Optional key value information to store on the policy in the policy
* **Mode** determines which resource types are evaluated. Changes whether using Resource Provider or Azure Resource Manager
	* **Resource Manager**
		* All - resource groups, subscriptions, and all resources types
		* Indexed - only resource types that support tags and location
	* **Resource Provider**
		* `Microsoft.ContainerService.Data` (Deprecated)
		* `Microsoft.Kubernetes.Data`
		* `Microsoft.KeyVault.Data`
* **Parameters** Values you can pass into the policy to allow the policy to be more flexible. A parameter has the following properties
	* **name**
	* **type**
	* **metadata**
	* **defaultValue**
	* **allowedValues**
* **Policy Rule** consists of `If` and `Then` blocks
* **Deny** The resource creation/update fails due to policy
* **Audit** Create a warning event in the activity log when evaluating a non-compliant resource, but doesn't stop the request
* **Append** Adds additional parameters/fields to the requested resource during creation or update. A common example is adding tags on resources such as Cost Center or specifying allowed IPs for a storage resource.
* **Audit If Not Exists** Create a warning event in the activity log when evaluating a non-compliant resource
* **Deploy If Not Exists** Executes a template deployment when a specific condition is met**
* **Disabled** This policy rule is ignored