# Azure Active Directory
# Introduction
## Intro to Azure AD
* **Azure AD** - Microsoft's cloud-based identity and access management service
* Can be used to implement SSO (Single-Sign On)
* Comes in four editions:
	1. Free - MFA, SSO, Basic Security and Usage Reports, User Management
	2. Office 365 Apps - Company Branding, SLA, Two-Sync between On-Premise and Cloud
	3. Premium 1 - Hybrid Architecture, Advanced Group Access, On-Premise and Cloud
	4. Premium 2 - Identity Protection, Identity Governance
# Use Case
* **Azure AD** can authorize and authenticate to multiple sources
# Active Directory vs Azure Active Directory
## Active Directory
* Introduced by Microsoft in **Windows 2000** to give organizations the ability to manage multiple on-premises infrastructure components and systems using a single identity per user.
## Azure AD
* **Azure AD** takes this approach by providing organizations with an Identity as a Service solution for all their apps across cloud and on-premises.
* Both are still used today
# Active Directory Terminology
## Domain
A domain is an area of a network organized by a single authentication database.
**An Active Directory domain** is a **logical grouping** of AD objects on a network.
## Domain Controller
Server that authenticates user identities and authorizes their access to resources.
## Domain Computer
Computer registered with a central authentication database. This would be an AD Object.
## AD Object
Basic element of a Active Directory such as: Users, Groups, Printers, Computers, Shared Folders
## Group Policy Object
Virtual collection of policy settings. Controls access for AD Objects.
## Organizational Units (OU)
Subdivision within Active Directory where you place AD Objects to. Provides logical grouping.
## Directory Service
Provides the methods of storing directory data and making data available to network users and administrators. Runs on a Domain Controller.
# Azure AD Tenant
* A **tenant** represents an organization in Azure Active Directory.
* Automatically created when you sign up for either
	* Microsoft Azure
	* Microsoft Intune
	* Microsoft 365
# Azure AD Domain Services (AD DS)
* AD DS provides **managed domain service** such as:
	* Domain joins
	* Group policies
	* Lightweight directory access protocol (LDAP)
	* Kerberos/NTLM authentication
# Azure AD Connect
* **Azure AD Connect** is a hybrid service to connect your on-premise Active Directory to your Azure Account
* Allows for SSO from your on-premise workstation to Microsoft Azure
* Azure AD Connect has the following features:
	* **Password Hash Synchronization** - sign-in method, synchronizes a hash of a users on-premises AD password with Azure AD.
	* **Pass-through authentication** - sign-in method, allows users to use the same password on-premises and in the cloud.
	* **Federation integration** - hybrid environment using an on-premises AD FS infrastructure, for certificate renewal
	* **Synchronization** - Responsible for creating users, groups, and other objects, ensures on-prem and cloud data matches
	* **Health Monitoring** - robust monitoring and provide a central location in the Azure portal (Azure AD Connect Health) to view this activity.
# Azure Active Directory Users
* Users represent and **identify for a person or employee** in your domain. A user has login credentials and can use them to log into the Azure portal.
* You can assign **admin roles** to users
* You can add users to groups
* You can enforce authentication methods such as (MFA) Multi-Factor Authentication
* You can track user sign ins
* Track devices user's login from and allow and deny devices
* Assign Microsoft Licenses
* Azure AD has two kinds of users:
	* Users - a user belongs to your organization
	* Guest Users - A guest user belongs to another organization
# Active Directory Groups
**Groups** let the resource owner (or Azure AD directory owner) assign a set of access permissions to all the members of a group, instead of having to provide the rights one-by-one.
* Groups contain:
	* **Owners** - Has permissions to add and remove members
	* **Members** - has permissions to do things
* Assignment
	* You can assign roles directly to a group
	* You can assign applications directly to a group.
## Request to Join Groups
The group owner can let users find their groups to join, instead of assigning them. The owner can also set up the group to automatically accept all users that joint or to require approval.
# AD Assign Access Rights
* Four ways to **assign access rights** to your users:
	* **Direct Assignment** - the resources owner directly assigns the user to the resources.
	* **Group Assignment** - resource owner assigns an Azure AD group to the resource, giving all of the group members access to the resource
	* **Rule-Based Assignment** - The resource owner creates a group and uses a rule to define which users are assigned to a specific resource.
	* **External Authority Assignment** - Access comes form an external source, such as an on-premises directory or a SaaS app.
# External Identities
**External Identities** in Azure AD, allow people outside your organization to access your apps and resources, while letting them sign in whatever identity they prefer.
* Share apps with external users (B2B collaboration)
* Develop apps intended for other Azure AD tenants (single-tenant or multi-tenant)
* Develop white-labeled apps for consumers and customers (Azure AD B2C)
# Follow Along
## Create a Tenant
1. Go to https://portal.azure.com and log in.
2. Type in search bar: **Azure Active Directory**
	Note: Azure Active Directory is now called **Microsoft Entra ID**
3. Click on **Manage Tenants**
4. Click **Create Tenant**. Take note of the following options:
	1. Microsoft Entra ID - Business to Business
	2. Azure AD B2C - Business to Consumer
5. Click **Configure**
6. On configuration, enter the following information:
	1. Organization Name
	2. Initial Domain Name
	3. Location
7. Click **Review + Create**
8. Wait a few minutes until a tenant has been created.
## Upgrade License
1. Switch between tenants by search for Microsoft Entra ID then clicking to the new tenant. Then click Switch Tenants.
2. Click on **Licences** on the left hand corner.
3. Click on **All Products** then **Try/Buy**.
4. Click on desired license
	1. Microsoft Entra ID Governance
	2. Microsoft Entra ID P2
5. Wait until your license has been upgraded to desired license
## User and Groups
* Since users require a group, you cannot create users without a group. You will have to create a group then create a user.
### Create a Group
1. Click **Add**, then **Group**.
2. Fill in the following information:
	1. **Group Type**: **Security** (could be users, devices, service principals) of **Microsoft 365** (could only be users)
	2. **Group Name**
	3. **Group Description**
	4. **Membership Type**: only **Assigned** is available for the free tier
3. Click **Create Group**
### Create a User
1. On the left side of the **Microsoft Entra ID Dashboard**, click on **Users**
2. Click on **Add**, then **User**
3. Enter required info, then click **Create**