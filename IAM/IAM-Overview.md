# 🔐 AWS Identity and Access Management (IAM)
---

# 📚 Table of Contents

- What is IAM?
- Why IAM is Important
- Features of IAM
- IAM Architecture
- Core Components of IAM
- IAM Authentication Methods
- IAM Authorization
- IAM Workflow
- IAM Best Practices
- Advantages of IAM
- Summary

---

# 📖 What is IAM?

**AWS Identity and Access Management (IAM)** is a global AWS service that helps you **securely manage access** to AWS resources.

It allows you to:

- Create users and groups
- Assign permissions
- Control access to AWS services
- Implement security best practices
- Manage authentication and authorization

> **Definition:** IAM is a service that controls **who** can access AWS resources and **what actions** they are allowed to perform.

---

# 🎯 Why IAM is Important

IAM helps organizations:

- Secure AWS resources
- Control user permissions
- Implement the Principle of Least Privilege
- Prevent unauthorized access
- Monitor user activities
- Enable secure access for applications and AWS services

---

# ⭐ Features of IAM

- 🌍 Global AWS Service (Not Region-specific)
- 🔐 Secure authentication
- 📜 Fine-grained access control
- 👥 User and Group management
- 🎭 Role-based access
- 🔑 Temporary security credentials
- 🛡 Multi-Factor Authentication (MFA)
- 📊 Activity monitoring with AWS CloudTrail
- 🔄 Cross-account access
- 🌐 Identity Federation

---

# 🏗 IAM Architecture

```text

                    AWS Account
                        │
                        ▼
                   AWS IAM Service
                        │
        ┌───────────────┬───────────────┬
        │               │               │
   IAM Users      IAM Groups      IAM Roles
        │               │               │
        └───────────────┼───────────────┘
                        │
                  IAM Policies
                        │
                        ▼
             AWS Resources & Services
      (EC2, S3, RDS, Lambda, VPC, CloudWatch)
```

---

# 🧩 Core Components of IAM

| Component | Description |
|-----------|-------------|
| **Root User** | The AWS account owner with full access to all AWS resources. |
| **IAM User** | An identity created for an individual person or system requiring AWS access. |
| **IAM Group** | A collection of IAM Users that share the same permissions. |
| **IAM Role** | A temporary identity that provides permissions to users, applications, or AWS services. |
| **IAM Policy** | A JSON document that defines what actions are allowed or denied. |
| **Permission Boundary** | Defines the maximum permissions that an IAM User or Role can have. |
| **MFA (Multi-Factor Authentication)** | Adds an extra layer of security during authentication. |
| **AWS STS** | AWS Security Token Service issues temporary security credentials. |
| **Identity Federation** | Allows users from external identity providers to access AWS resources. |

---

# 🔑 IAM Authentication Methods

Authentication verifies **who you are**.

IAM supports the following authentication methods:

| Method | Purpose |
|---------|----------|
| Username & Password | AWS Management Console |
| Access Key ID & Secret Access Key | AWS CLI, SDKs, APIs |
| Multi-Factor Authentication (MFA) | Additional security layer |
| Temporary Security Credentials | Access through IAM Roles using AWS STS |
| Identity Federation | Login using external identity providers |

---

# 🔒 IAM Authorization

Authorization determines **what actions an authenticated identity can perform**.

Permissions are controlled using:

- IAM Policies
- IAM Groups
- IAM Roles
- Permission Boundaries
- Resource-based Policies

---

# 🔄 IAM Workflow

```text
User / Application
        │
        ▼
Authentication
(Login / Access Keys / IAM Role)
        │
        ▼
IAM Policy Evaluation
        │
        ▼
Authorization
        │
        ▼
Allow or Deny Request
        │
        ▼
AWS Resource
```

---

# 🚀 Advantages of IAM

- Secure access management
- Fine-grained permissions
- Centralized identity management
- Supports AWS CLI and SDKs
- Temporary credentials using IAM Roles
- Multi-Factor Authentication
- Cross-account access
- Integration with external identity providers
- No additional cost

---


# 📝 Summary

AWS Identity and Access Management (IAM) is the foundation of AWS security. It enables you to securely control access to AWS resources by creating users, groups, roles, and policies. IAM follows the **Principle of Least Privilege**, ensuring that identities receive only the permissions they need. By combining authentication, authorization, MFA, IAM Roles, and AWS STS, IAM helps organizations build secure and scalable cloud environments.

---

# 📌 Key Takeaways

- 🔐 IAM controls **who can access AWS** and **what they can do**.
- 👤 IAM Users are permanent identities for people or systems.
- 👥 IAM Groups simplify permission management.
- 🎭 IAM Roles provide temporary credentials.
- 📜 IAM Policies define permissions.
- 🛡 MFA strengthens account security.
- 🔑 AWS STS provides temporary credentials.
- 🌐 Identity Federation enables external users to access AWS.
- 🚫 Avoid using the Root User for everyday tasks.
- ✅ Follow the Principle of Least Privilege.
