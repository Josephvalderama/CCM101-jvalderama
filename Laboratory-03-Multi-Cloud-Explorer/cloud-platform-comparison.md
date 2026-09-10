cat > Laboratory-03-Multi-Cloud-Explorer/cloud-platform-comparison.md << 'EOF'
# Cloud Platform Comparison

## Checkpoint 3 — Comparison Table

| Category | AWS | Microsoft Azure | Google Cloud Platform |
|---|---|---|---|
| Launch Year | 2006 | 2010 | 2008 (App Engine preview) / GA ~2011–2013 |
| Compute Service | Amazon EC2 | Azure Virtual Machines | Compute Engine |
| Storage Service | Amazon S3 | Azure Blob Storage | Cloud Storage |
| Networking Service | Amazon VPC | Azure Virtual Network (VNet) | Virtual Private Cloud (VPC) |
| Identity Service | AWS IAM | Microsoft Entra ID (Azure AD) | Cloud IAM |
| Primary Strength | Broadest service catalog, market maturity | Enterprise/Microsoft ecosystem integration | Data analytics, AI/ML, Kubernetes |
| Ideal Organizations | Startups to large enterprises needing maximum flexibility | Enterprises already using Windows Server/Microsoft 365/AD | Data-driven companies, AI/ML teams, Kubernetes-native workloads |

### Reflection Questions

**1. Which cloud provider offers the broadest range of services?**
AWS offers the broadest range of services, with over 200 offerings spanning compute, storage, databases, IoT, media, and more. Its first-mover advantage and long track record mean it has built out niche services that competitors haven't fully matched yet.

**2. Which provider best integrates with Microsoft technologies?**
Microsoft Azure best integrates with Microsoft technologies, since it was built by the same company behind Windows Server, Active Directory, and Microsoft 365. Organizations already running Microsoft infrastructure get near-seamless hybrid identity and management through Entra ID and Azure Arc.

**3. Which provider is strongest in Artificial Intelligence and Kubernetes?**
Google Cloud Platform is generally considered strongest here, since Google originally created Kubernetes and Google Kubernetes Engine (GKE) is widely viewed as the most mature managed Kubernetes service. GCP's Vertex AI and BigQuery ML also make it a top choice for AI/ML and data science workloads.

**4. Which cloud platform would you personally choose and why?**
I would cboose  broad general-purpose flexibility (AWS)

---

## Checkpoint 5 — Equivalent Services Reference Table

| Service Category | AWS | Azure | GCP |
|---|---|---|---|
| Virtual Machine | Amazon EC2 | Azure Virtual Machines | Compute Engine |
| Object Storage | Amazon S3 | Azure Blob Storage | Cloud Storage |
| Identity Management | AWS IAM | Microsoft Entra ID | Cloud IAM |
| SQL Database | Amazon RDS | Azure SQL Database | Cloud SQL |
| Kubernetes | Amazon EKS (Elastic Kubernetes Service) | Azure Kubernetes Service (AKS) | Google Kubernetes Engine (GKE) |
EOF

