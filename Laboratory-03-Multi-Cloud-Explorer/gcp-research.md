
# GCP Research — Google Cloud Platform

## Brief Overview
Google Cloud Platform (GCP) is Google's public cloud offering, with roots going back to the App Engine preview launch in 2008 and a full public GA around 2011–2013. GCP leverages the same infrastructure that powers Google Search, YouTube, and Gmail, and is especially known for strength in data analytics, AI/ML, and container orchestration (Google created Kubernetes).

## Global Infrastructure
GCP infrastructure is organized into:
- **Regions** — independent geographic areas (e.g., `us-central1`, `asia-southeast1`).
- **Zones** — isolated deployment areas within a Region.
- **Google's private global network** — Google routes traffic over its own fiber backbone rather than the public internet where possible, which can improve performance.

See the current footprint on the [Google Cloud Locations page](https://cloud.google.com/about/locations).

## Cloud Management Console
The **Google Cloud Console** is the web-based management dashboard. Other tools include:
- **gcloud CLI** — command-line interface.
- **Cloud Shell** — free browser-based shell with pre-installed tools.
- **Terraform / Deployment Manager** — infrastructure-as-code options.

*(Insert screenshot: `screenshots/gcp-homepage.png` — GCP homepage or console dashboard)*

## Four (4) Core Services
1. **Compute Engine** — customizable virtual machine instances.
2. **Cloud Storage** — object storage for any amount of unstructured data.
3. **Cloud SQL** — managed relational database service (MySQL, PostgreSQL, SQL Server).
4. **Identity and Access Management (Cloud IAM)** — centralized access control for GCP resources.

## Three (3) Advantages
1. **Leader in data analytics and AI/ML** — BigQuery (serverless data warehouse) and Vertex AI are considered top-tier in the industry.
2. **Kubernetes origin and container expertise** — Google created Kubernetes, and Google Kubernetes Engine (GKE) is widely regarded as the most mature managed Kubernetes offering.
3. **Competitive, simple pricing** — sustained-use discounts and generally straightforward pricing structure.

## Typical Enterprise Use Cases
- Big data analytics and business intelligence (BigQuery).
- AI/ML model development and training (Vertex AI, TensorFlow on GCP).
- Container-based and Kubernetes-native application deployment (GKE).
- Data-heavy startups and research organizations needing high-performance computing.

---
