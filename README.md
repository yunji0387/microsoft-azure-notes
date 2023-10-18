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

