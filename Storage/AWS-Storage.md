# 💾 AWS Storage Services (EBS, EFS & S3)

## 📖 Introduction

AWS provides different storage services to meet different application needs. Choosing the right storage service depends on whether you need storage for a **single server**, **multiple servers**, or **internet-scale object storage**.

The three most commonly used AWS storage services are:

- 💽 **Amazon EBS (Elastic Block Store)**
- 📂 **Amazon EFS (Elastic File System)**
- 🪣 **Amazon S3 (Simple Storage Service)**

---

# 💽 Amazon EBS (Elastic Block Store)

## What is Amazon EBS?

Amazon **EBS** is a **block storage** service that provides persistent storage for EC2 instances.

### 💡 Simple Definition

> **Amazon EBS is like a hard disk attached to an EC2 instance.**


## Features

- Persistent block storage
- Attached to EC2 instances
- High performance SSD/HDD storage
- Supports snapshots
- Data remains after stopping the instance

## EBS Volume Types

| Volume Type | Best For |
|-------------|----------|
| gp3 | General Purpose SSD |
| io2 | High Performance Databases |
| st1 | Frequently Accessed HDD |
| sc1 | Archive Storage |

---

# 📂 Amazon EFS (Elastic File System)

## What is Amazon EFS?

Amazon **EFS** is a fully managed **shared file storage** service.

Multiple EC2 instances can access the same file system simultaneously.

### 💡 Simple Definition

> **Amazon EFS is like a shared network drive that multiple EC2 instances can access at the same time.**


## Features

- Shared file storage
- Automatically scales
- Fully managed
- Supports Linux file systems
- Accessible from multiple Availability Zones
 ---

# 🪣 Amazon S3 (Simple Storage Service)

## What is Amazon S3?

Amazon **S3** is an **object storage** service used to store and retrieve unlimited amounts of data.

### 💡 Simple Definition

> **Amazon S3 is like an online cloud storage bucket where you can store files, images, videos, backups, and documents.**



## Features

- Unlimited object storage
- Highly durable (99.999999999%)
- Highly available
- Versioning support
- Lifecycle management
- Static website hosting
- Server-side encryption

# 🪣 S3 Storage Classes

| Storage Class | Use Case |
|---------------|----------|
| S3 Standard | Frequently accessed data |
| S3 Intelligent-Tiering | Automatically moves data between tiers |
| S3 Standard-IA | Infrequently accessed data |
| S3 One Zone-IA | Low-cost storage in one AZ |
| S3 Glacier Instant Retrieval | Archive with quick access |
| S3 Glacier Flexible Retrieval | Long-term backups |
| S3 Glacier Deep Archive | Lowest-cost archival storage |

---

# 🔄 EBS vs EFS vs S3

| Feature | Amazon EBS | Amazon EFS | Amazon S3 |
|----------|------------|------------|-----------|
| Storage Type | Block Storage | File Storage | Object Storage |
| Used With | Single EC2 | Multiple EC2 | Internet Applications |
| Accessible By | One EC2 (per AZ) | Multiple EC2 | Anywhere via Internet/API |
| Automatically Scales | ❌ | ✅ | ✅ |
| Storage Limit | Limited by volume size | Petabytes | Virtually Unlimited |
| Best For | OS, Databases | Shared Files | Images, Videos, Backups |

---


### Quick Revision

- 💽 **EBS** → Block Storage → One EC2
- 📂 **EFS** → File Storage → Multiple EC2
- 🪣 **S3** → Object Storage → Unlimited Files

---
