cat > Laboratory-03-Multi-Cloud-Explorer/client-recommendations.md << 'EOF'
# Client Recommendations

## Checkpoint 4 — Cloud Platform Recommendation Challenge

### Client A — Startup Company
**Scenario:** A startup wants to launch a new mobile application. Budget is limited, but they expect rapid growth.

**Recommended Platform: AWS**

AWS is a strong fit because it offers a generous free tier and pay-as-you-go pricing, which keeps costs low while the app is small. It also provides serverless and auto-scaling options that let the startup grow from a handful of users to millions without re-architecting the backend. AWS's large ecosystem of managed services means the small team doesn't need to hire specialized infrastructure engineers early on.

**Services to use:**
- **AWS Lambda** — serverless backend logic without managing servers.
- **Amazon DynamoDB** — scalable NoSQL database for app data.
- **Amazon S3 + CloudFront** — storage and content delivery for app assets/media.

### Client B — University
**Scenario:** Already uses Windows Server, Microsoft 365, and Active Directory. Wants to migrate some services to the cloud.

**Recommended Platform: Microsoft Azure**

Azure is the clear choice because the university's existing identity system (Active Directory) can extend directly into the cloud via Microsoft Entra ID / Azure AD Connect, avoiding a costly identity overhaul. Its native integration with Microsoft 365 and Windows Server workloads means less re-training for IT staff and fewer compatibility issues during migration.

**Services to use:**
- **Azure Virtual Machines** — lift-and-shift existing Windows Server workloads.
- **Microsoft Entra ID** — extend on-prem Active Directory identities to the cloud.
- **Azure Files** — cloud file shares compatible with existing Windows file server setups.

### Client C — AI Research Company
**Scenario:** Develops AI/ML applications requiring high-performance computing.

**Recommended Platform: Google Cloud Platform**

GCP is best suited here because it offers some of the most advanced AI/ML tooling in the industry, backed by Google's own research (TensorFlow, TPUs). Its high-performance compute options, including GPU/TPU-backed instances, are purpose-built for training large models efficiently, and BigQuery makes it easy to process the large datasets AI research typically requires.

**Services to use:**
- **Vertex AI** — end-to-end platform for building, training, and deploying ML models.
- **Compute Engine (with GPUs/TPUs)** — high-performance compute for model training.
- **BigQuery** — serverless data warehouse for large-scale data analysis.

### Client D — Global E-Commerce Company
**Scenario:** Multinational online shopping company requiring highly available infrastructure with automatic scaling.

**Recommended Platform: AWS**

AWS is well suited to global e-commerce because of its extensive global Region/Availability Zone footprint, which allows the company to serve customers with low latency worldwide. Its auto-scaling and load-balancing services are mature and battle-tested at massive scale (Amazon itself runs its retail business on this same infrastructure), and its content delivery network keeps product pages and media fast everywhere.

**Services to use:**
- **Elastic Load Balancing (ELB) + EC2 Auto Scaling** — automatically scale servers to handle traffic spikes (e.g., sales events).
- **Amazon CloudFront** — global CDN for fast content delivery.
- **Amazon Aurora** — highly available, globally distributed relational database.

---

## Checkpoint 6 — Multi-Cloud Decision Matrix

| Business Requirement | Recommended Platform | Justification |
|---|---|---|
| Startup Company | AWS | Low-cost entry (free tier, pay-as-you-go) plus serverless options that scale automatically as the user base grows. |
| Enterprise Organization | AWS or Azure | AWS for broadest general-purpose service catalog; Azure if the enterprise already runs on Microsoft technologies. |
| Microsoft Environment | Microsoft Azure | Native integration with Active Directory, Windows Server, and Microsoft 365 minimizes migration friction. |
| AI / Machine Learning | Google Cloud Platform | Industry-leading AI/ML tooling (Vertex AI, TPUs) and strong data analytics via BigQuery. |
| Kubernetes Deployment | Google Cloud Platform | Google created Kubernetes; GKE is considered the most mature managed Kubernetes offering. |
| Global Web Application | AWS | Largest global Region/AZ footprint plus mature auto-scaling and CDN services for worldwide low-latency access. |
EOF
