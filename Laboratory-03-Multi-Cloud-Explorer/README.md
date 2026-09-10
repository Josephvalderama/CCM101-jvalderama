
# Laboratory Activity 3 — Multi-Cloud Explorer

## Mission Overview
This lab evaluates three leading cloud providers — AWS, Microsoft Azure, and Google Cloud Platform (GCP) — for CloudNova Technologies clients, comparing their services and recommending the best fit for different business scenarios.

## Folder Contents
- `aws-research.md` — AWS platform research (Checkpoint 2)
- `azure-research.md` — Azure platform research (Checkpoint 2)
- `gcp-research.md` — GCP platform research (Checkpoint 2)
- `cloud-platform-comparison.md` — Comparison table + equivalent services table (Checkpoints 3 & 5)
- `client-recommendations.md` — Client scenarios + decision matrix (Checkpoints 4 & 6)
- `reflection.md` — Mission reflection (Checkpoint 8)
- `screenshots/` — Evidence screenshots for each checkpoint

## Checkpoint 7 — Linux Investigation (KillerCoda)

### My Findings
Linux Investigation & Cloud Migration Recommendation (Checkpoint 7)
Findings from my KillerCoda environment:

Operating System: Ubuntu 24.04.4 LTS (Noble Numbat)
CPU Information: Intel Xeon E312xx (Sandy Bridge, IBRS update), BIOS model HVAG-9.6.0 PC (Q35 + ICH9, 2009), CPU @ 2.0GHz
Memory: 1.9Gi total, 416Mi used, 823Mi free, 1.5Gi available
Disk Space: 19G total on /, 5.4G used, 13G available (30% used)
If this Linux server were migrated to the cloud, which AWS, Azure, and GCP services could host it?

Given this is a lightweight, single-core Ubuntu server with modest RAM and disk space, it maps closely to each provider's smallest general-purpose virtual machine tier:

AWS: Amazon EC2 (e.g., a t3.micro or t2.micro instance), with Amazon EBS for disk storage
Azure: Azure Virtual Machines (e.g., a B1s burstable-tier VM), using Azure Managed Disks for storage
GCP: Google Compute Engine (e.g., an e2-micro instance), using Persistent Disk for storage
All three providers offer free-tier or low-cost VM options well-suited to a small workload like this one, since its specs comfortably fit within each provider's entry-level instance types.
