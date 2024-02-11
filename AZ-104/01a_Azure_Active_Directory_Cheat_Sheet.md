# Azure Active Directory Cheat Sheet
* **Active Directory**: Microsoft's **identity and access management service**.
* **Azure Active Directory (Azure AD)**: Microsoft's cloud-based version of AD. **Identity as a Service (IDaaS)**. Also now more known as **Microsoft Entra ID**
* Azure Active Directory comes in **4 editions**:
	* **Free**: MFA, SSO, Basic Security and Usage Reports, User Management
	* **Office 365 Apps**: Company Branding, SLA, Two-Sync between On-Premise and Cloud
	* **Premium 1 (P1)**: Hybrid Architecture, Advanced Group Access, **Conditional Access**
	* **Premium 2 (P2)**: Identity Protection, Identity Governance
* **Azure AD** can **authorize** and **authenticate** to multiple sources
* Active Directory Terminology:
	* **Domain** A domain is an area of a network organized by a single authentication database
	* **Active Directory domain** is a **logical grouping** of AD objects on a network
	* **Domain Controller (DC)** A domain controller is a server that **authenticates** and **authorizes** their access to resources
	* **Domain Computer** A computer that is registered with a central authentication database.
	* **AD Object** a basic element of AD such as: Users, Groups, Printers, Computers, Shared Folders
	* **Group Policy Object(GPO)** A virtual collection of policy settings
	* **Organization Units** subdivision within AD
	* **Directory Service** provides the methods of storing directory data and making this data available to network users and administrators
	* **A tenant represents an organization** in Active Directory. A tenant is automatically created when you sign up for either: Microsoft Azure, Microsoft Intune, Microsoft 365.
* Not all AD features are supported and in that case you need to use AD DS
* **Azure Active Directory Domain Services (AD DS)** provides **managed domain services** such as: Domain joins, Group policiees, LDAP, Kerberos
* Azure AD Connect has the following features
	* **Password hash synchronization**
	* **Pass-through authentication**
	* **Federation integration**
	* **Synchronization**
	* **Health Monitoring**
* **Users** represent an **identity for a person or employee** in your domain.
* Azure AD has two kinds of users:
	* **Users** - A user belongs to your organization
	* **Guest Users** - A guest user belongs to another organization
* **Groups** let the resource owner assign a set of access permissions to all the members of the group, instead of having to provide the rights one-by-one.a
* Groups contain:
	* Owners
	* Members
* Assignment - you can assign roles and assignment directly to a group
* **Request to join groups** The group owner can let users find their own groups to join, instead of assigning them.
* Four ways to **assign resource access rights** to your users
	* **Direct assignment** The resource owner directly assigns the user to the resource
	* **Group assignment** Assigns an Azure AD group to the resource, which automatically gives all of the group members access to the resource
	* **Rule based assignment** creates a group and a rule which users are assigned to a specific resource
	* **External authority assignment** Access comes from an external resource, such as an on-premises directory or a SaaS app