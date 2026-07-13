# 🔐 AWS IAM (Identity and Access Management)


---

# 📚 Table of Contents

1. What is IAM?
2. Root User
3. IAM Users
4. IAM Groups
5. IAM Policies
6. IAM Workflow
7. Summary

---

# 📖 What is IAM?

AWS Identity and Access Management (IAM) is a global AWS service that controls **who can access AWS resources** and **what actions they are allowed to perform**.

IAM provides secure authentication and authorization for users, applications, and AWS services.

---

# 👑 Root User

## What is a Root User?

The **Root User** is the AWS account owner created when you sign up for AWS.

It has **complete and unrestricted access** to all AWS services and resources.

### Components of Root User

| Component | Description |
|-----------|-------------|
| Email Address | Used to sign in to the AWS account |
| Password | Console login password |
| MFA | Adds an additional layer of security |
| Billing Access | Full billing and payment management |
| Full Permissions | Cannot be restricted by IAM policies |

### Best Practices

- Enable MFA
- Never share credentials
- Avoid daily usage
- Do not create Root Access Keys
- Use only for billing and account-level tasks

---

# 👤 IAM Users

## What is an IAM User?

An IAM User is an identity created for an individual person or system that needs access to AWS resources.

Unlike the Root User, an IAM User has only the permissions granted through IAM Policies.

### Components of IAM User

| Component | Description |
|-----------|-------------|
| Username | Unique identity name |
| Console Password | Login to AWS Console |
| Access Key ID | Used for CLI/SDK/API |
| Secret Access Key | Private credential |
| IAM Policies | Defines permissions |
| IAM Groups | Organizes users |
| MFA | Extra security |
| Tags | Resource organization |
| Permission Boundary | Maximum permissions |

---

# 👥 IAM Groups

## What is an IAM Group?

An IAM Group is a collection of IAM Users.

Instead of assigning permissions to each user individually, permissions are assigned to the group.

### Components of IAM Group

| Component | Description |
|-----------|-------------|
| Group Name | Unique group identifier |
| IAM Users | Members of the group |
| Attached Policies | Permissions shared by all users |
| Tags | Organize IAM Groups |

### Example

```text
Developers Group
      │
 ┌────┼─────┐
 │    │     │
Alice Bob Charlie
```

---

# 📜 IAM Policies

## What is an IAM Policy?

An IAM Policy is a JSON document that defines **what actions are allowed or denied** on AWS resources.

Policies can be attached to:

- IAM Users
- IAM Groups
- IAM Roles

### Components of an IAM Policy

| Component | Description |
|-----------|-------------|
| Version | Policy language version |
| Statement | One or more permission statements |
| Effect | Allow or Deny |
| Action | AWS operations (e.g., s3:GetObject) |
| Resource | AWS resources affected |
| Condition | Optional rules for access |

### Example Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "*"
    }
  ]
}
```

---

# 🔄 IAM Workflow

```text
                    AWS Account
                          │
                    Root User
                          │
          Creates IAM Users & Groups
                          │
                 Attach IAM Policies
                          │
                    Authentication
                          │
                    Authorization
                          │
                    AWS Resources
```

---



# 📝 Summary

AWS IAM is the foundation of AWS security. The **Root User** manages the AWS account, **IAM Users** provide secure access for individuals, **IAM Groups** simplify permission management, and **IAM Policies** define what actions identities can perform. Following IAM best practices ensures a secure and scalable AWS environment.

---

# 📌 Key Takeaways

- 👑 Root User has unrestricted access.
- 👤 IAM Users represent individual people or systems.
- 👥 IAM Groups simplify permission management.
- 📜 IAM Policies define permissions.
- 🔒 Enable MFA for stronger security.
- 🚫 Avoid using the Root User for daily tasks.
- ✅ Follow the Principle of Least Privilege.
- 📊 Monitor IAM activity using AWS CloudTrail.
