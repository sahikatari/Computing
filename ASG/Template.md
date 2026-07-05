
# 📄 Launch Templates

## What is a Launch Template?

A **Launch Template** is a reusable blueprint that defines how EC2 instances should be launched.

Whenever Auto Scaling needs to create a new EC2 instance, it uses the Launch Template.

### 💡 Simple Definition

> **A Launch Template contains all the settings required to launch an EC2 instance.**

---

## Launch Template Includes

| Configuration | Description |
|---------------|-------------|
| 🖥️ AMI | Operating System Image |
| 💻 Instance Type | e.g., t2.micro, t3.medium |
| 🔑 Key Pair | SSH Access |
| 🛡️ Security Group | Firewall Rules |
| 👤 IAM Role | AWS Permissions |
| 💾 Storage (EBS) | Root and additional volumes |
| 📜 User Data | Startup script |
| 🌐 Network | VPC and Subnet configuration |

---

## Why Use Launch Templates?

- ✅ Reusable configuration
- ✅ Consistent EC2 deployment
- ✅ Supports versioning
- ✅ Faster instance creation
- ✅ Required for modern Auto Scaling features

---
