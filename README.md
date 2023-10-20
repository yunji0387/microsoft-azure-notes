# Microsoft Azure Notes

## Notes
- [AZ-900 notes](./notes/az_900_notes.md)

## Resources
- [Microsoft Learn](https://learn.microsoft.com/en-us/collections/o5met117w6pp01)


## Virtual Training Notes

### Regions
- **Regions are made up of one or more datacenters in close proximity.**

- **Provide flexibility and scale to reduce customer latency.**

- **Preserve data residency with a comprehensive compliance offering.**

---

### Availability zones

- **Provide protection against downtime due to datacenter failure**: Availability zones are designed to protect your applications and data from datacenter failures.
  
- **Physically separate datacenters within the same region**: This ensures a high level of resilience and redundancy within a geographical area.

- **Each datacenter is equipped with independent power, cooling, and networking**: This ensures that if one datacenter faces any issues, the other datacenters can still function independently.

- **Connected through private fiber-optic networks**: This ensures fast and secure communication between datacenters.

---

### Region Pairs

- ** Disaster recovery: Your resources will automatically replicated in the secondary region pair **
- **At least 300 miles of separation between region pairs.**
- **Automatic replication for some services.**
- **Prioritized region recovery in the event of outage.**
- **Updates are rollout sequentially to minimize downtime.**

[Web Link](https://aka.ms/PairedRegions)

---

### Azure Sovereign Regions (US Government services)

Meets the security and compliance needs of US federal agencies, state and local governments, and their solution providers.

#### Azure Government:
- **Separate instance of Azure**
- **Physically isolated from non-US government deployments**
- **Accessible only to screened, authorized personnel**

---

### Azure Sovereign Regions (Azure China)

Microsoft is China’s first foreign public cloud service provider, in compliance with government regulations.

#### Azure China features:
- **Physically separated instance of Azure cloud services operated by 21Vianet**
- **All data stays within China to ensure compliance**

---

### Azure Resources

Azure **resources** are components like storage, virtual machines, and networks that are available to build cloud solutions.

- **Virtual Machines**
- **Storage Accounts**
- **Virtual Networks**
- **App Services**
- **SQL Databases**
- **Functions**

---

### Resource groups

A **resource group** is a container to manage and aggregate resources in a single unit.

- Resources can exist in only one resource group.
- Resources can exist in different regions.
- Resources can be moved to different resource groups.
- Applications can utilize multiple resource groups.
- **Important:**
  - once you delete a resource group, you also delete the resources in the resource group
**Example:**

Resource groups (web + DB, VM, Storage) in one group:
- Web and DB resource group
- Virtual machine resource group
- Storage resource group

_OR_

Each resource in separate groups:
- Web resource group
- DB resource group
- VM resource group
- Storage resource group

---

### Azure Subscriptions

An Azure subscription provides you with authenticated and authorized access to Azure accounts.

- **Billing boundary**: Generate separate billing reports and invoices for each subscription.
- **Access control boundary**: Manage and control access to the resources that users can provision with specific subscriptions.

#### Subscription Types:

- **Dev Subscription**
- **Test Subscription**
- **Production Subscription**

**Note:** This markdown does not represent the visual diagram of the Azure Account and its associated subscriptions, billing accounts, and profiles. It is advised to refer to the actual diagram for a visual representation.

---

### Management Groups

- Management groups can include multiple Azure subscriptions.
- Subscriptions inherit conditions applied to the management group.
- 10,000 management groups can be supported in a single directory.
- A management group tree can support up to six levels of depth.

**Note:** This markdown does not represent the visual hierarchy and relationships shown in the diagram. For a complete understanding, refer to the provided diagram.

---

### Azure Compute Services
Azure **compute** is an on-demand computing service that provides computing resources such as disks, processors, memory, networking, and operating systems.

- **Virtual Machines**
- **App Services**
- **Container Instances**
- **Azure Kubernetes Services (AKS)**
- **Azure Virtual Desktop**

**Note:** The `path_to_icon` placeholders are meant to be replaced with actual paths or URLs to the respective icons if you wish to represent them in markdown.

---

### Azure virtual machines

Azure **Virtual Machines (VM)** are software emulations of physical computers.

- Includes virtual processor, memory, storage, and networking.
- IaaS offering that provides total control and customization.

**Note:** The `path_to_vm_icon_large` placeholder is meant to be replaced with the actual path or URL to the Azure VM icon.

---

### VM scale sets

Scale sets provide a load-balanced opportunity to automatically scale resources.

- Scale out when resource needs increase.
- Scale in when resource needs are lower.

**Note:** Replace `path_to_scale_sets_icon` with the actual path or URL to the VM Scale Sets icon for it to be displayed.

---

### VM availability sets

VM availability sets help in ensuring that your application remains available during network failures, local disk hardware failures, and any unplanned maintenance events.

#### Fault Domain (FD)

A Fault Domain represents a physical unit in a data center, like a server rack. It ensures VMs aren't all on the same hardware, protecting against localized hardware failures.

#### Update Domain (UD)

An Update Domain is a logical grouping ensuring VMs aren't updated simultaneously during maintenance. This prevents all VMs from rebooting at the same time, ensuring service availability.

---

### Azure Virtual Desktop

**Azure Virtual Desktop** is a desktop and app virtualization that runs in the cloud.

1. **Create a full desktop virtualization environment** without having to run additional gateway servers.
2. **Reduce risk** of resource being left behind.
3. **True multi-session deployments**.

---

### Azure Container Services

**Azure Containers** are a light-weight, virtualized environment that does not require operating system management, and can respond to changes on demand.

#### Azure Container Instances
A PaaS offering that runs a container in Azure without the need to manage a virtual machine or additional services.

#### Azure Kubernetes Service
An orchestration service for containers with distributed architectures and large volumes of containers.

---

### Azure Functions

- Event-based code running your service and not the underlying infrastructure.
- **Serverless Computing**: Azure Functions are part of the serverless computing paradigm. In serverless computing, the code is event-driven.
- **Event-Driven Architecture**: This allows for code to run in response to specific events, focusing on your service without managing the underlying infrastructure.

---

### Azure App Services

Azure App Services is a fully managed platform to build, deploy, and scale web apps and APIs quickly. It provides services like HTTP and REST API.

- **Supported Platforms**: Works with .NET, .NET Core, Node.js, Java, Python, or PHP.
- **Features**: PaaS offering with enterprise-grade performance, security, and compliance requirements.

---

## Virtual Networking

### Azure networking services

**Azure Virtual Network (VNet)** enables Azure resources to communicate with each other, the internet, and on-premises networks.
- Public endpoints, accessible from anywhere on the internet
- Private endpoints, accessible only from within your network
- Virtual subnets, segment your network to suit your needs
- Network peering, connect your private networks directly together

**RDP ??????**

---

### Azure Virtual Private Network Gateway

**Virtual Private Network Gateway (VPN)** is used to send encrypted traffic between an Azure virtual network and an on-premises location over the public internet.

---

### Azure ExpressRoute

**Azure ExpressRoute** provides a direct extension of on-premises networks into Azure. This connection is not only facilitated by a trusted connectivity provider but also offers the following advantages:
- **Enhanced Security**: Offers a more secure connection compared to traditional VPNs.
- **Cost Implications**: While it's a premium service and can be more expensive, the benefits in terms of performance and security often justify the investment.

---

### Azure DNS

- **Reliability and performance**: Leveraging a global network of DNS name servers using Anycast networking.
- **Azure DNS security**: Based on Azure resource manager, enabling role-based access control and monitoring and logging.
- **Ease of use**: For managing your Azure and external resources with a single DNS service.
- **Customizable virtual networks**: Allow you to use private, fully customized domain names in your private virtual networks.
- **Alias records**: Supports alias record sets to point directly to an Azure resource.

---

## Azure Storage

### Azure Storage Accounts Overview

Azure Storage Accounts offer various services and are equipped with different redundancy options.

## Introduction
- A storage account provides a **unique namespace** for Azure Storage data.
- Accessible globally over HTTP or HTTPS.
- Ensures **security**, **high availability**, **durability**, and **scalability**.

## Redundancy Options
- **Locally redundant storage (LRS)**: Basic redundancy option.
- **Geo-redundant storage (GRS)**: Enhanced geo-redundancy.
- **Read-access geo-redundant storage (RA-GRS)**: GRS with read access.
- **Zone-redundant storage (ZRS)**: Redundancy within availability zones.
- **Geo-zone-redundant storage (GZRS)**: Combination of geo-redundancy and ZRS.
- **Read-access geo-zone-redundant storage (RA-GZRS)**: GZRS with read access.

## Types of Storage Accounts

| **Type**              | **Supported Services**                              | **Redundancy Options**           | **Usage**                                                       |
|-----------------------|-----------------------------------------------------|----------------------------------|-----------------------------------------------------------------|
| Standard general-purpose v2 | Blob Storage, Data Lake Storage, Queue Storage, Azure Files | LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS | Ideal for blobs, files shares, queues, tables. |
| Premium block blobs   | Blob Storage, Data Lake Storage                    | LRS, ZRS                         | Suited for high transaction rates or small objects.              |
| Premium file shares   | Azure Files                                        | LRS, ZRS                         | For high-performance scale applications.                         |
| Premium page blobs    | Page blobs only                                    | LRS                             | Exclusive for page blobs.                                        |

## Storage Account Naming Rules
- Name length: **3 to 24 characters**.
- Allowed characters: **Numbers** and **lowercase letters** only.
- Names must be **unique** within Azure.

## Endpoints for Azure Storage Services

- **Blob Storage**: `https://<storage-account-name>.blob.core.windows.net`
- **Data Lake Storage Gen2**: `https://<storage-account-name>.dfs.core.windows.net`
- **Azure Files**: `https://<storage-account-name>.file.core.windows.net`
- **Queue Storage**: `https://<storage-account-name>.queue.core.windows.net`
- **Table Storage**: `https://<storage-account-name>.table.core.windows.net`

---

### Azure Storage Redundancy Overview

Azure Storage ensures data protection by storing multiple copies. This protection safeguards data against events like hardware failures, outages, and natural disasters. The redundancy choice relies on factors like replication methods, regional disasters protection, and data access in case the primary region is down.

## Redundancy in the Primary Region
Azure always replicates data thrice in the primary region. The two main options are:

### Locally Redundant Storage (LRS)
- Replicates data three times within one data center in the primary region.
- Durability: 99.999999999% annually.
- Affordable but riskier due to vulnerability to large-scale disasters.

### Zone-Redundant Storage (ZRS)
- Replicates data across three Azure availability zones.
- Durability: 99.9999999999% annually.
- Maintains data accessibility even if a zone is down.

## Redundancy in a Secondary Region
For high durability, data can be replicated to a secondary region distant from the primary. Available options are:

### Geo-Redundant Storage (GRS)
- Uses LRS in primary and asynchronously replicates to LRS in a secondary region.
- Durability: 99.99999999999999% annually.

### Geo-Zone-Redundant Storage (GZRS)
- Combines ZRS in primary and LRS in secondary.
- Durability: 99.99999999999999% annually.

### Data Access in Secondary Region
- GRS and GZRS replicate data to another region for regional outages protection.
- Data in secondary is readable only during a failover unless read-access is enabled.
- Options for read access: Read-Access Geo-Redundant Storage (RA-GRS) and Read-Access Geo-Zone-Redundant Storage (RA-GZRS).

> **Note**: Data in the secondary region might be outdated due to Recovery Point Objective (RPO).

---

### Azure Storage Services

## Overview

Azure Storage provides various data services optimized for durability, scalability, and accessibility.

## Data Services

### **1. Azure Blobs**
- **Definition**: Azure Blob storage is an object storage solution for the cloud. It can store massive amounts of unstructured data.
- **Usage Scenarios**:
  - Serving images/documents to a browser.
  - Storing files for distributed access.
  - Streaming video and audio.
  - Backup, restore, disaster recovery, and archiving.
  - Storing data for analysis.
- **Accessing**: Blobs can be accessed globally via HTTP/HTTPS using URLs, the Azure Storage REST API, Azure PowerShell, Azure CLI, or Azure Storage client libraries.
- **Storage Tiers**:
  - **Hot**: Frequent access (e.g., website images).
  - **Cool**: Infrequent access, stored for 30+ days (e.g., monthly invoices).
  - **Cold**: Rare access, stored for 90+ days.
  - **Archive**: Rarely accessed, stored for 180+ days (e.g., long-term backups).

### **2. Azure Files**
- **Definition**: Azure File storage offers fully managed file shares accessible via SMB or NFS protocols.
- **Key Benefits**:
  - **Shared Access**: Supports SMB and NFS; replace on-premises file shares seamlessly.
  - **Fully Managed**: No need for hardware or OS management.
  - **Scripting & Tooling**: Managed using PowerShell, Azure CLI, Azure portal, and Azure Storage Explorer.
  - **Resiliency**: Built for high availability.
  - **Familiar Programmability**: Access data via file system I/O APIs, Azure Storage Client Libraries, or the Azure Storage REST API.

### **3. Azure Queues**
- Reliable messaging store.
- Can store millions of messages, each up to 64 KB.
- Useful for processing work asynchronously.

### **4. Azure Disks**
- Block-level storage volumes for Azure VMs.
- Virtualized for greater resiliency and availability.

### **5. Azure Tables**
- NoSQL store for structured, non-relational data.
- Accepts authenticated calls from both inside and outside Azure.

## Benefits of Azure Storage

- **Durable & Highly Available**: Redundant storage options.
- **Secure**: Data encryption and controlled access.
- **Scalable**: Handles massive data requirements.
- **Managed**: Azure oversees hardware maintenance and critical issues.
- **Accessible**: Globally available over HTTP/HTTPS with various client libraries.

---

### Azure Data Migration Options

## Azure Migrate

Azure Migrate assists in transitioning on-premises environments to Azure.

- **Unified migration platform**: A single portal for initiating, executing, and monitoring migration to Azure.
- **Range of tools**: It provides multiple tools for assessment and migration including Azure Migrate: Discovery, assessment, server migration, and more. It also integrates with other Azure services, tools, and independent software vendor (ISV) offerings.
- **Integrated tools**: Azure Migrate offers various tools such as:
    - **Azure Migrate: Discovery and assessment**: Assesses servers on VMware, Hyper-V, and physical servers for Azure migration.
    - **Azure Migrate: Server Migration**: Migrates VMware VMs, Hyper-V VMs, physical servers, other virtualized servers, and public cloud VMs to Azure.
    - **Data Migration Assistant**: Assesses SQL Servers for migration readiness.
    - **Azure Database Migration Service**: Migrates databases to Azure.
    - **Azure App Service migration assistant**: Migrates .NET and PHP web apps to Azure.

## Azure Data Box

Azure Data Box is a physical migration service ideal for transferring large amounts of data.

- **How it works**: Microsoft ships a Data Box storage device to you. You transfer your data to this device, and then ship it back. Microsoft then uploads your data to Azure.
- **Use cases**: Suitable for data sizes larger than 40 TBs, especially in scenarios with limited network connectivity. This can be used for:
    - **One-time migration**: Move a significant amount of on-premises data to Azure.
    - **Periodic uploads**: Transfer large data to Azure at regular intervals.
    - **Initial bulk transfer**: Do an initial bulk transfer with Data Box followed by incremental transfers over the network.
- **Data export scenarios**: Data Box can also be used to export data from Azure for purposes like disaster recovery, security requirements, or migrating data back to on-premises.

_Note: Once the data is uploaded to Azure, the disks on the device are wiped clean following NIST 800-88r1 standards._

---

### Azure File Movement Options

Azure offers several tools to handle individual files or smaller file groups in addition to large scale migrations. Here's a summary:

## AzCopy

- **Description**: A command-line utility for copying blobs or files to/from your Azure storage account.
- **Features**: Upload, download, copy between storage accounts, and synchronization (one-direction only).

> **Note**: AzCopy doesn't support bi-directional synchronization based on timestamps or other metadata.

## Azure Storage Explorer

- **Description**: A standalone application to manage files and blobs in Azure Storage. Operates on Windows, macOS, and Linux.
- **Backend**: Uses AzCopy for all file and blob operations.
- **Features**: Upload, download, and move files between Azure storage accounts.

## Azure File Sync

- **Description**: Syncs(bidirectional synchronization) local Windows server(on-premises) file shares with Azure(cloud) Files, effectively making your Windows server akin to a mini content delivery network.
- **Features**:
    - Supports multiple protocols like SMB, NFS, and FTPS for local data access.
    - Allows numerous global caches.
    - Easily replaces a local server in the same datacenter by installing Azure File Sync on a new server.
    - Enables cloud tiering to balance frequently accessed files locally with infrequently accessed ones in the cloud.

---

## Azure Identity, Access, and Security

### Azure Directory Services

## **Microsoft Entra ID**
- Cloud-based identity and access management service from Microsoft.
- Works alongside on-premises Active Directory.
- Provides global accessibility with user-managed identity accounts.

**Key Features**:
- **Authentication**: Includes identity verification, self-service password reset, multifactor authentication, and more.
- **Single Sign-on (SSO)**: One username and password for multiple applications.
- **Application Management**: For cloud and on-premises apps.
- **Device Management**: Register and manage devices, integrating with tools like Microsoft Intune.

**Who uses it?**
- IT Administrators
- App Developers
- End Users
- Microsoft 365, Office 365, Azure, and Dynamics CRM Online subscribers.

## **Connecting On-Premises AD with Microsoft Entra ID**
- Maintain consistent identity experience between cloud and on-premises.
- **Microsoft Entra Connect**: Synchronizes user identities between on-premises AD and Microsoft Entra ID.

## **Microsoft Entra Domain Services**
- Provides managed domain services like domain join, group policy, LDAP, and authentication.
- Ideal for legacy applications in the cloud that need domain services.
- Integrates with existing Microsoft Entra tenant.

**How it works**:
- Creates a unique namespace (domain name) with two Windows Server domain controllers deployed in an Azure region.
- Azure manages, configures, and updates these domain controllers.
- One-way synchronization from Microsoft Entra ID to Microsoft Entra Domain Services.

> **Note**: Resources can be created in the managed domain but aren't synced back to Microsoft Entra ID.

---

### Azure Authentication Methods

**Authentication** is like presenting ID when traveling: proving one's identity.

## Azure Supported Authentication Methods:
- **Standard Passwords**
- **Single Sign-On (SSO)**
- **Multifactor Authentication (MFA)**
- **Passwordless**

> Security vs. Convenience: 
> - Passwordless: High Security & High Convenience.
> - Passwords + 2FA: High Security & Low Convenience.

## Single Sign-On (SSO)

Allows a user to sign in once and access multiple resources.
- Reduces passwords to remember.
- Simplifies security model.
- Less strain on IT management.

> **Note**: SSO's security is based on the security of the initial authenticator.

## Multifactor Authentication (MFA)

Requires two or more elements to authenticate. Categories:
1. **Something the user knows** - e.g., a challenge question.
2. **Something the user has** - e.g., a code to a mobile phone.
3. **Something the user is** - e.g., fingerprint or face scan.

> MFA limits the impact of credential exposure and provides added security benefits.

## Microsoft Entra Multifactor Authentication

A service offering multifactor authentication with options like phone call or mobile app notifications.

## Passwordless Authentication

Removes password and replaces it with:
1. Something you have (e.g., registered device).
2. Plus something you know or are (e.g., PIN or fingerprint).

**Azure Passwordless Options**:
- **Windows Hello for Business**: Tied to user's PC, supports SSO.
- **Microsoft Authenticator App**: Turns phones into passwordless credentials.
- **FIDO2 Security Keys**: Standards-based passwordless method.

> FIDO2 keys can be USB, Bluetooth, or NFC. They enhance security by eliminating password exposure.

---

### Azure External Identities

External identity refers to any entity outside an organization. With Microsoft Entra External ID, securely collaborate with users outside your organization or manage customer identity experiences in consumer-facing apps.

- External users can bring their own identities, e.g., Google, Facebook, or corporate credentials.
- Their identity provider manages their identity; you control access with Microsoft Entra ID or Azure AD B2C.

## Key Capabilities

### 1. **Business to Business (B2B) Collaboration**
   - Let external users sign-in with their preferred identity to your applications.
   - External users appear as guest users in your directory.

### 2. **B2B Direct Connect**
   - Establish a two-way trust with another Microsoft Entra organization.
   - Enables external users to access your resources within their Teams. 
   - Users aren't in your directory but visible in Teams shared channel.

### 3. **Microsoft Entra Business to Customer (B2C)**
   - Publish apps to consumers using Azure AD B2C for identity and access management.

Use a combination of these capabilities based on your collaboration needs.

With Microsoft Entra ID's B2B feature, you can:
- Enable collaboration across organizations.
- Invite guest users from other tenants.
- Ensure guest users have appropriate access through access reviews.

---

##

---

### Cost Management in Azure

???

---

## Azure governance and compliance, Azure resource management, and Azure monitoring services

### Azure Blueprints

**Azure Blueprints** makes it possible for development teams to rapidly build and stand up new environments. Development teams can quickly build trust through organizational compliance with a set of built-in components (such as networking) in order to speed up development and delivery.

- **Role Assignments**
- **Policy Assignments**
- **Azure Resource Manager Templates**
- **Resource Groups**

---

### Azure Policy

**Azure Policy** assists in enforcing organizational standards and evaluating compliance at scale. It ensures governance, resource consistency, security, cost management, and alignment with regulatory compliance.

- **Evaluates Azure Resources**: Identifies resources that might not be in line with your policies.
- **Policy and Initiative Definitions**: Offers predefined policies for various categories such as Storage, Networking, Compute, Security Center, and Monitoring.
- **Azure DevOps Integration**: Seamlessly integrates with Azure DevOps, supporting continuous integration and ensuring compliance both pre-deployment and post-deployment.

---

### Resource locks

- **Protect your Azure resources** from accidental deletion or modification.
- **Manage locks** at subscription, resource group, or individual resource levels within Azure Portal.

### Lock Types

|           | Read | Update | Delete |
|-----------|------|--------|--------|
| Delete    | Yes  | Yes    | No     |
| ReadOnly  | Yes  | No     | No     |

---

### Service Trust Portal

- A Microsoft platform focusing on **trust**, **security**, and **compliance**.
- Features:
  - Access to **Trust Documents**.
  - Details on specific **Industries & Regions**.
  - Exploration of the **Trust Center**.
  - Various **Resources** for users.
  - Personal content management through **My Library**.
  - Tools like **Whitepaper**, **Audit Report**, and **Compliance Manager** to ensure compliance standards.

---

## Azure resource management

### Tools for interacting with Azure

- **Azure portal**: A web-based unified console to manage all Azure services.
- **Azure PowerShell**: A module offering cmdlets to manage Azure resources directly from the PowerShell command line.
- **Azure Cloud Shell**: An interactive, browser-accessible shell for managing Azure resources.
- **Command-Line Interface (CLI)**: A command-line tool to manage Azure resources using commands.

---

### Azure Resource Manager Overview

**Azure Resource Manager (ARM)** offers a unified management layer, allowing users to:

- **Create, update, and delete** resources in their Azure subscription.
  
### Tools and Services:
- **Azure portal**, **Azure PowerShell**, and **Azure CLI**: Direct interfaces for management tasks.
- **SDKs**: For programmatic access.
- **Rest clients**: Another mode for developers to interact with ARM.

### Core Components:
- **Authentication**: Ensures secure access to resources.
- **Resources**: Includes **Data Store**, **Web App**, **Virtual Machine**, **Service Management**, and other services.

---

### Azure Resource Manager (ARM) Templates

**ARM Templates** are defined as **JavaScript Object Notation (JSON)** files. They allow users to:

- **Deploy Azure infrastructure** without the need to write individual programming commands.

### Key Features of ARM Templates:
- **Declarative syntax**: Define "what" you want rather than "how".
- **Repeatable results**: Ensure consistency across deployments.
- **Orchestration**: Coordinate and manage the deployment of multiple resources.
- **Modular files**: Break down templates for better organization and reuse.
- **Built-in validation**: Check templates for errors before deployment.
- **Exportable code**: Easily share and distribute your templates.

### Visual Representation:
- **Resource Manager Template**: Represents the main ARM template file. 
- **Non-template Infrastructure as code**: Alternative methods to deploy resources using imperative PUT calls.

Connected with **Azure Resource Manager** and **Resource Providers** for efficient deployment.

---

### Azure Arc Overview

**Azure Arc** allows users to extend Azure services and management to any infrastructure, including:
- **On-premises**
- **Multicloud**
- **Edge locations**

### Main Components:

1. **Customers**:
   - Engage with Azure through various **tools and experiences**.
   - Examples include the **Azure Portal**, **PowerShell**, and **Azure CLI**.

2. **Azure**:
   - At the heart of Azure Arc, serving as the main platform.
   - Uses **Azure Resource Manager** for management with features like:
     - **Single-pane-of-glass for management**: Centralized view for resources.
     - **Role-based access control**: Define who can do what.
     - **Cloud-native practices**: Implement standard practices for cloud deployments.
     - **Security and Compliance**: Ensures that resources adhere to necessary compliance measures.
     - **Resources in Azure**: Direct resources that reside in Azure.

3. **Azure Arc**:
   - **Extend Azure management** to other environments, such as on-premises, multicloud, and edge.
   - Resources in these locations can be managed similarly to how resources are managed in Azure.
   - **Local management tools** available for more specific or granular management at these locations.

With Azure Arc, organizations can have a unified approach to manage resources irrespective of where they are located, offering flexibility and scalability.

---

## Azure Monitoring Services

### Azure Advisor

**Azure Advisor** analyzes deployed Azure resources and provides recommendations based on best practices to optimize Azure deployments.

## Key Areas of Recommendation:

- **Reliability**
- **Security**
- **Performance**
- **Cost**
- **Operational Excellence**

### Recommendations Overview:

#### 1. **Reliability**:
   - Recommendations: `4`
   - Impacted Resources: `122`

#### 2. **Security**:
   - Recommendations: `31`
   - Impacted Resources: `218`

#### 3. **Performance**:
   - Status: You are following all of our performance recommendations.

Azure Advisor serves as a guide to ensure your Azure resources are optimized and aligned with best practices.

---

### Azure Service Health

Azure Service Health is a collection of services that keep you informed of general Azure status, service status that may impact you, and specific resource status that is impacting you.

## Azure Status
Global view of the health of all Azure services across all Azure regions.

## Service Health
Focused view on only the services and regions that you're using. If a service is experiencing a problem in a region you're not using, it won't show up here.

## Resource Health
Tailored view of your actual Azure resources. It provides information about the health of your individual cloud resources.

---

### Azure Monitor

**Azure Monitor** maximizes the availability and performance of applications and services by collecting, analyzing, and acting on telemetry from cloud and on-premises environments.

- **Application Insights**
- **Log Analytics**
- **Smart Alerts**
- **Automation Actions**
- **Customized Dashboards**

---
