# Introduction to Storage Accounts
* Azure Storage offers several types of storage accounts
* Each with **different features** and their **own pricing models**
	* General-purpose v1 (legacy)
	* General-purpose v2
	* BlobStorage
	* BlockBlobStorage
	* File Storage
* **Storage type** and **Account Kind** mean the same thing
* Storage accounts vary with the following features
	* **Supported services** - What can I put in this storage account?
		* Blob, File, Queue, Table, **Disk**, and Data Lake Gen2
	* **Performance Tiers** - How fast my read and writes be?
		* Standard and Premium
	* **Access tiers** - How often do I need quick access to files?
		* Hot, Cool, Archive
	* **Replication** - How many redundant copies should be made and where?
		* LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS
	* **Deployment Model** - Who should deploy the supported services?
		* Resource Manager, Classic
		* In most cases, it is going to be Resource Manager.
# Core Storage Services
* Azure has **5 Core Storage Services**
	* **Azure Blob**
		* A massively scalable **object store** for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2
	* **Azure Files**
		* Managed **file shares** for cloud or on-premises deployments
	* **Azure Queues**
		* A **NoSQL store** for schemaless storage of structured data
	* **Azure Tables**
		* A messaging store for reliable messaging between application components
	* **Azure Disks**
		* **Block-level** storage volumes for Azure VMs
* Azure Blob, Azure Files, Azure Queues and Azure Tables ca be found under **Storage Accounts** while Azure Disks can be found under **Disks**
# Performance Tiers
* There are 2 types of performance tiers for storage accounts: **Standard** and **Premium**
* **IOPS** - stands for Input/Output Operations Per Second. The higher the IOPS the faster a drive can read and write
* **Premium Performance**
	* Stored on Solid State Drives (SSDs)
	* Optimized for low latency
	* Higher throughput
	* Use cases: Interactive workloads, analytics, AI or ML or data transformation
* **Standard Performance**
	* Stored on Hard Disk Drives (HDDs)
	* Varied performance based on access tier (Hot, Cool, Archive)
	* Use cases: Backup and disaster recovery, media content, bulk data processing.
# Access Tiers
* 3 Types of access tiers for **Standard storage**: **Cool, Hot** and **Archive**
* **Hot**
	* Data that's accessed frequently
	* Highest storage cost, lowest access cost
	* Use cases:
		* Data that's in active use or expected to be accessed frequently
		* Data that's staged for processing and eventual migration to the cool access tier
* **Cool**
	* Data that's infrequently accessed and stored for at least 30 days
	* Lower storage cost, higher access cost
	* Use cases:
		* Short-term backup and disaster recovery datasets
		* Older media content not viewed frequently anymore but is expected to be available immediately when accessed
		* Large data sets that need to be stored cost effectively while more data is being gathered for future processing.
* **Archive**
	* Data that's rarely accessed and stored for at least 180 days
	* Lowest storage cost, highest access cost
	* Use cases:
		* Long-term backup, secondary backup, and archival datasets
		* Original (raw) data that must be preserved, even after it has been processed into final usable form.
		* Compliance and archival data that needs to be stored for a time and is hardly ever accessed.
* **Account Level Tiering**
	* Any blob that doesn't have an explicitly assigned tier infers the tier from the Storage Account access tier setting.
* **Blob-Level Tiering**
	* You can upload a blob to the tier of your choice.
	* Changing tiers happens instantly with the exception from moving out of archive
* 