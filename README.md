# Microsoft Azure Notes

## Notes
- [AZ-900 notes](./notes/az_900_notes.md)

## Resources
- [Microsoft Ignite](https://learn.microsoft.com/en-us/collections/o5met117w6pp01)


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

