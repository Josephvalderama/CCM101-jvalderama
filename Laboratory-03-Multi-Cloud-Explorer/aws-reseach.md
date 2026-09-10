
# AWS Research — Amazon Web Services

## Brief Overview
Amazon Web Services (AWS) is the cloud computing platform launched by Amazon in 2006. It was the first major public cloud provider and remains the largest by market share. AWS offers a very broad catalog of on-demand infrastructure and managed services — compute, storage, databases, networking, machine learning, analytics, and more — billed on a pay-as-you-go basis.

## Global Infrastructure
AWS infrastructure is organized into:
- **Regions** — separate geographic areas (e.g., `us-east-1`, `ap-southeast-1`), each fully isolated for fault tolerance and data residency.
- **Availability Zones (AZs)** — each Region has multiple AZs (isolated data centers with independent power/networking) to support high availability.
- **Edge Locations** — used by Amazon CloudFront (CDN) and Route 53 to cache content and reduce latency close to end users.

AWS currently operates dozens of Regions and 100+ AZs worldwide (verify the current count on the [AWS Global Infrastructure page](https://aws.amazon.com/about-aws/global-infrastructure/) since this expands regularly).

## Cloud Management Console
The **AWS Management Console** is the web-based dashboard for provisioning and managing resources. It also offers:
- **AWS CLI** — command-line interface for scripting.
- **AWS CloudShell** — browser-based shell pre-authenticated to your account.
- **SDKs** — for programmatic access in languages like Python (boto3), Java, Node.js, etc.

*(Insert screenshot: `screenshots/aws-homepage.png` — AWS homepage or console dashboard)*

## Four (4) Core Services
1. **Amazon EC2 (Elastic Compute Cloud)** — resizable virtual machine instances for general-purpose compute.
2. **Amazon S3 (Simple Storage Service)** — object storage for files, backups, static websites, and data lakes.
3. **Amazon RDS (Relational Database Service)** — managed relational databases (MySQL, PostgreSQL, SQL Server, etc.).
4. **AWS IAM (Identity and Access Management)** — fine-grained control over who/what can access AWS resources.

## Three (3) Advantages
1. **Largest service catalog** — 200+ services covering nearly every use case (AI/ML, IoT, quantum, media, etc.).
2. **Market maturity and ecosystem** — largest partner network, documentation, and third-party tooling.
3. **Global reach and scalability** — most extensive Region/AZ footprint, enabling low-latency deployment almost anywhere.

## Typical Enterprise Use Cases
- Hosting scalable web and mobile application backends.
- Big data analytics and data lakes (S3 + Athena + Redshift).
- Disaster recovery and backup for on-premises data centers.
- Machine learning model training and deployment (SageMaker).

---
**Sources to cite:** AWS official documentation (https://docs.aws.amazon.com), AWS Global Infrastructure page.
