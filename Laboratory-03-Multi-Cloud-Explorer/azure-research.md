cat > Laboratory-03-Multi-Cloud-Explorer/azure-research.md << 'EOF'
# Azure Research — Microsoft Azure

## Brief Overview
Microsoft Azure is Microsoft's public cloud platform, launched in 2010 (originally as "Windows Azure"). Azure is deeply integrated with Microsoft's enterprise ecosystem — Windows Server, Active Directory, Microsoft 365, and .NET — making it a natural fit for organizations already invested in Microsoft technologies.

## Global Infrastructure
Azure infrastructure is organized into:
- **Regions** — geographic areas containing one or more datacenters (e.g., East US, Southeast Asia).
- **Availability Zones** — physically separate datacenters within a Region for high availability.
- **Region Pairs** — Azure pairs Regions within the same geography for disaster recovery.

Azure claims the largest number of Regions of any cloud provider (verify current count on the [Azure Global Infrastructure page](https://azure.microsoft.com/en-us/explore/global-infrastructure/)).

## Cloud Management Console
The **Azure Portal** is the primary web-based console. Other management tools include:
- **Azure CLI** and **Azure PowerShell** — command-line management.
- **Azure Cloud Shell** — browser-based shell.
- **Azure Resource Manager (ARM) templates / Bicep** — infrastructure-as-code.

*(Insert screenshot: `screenshots/azure-homepage.png` — Azure homepage or portal dashboard)*

## Four (4) Core Services
1. **Azure Virtual Machines** — on-demand scalable compute instances.
2. **Azure Blob Storage** — object storage for unstructured data.
3. **Azure SQL Database** — managed relational database service.
4. **Microsoft Entra ID (formerly Azure Active Directory)** — identity and access management, tightly integrated with on-prem Active Directory.

## Three (3) Advantages
1. **Best-in-class Microsoft integration** — seamless with Windows Server, Active Directory, Microsoft 365, and .NET applications.
2. **Strong hybrid cloud support** — Azure Arc and Azure Stack let organizations extend on-prem infrastructure into the cloud.
3. **Enterprise trust and compliance** — widely adopted by large enterprises and government due to Microsoft's compliance certifications.

## Typical Enterprise Use Cases
- Migrating on-prem Windows Server/Active Directory environments to the cloud (hybrid identity).
- Running enterprise line-of-business apps built on .NET.
- Office 365 / Microsoft 365 integrated workflows.
- Hybrid cloud deployments for organizations not ready to go fully cloud-native.

---
**Sources to cite:** Microsoft Azure official documentation (https://learn.microsoft.com/azure), Azure Global Infrastructure page.
EOF
