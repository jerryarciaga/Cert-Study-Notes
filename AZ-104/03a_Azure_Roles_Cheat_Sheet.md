# Azure Roles Cheat Sheet
* Within Azure there are 3 kinds of roles:
	* **Classic subscription administrator roles** This is the original role system
	* **Azure roles** known as Role-Based Access Controls (RBAC), built on top of Azure Resource Manager
	* **Azure Active Directory (Azure AD) roles** used to managed Azure AD resources in a directory
* **Identity Access Management (IAM)** allows you to create and assign Azure (RBAC system) roles to users
* Roles restrict access to resource actions (operations). Two types of roles:
	* Built-in Role - Managed Microsoft roles are read only pre-created roles for you to use
	* Custom Role - A role created by you with your own custom logic
* **Role assignment** is when you apply a role to user. A role assignment is composed of a Security Principle, Role definition and Scope
* Azure's 4 built in roles are: **Owner, Contributor, Reader, User Access Administrator**
* **Classic Administrators
	* **Account Administrator
	* **Service Administrator**
	* **Co-Administrator**
* **Important Azure AD Roles**
	* Global administrator
	* User administrator
	* Billing Administrator
* For custom Azure AD Roles you need either **Azure AD Premium P1 or P2**