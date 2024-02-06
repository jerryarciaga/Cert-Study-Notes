# Describe Cloud Computing
## Introduction to Microsoft Azure Fundamentals
* Services in the cloud
	* web services
	* remote storage
	* database hosting
	* centralized account management
	* AI, IoT
###  Why should I take Azure Fundamentals
| AZ-900 Domain Area | Weight |
| ---- | ---- |
| Describe cloud concepts | 25-30% |
| Describe Azure architecture and services | 35-40% |
| Describe Azure management and governance | 30-35% |
## Introduction to cloud computing
### What is cloud computing
* Cloud computing is the delivery of computing services over the internet. Cloud services also expand the traditional IT offerings to include things like IoT, ML and AI.
### Describe the shared responsibility model
* With an on-premises datacenter, you're responsible for everything. With cloud computing, those responsibilities shift.
	* IaaS - infrastructure as a service - most responsibility on the consumer
	* PaaS - platform as a service - middle ground between IaaS and SaaS
	* SaaS - software as a service - places most responsibility to the cloud provider
* User is always responsible for:
	* The information and data stored in the cloud
	* Devices that are allowed to connect to your cloud
	* The accounts and identities of the people, services, and devices within your organization.
* The cloud provider is always responsible for:
	* The physical datacenter
	* The physical network
	* The physical hosts
* The service model will determine responsibility for things like
	* Operating systems
	* Network controls
	* Applications
	* Identity and infrastructure
### Define cloud models
#### Private cloud
* Cloud that's used by a single entity.
* May be hosted in a dedicated datacenter offsite, potentially even by a third party that has a datacenter to your company.
#### Public cloud
* Built, controlled and maintained by a third-party cloud provider.
* Anyone that wants to purchase cloud services can access and use resources.
#### Hybrid cloud
* uses both public and private clouds in an inter-connected environment
#### Multi-Cloud
* Use multiple public cloud providers.
#### Azure Arc
* set of technologies that helps manage your cloud environment.
### Describe the consumption-based model
* Two types of expenses to consider for IT infrastructure models.
	* **Capital Expenditure (CapEx)** - one-time, up-front expenditure to purchase or secure tangible resources. New building, repaving the parking lot, building a datacenter, or buying a company vehicle
	* **Operational Expenditure (OpEx)** - spending money on services or products over time. Cloud computing falls under OpEx
* Benefits of consumption-based model:
	* No upfront costs
	* No need to purchase and manage costly infrastructure that users might not use to its fullest potential.
	* The ability to pay for more resources when they're needed.
	* The ability to stop paying for resources that are no longer needed.
### Compare cloud pricing models
Cloud computing is a way to rent compute power and storage from someone else's datacenter. Instead of maintaining CPUs and storage in your datacenter, you rent them for the time that you need them. You're billed only for what you use.

# Describe the benefits of using cloud services
## Learning Objectives
* Describe the benefits of high availability and scalability in the cloud.
* Describe the benefits of reliability and predictability in the cloud.
* Describe the benefits of security and governance in the cloud.
* Describe the benefits of manageability in the cloud.
## Describe the benefits of high availability and scalability in the cloud
### High Availability
* Need to account for service availability guarantees.
* SLA 
	* service level agreement
	* Formal agreement between service provider and customer
	* Azure SLA - represented by percentage (uptime)
	* Also defines downtime and what to do if SLA is not met.
	* 100% uptime is impossible due to required maintenance
	* Usually defined in 99%, 99.99% or 99.95% uptime
### Scalability
* Refers to the ability to adjust resources to meet demand.
* Ensures you aren't overpaying for services.
* **Vertical Scaling** - adding or lowering CPU and RAM specifications to a virtual machine.
* **Horizontal Scaling** - adding or removing virtual machines on demand.

## Describe the benefits of reliability and predictability in the cloud
### Reliability
* Ability of a system to recover from failures and continue to function.