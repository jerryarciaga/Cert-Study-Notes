# Types of Azure Roles
## 3 Types of Roles that can serve the same purpose
* **Classic subscription administrator roles**
	* Original role system
* **Azure roles**
	* Authorization system is known as Role-Based Access Controls (RBAC) and is built on top of Azure Resource Manager
* **Azure Active Directory (Azure AD) roles**
	* Azure AD Roles are used to managed Azure AD resources in a directory
# IAM Access Controls
**Identity Access Management (IAM)** allows you to create and assign roles to users.
* **Azure Roles(RBAC System)**
	* Roles restrict access to resource actions (aka operations). Two types of roles:
	1. Builtin Role - Managed Microsoft roles are read only pre-created roles for you to use
	2. Custom Role - Role created by you with your own custom logic
* **Role Assignment**
	* Is when you apply a role to a service principle, (user) group or user
* **Deny Assignments**
	* block users from performing specific actions even if a role assignment grants them access. The only way to apply **Deny Assignments** is through **Azure BluePrints**
# Classic Administrators
**Classic Administrators** is the **original role system**. You <u>should use the new RBAC system</u> when possible.