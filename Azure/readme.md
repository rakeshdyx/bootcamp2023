### Azure Cloud Basic ###

> #### Cloud Service Type ####
- IaaS
    - **Computing** - Example: Azure VM
    - **Storage** - Example: Azure Storage. Storage can be used as a HHD to a VM, Blob, File, Queue and Table. It also can be used as Data Lake for Bigdata or Databricks
    - **Networking** - Example: VNet and Subnets. In Networking, mostly igress is free, but when it comes to egress we have certion bandwith limit. The extra amount will be charged if limit crossed.
- PaaS
    - **PaaS Computing** - Example: Azure App Service
    - **PaaS Storage** - Example: Managed Storage and Azure SQL DB
    - **PaaS Netwoking** - Example: Azure Front Door, LB, Firewall etc. These are software applications that perform networking tasks.
- SaaS
    - Cloud Apps

> #### Serverless ####
- When we say serverless service that mean we should not bother about the underneeth hardware cost like Memory, CPU. 
- Lets consider in case of Serverless Database, based on the ustilization we can increase or descrise the resource.
- If the DB is in ideal state for a while, then turn the cpu core to zero.
- Other serverless services
    - Functions
    - Container Apps
    - Kubernates
    - SQL Database
    - Cosmos DB

### Core Architecttural Components of Azure ###
>#### Regions ####
- Areas of the world where Azure has a **set of datacenters**(minium 3 in a set)
- Not necessarily "countries" but can be
- Usally each region is connected to another region to make a <i>region pair</i>
- <i>Sovereign Region</i> is a type which is not directly accessible as azure public cloud. To create a subscription some criteria must be fullfilled. It's mostly for US govt. top secrets and china.

>#### Availability Zone ####
- Azure availability zones are physically separate location within each Azure region.
- Each region doesn't comes AZ. When we choose a region we should make sure that the region falls under the AZ or not.
- Likely all Azure services also doesn't support AZ
- There are 3 types of AZ services
    - Zonal Service: Plan and deploym services to two zones to achive resiliancy. i.e VM
    - Zone-Redundant Services: Automatically deployed across zones for you. Dont have to configure it. i.e Azure SQL Database
    - Always Available Services: There are global services and Microsoft takes care of the availability. Also called as "Non-regional services". I.e Azure Portal, Azure AD, Azure Front Door.
    - Note: Some of services gives you choice between zonal and zone-redundant
>#### Resource and Resource Groups ####
- A generic word to represent an Azure service that you have access to, such as a specific VM, Storage Account or a DB.
- It can be created many different ways - Azure Portal, CLI, PowerShell, ARM template, terraform, etc.
- ***Resource Group*** is the logical group of resources. RG associated with a region can be diffierent then a resource it contains.  
- All resources must belong to one and only one RG
- Permission can be assigned at the RG level
- There is no secuirty boundary offered by a RG for communications.

>#### Subscriptions ####
- The billing unit within Azure. Payment method associated with a Subscription.
- User can have access to multiple Subscriptions.
- There are multiple subscription types
    - Free Subscription
    - Pay-As-You-Go
    - Enterprise Application
    - Free Credits - MSDN, Startup plans

>#### Management Groups ####
- Management group allow you to control single or multiple subscriptions with different types.

