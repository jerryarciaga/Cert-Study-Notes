# Introduction
## What is Device identity management?
The management of **physical devices** such as **phones, tablets, laptops and desktop** computers, that are granted access to company resources such as Printers, Cloud Resources via **device-based Conditional Access.**
* Allows remote employees to use their own personal equipment (BYOD - bring your own device)
* A way to protect their organization's assets such as access to cloud resources - they have less control over physical equipment!
## 3 Ways to get devices into Azure AD
* **Azure AD Registered**
	* **personally** owned or mobile devices
	* signed in with a **personal** or local account
* **Azure AD Joined**
	* owned by an **organization**
	* signed with an Azure AD account belonging to an organization
	* They exist **only in the cloud**
* **Hybrid Azure AD Joined**
	* owned by an **organization**
	* and signed in with an Active Directory Domain Services account belonging to that organization
	* exists in the **cloud and on-premises**
# AD Registered Devices
* **Definition** Registered to Azure AD without requiring organizational account to sign in to the device
* **Primary audience** BYOD, Mobile devices
* **Device Ownership** User or organization
* **Operating Systems** Windows 10, iOS, Android, and MacOS
* **Provisioning**
	* Windows 10 - Settings
	* iOS/Android - Company Portal or Microsoft Authenticator app
	* MacOS - Company portal
* **Device sign in options**
	* End-user local credentials, Password, **Windows Hello**, PIN
	* Biometrics or Pattern for other devices
* **Device management**
	* **Mobile Device Management** (example: **Microsoft Intune**)
	* **Mobile Application Management**
* **Key capabilities**
	* SSO to cloud resources
	* Conditional access when enrolled into Intune
	* Conditional access via App protection policy
	* Enables Phone sign in with **Microsoft Authenticator app**
# Windows Hello
## Windows Hello
Gives Windows 10 users an alternative way to log into their devices and applications using fingerprints, iris scan, facial recognition
# Mobile Device Management and Mobile Application Management
* Most important concept in device management
* MDM and MAM is managed via **Microsoft Intune**
* To use Microsoft Intune you have to upgrade to **Azure AD Premium 2**
* Microsoft Intune is part of **Microsoft Endpoint Manager**
* Both are part of **Microsoft Enterprise Mobility + Security (EMS)**
* Intune = Endpoint Manager = EMS
## Mobile Device Management (MDM)
Controls the entire device, can wipe data from it, and also reset to factory settings.
## Mobile Application Management (MAM)
Publish, push, configure, secure, monitor, and update mobile apps for your users.
# Enterprise Mobility + Security
Intelligent mobility maangement and security platform. Protect and secure your organization and empowers your employees to work in new and flexible ways. EMS is an **umbrella** of multiple Microsoft and Azure services
* Definitely remember these:
	* Azure Active Directory
	* Microsoft Intune
# Microsoft Authenticator App
Secure sign-ins for all your online accounts using MFA, passwordless, password autofill
# AD Joined Devices
* **Definition** joined only to Azure AD requiring organizational account to sign-in to the device.
* **Primary audience**
	* Suitable for both cloud-only and hybrid organizations
	* Applicable to all users in an organization
* **Operating Systems**
	* All Windows 10 devices **except Windows 10 Home**
	* Windows Server 2019 Virtual Machines running in Azure (Server core is not supported)
* **Provisioning**
	* Self-service: Windows OOBE and or Settings, Bulk enrollment, Windows Autopilot
* **Key capabilities**
	* SSO to both cloud and on-premises resources
	* Conditional Access through MDM enrollment and MDM compliance evaluation
	* Self-service Password Reset and Windows Hello PIN reset on lock screen
# FIDO 2.0 Security Keys
* Stands for Fast Identity Online Alliance
* Three sets of **open specifications** for simpler, stronger user authentication:
	* FIDO Universal Second Factor (FIDO U2F)
	* FIDO Universal Authentication Framework (FIDO UAF)
	* Client to Authenticator Protocols (CTAP)
	* CTAP is complementary to W3C's Web Authentication(WebAuthn), together known as FIDO2
## Security Key
Used as second step in authentication process to gain access to a device, workstation or application. Can resemble a memory stick
* A popular brand of security key is an Yubikey - works out of the box with Gmail, Facebook, and hundreds more
* Supports **FIDO2**/WebAuthn, U2F
# Hybrid Azure AD joined devices
* **Definition** Joined to on-premises or Azure AD requiring organizational account to sign in to the device
* **Primary audience** Suitable for hybrid organization with existing on-premises AD infrastructure
* **Device Ownership** organization
* **Device management**
	* Group Policy, Configuration Manager standalone or co-management with Microsoft Intune
* **Key Capabilities**
	* SSO to both cloud and on-premises resources
	* Conditional access through Domain join or through Intune if co-managed
	* Self-service Password Reset and Windows Hello PIN reset on lock screen
	* Enterprise State Roaming across devices
# Windows Autopilot
**Windows Autopilot** is a collection of technologies used to set up and pre-configure new devices, getting them ready for productive use.
* When initially deploying new Windows devices
	* Windows Autopilot uses the OEM-optimized version of Windows 10
* Instead of re-imaging the device, your existing Windows 10 installation can be transformed into a "business-ready" state that can that can be managed with Microsoft Intune, Windows Update for Business, Microsoft Endpoint Configuration Manager and other similar tools.