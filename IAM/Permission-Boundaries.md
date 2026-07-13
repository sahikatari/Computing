# 🔒 IAM Permission Boundaries in AWS

---

# 📚 Table of Contents

- What is a Permission Boundary?
- Why Use Permission Boundaries?
- How Permission Boundaries Work
- Components
- Permission Boundary vs IAM Policy
- Use Cases
- Advantages
- Limitations
- Best Practices
- Summary

---

# 📖 What is a Permission Boundary?

An **IAM Permission Boundary** is an advanced AWS IAM feature that defines the **maximum permissions** an IAM User or IAM Role can receive.

A Permission Boundary **does not grant permissions**. Instead, it limits the permissions granted by IAM policies.

> **Effective Permissions = IAM Policy ∩ Permission Boundary**

This means a user or role can perform only the actions allowed by **both** the IAM Policy and the Permission Boundary.

---

# 🎯 Why Use Permission Boundaries?

Permission Boundaries help you:

- ✅ Prevent privilege escalation
- ✅ Delegate IAM administration safely
- ✅ Restrict developers to approved services
- ✅ Enforce security standards
- ✅ Apply the Principle of Least Privilege

---

# ⚙️ How Permission Boundaries Work

Suppose an IAM User has the following IAM Policy:

```text
Allow:
- EC2 Full Access
- S3 Full Access
```

The user also has a Permission Boundary:

```text
Allow:
- EC2 Only
```

### Effective Permissions

```text
✅ EC2 Access
❌ S3 Access
```

Although the IAM Policy allows S3, the Permission Boundary blocks it because S3 is not included in the boundary.

---

# 🧩 Components

| Component | Description |
|-----------|-------------|
| Permission Boundary | Managed IAM Policy that limits maximum permissions |
| IAM User | Identity that receives the Permission Boundary |
| IAM Role | Role that receives the Permission Boundary |
| IAM Policy | Grants permissions |
| Effective Permissions | Permissions allowed by both the IAM Policy and the Permission Boundary |

---

# ⚖️ Permission Boundary vs IAM Policy

| Feature | IAM Policy | Permission Boundary |
|----------|------------|---------------------|
| Grants permissions | ✅ Yes | ❌ No |
| Limits permissions | ❌ No | ✅ Yes |
| Maximum permissions | ❌ No | ✅ Yes |
| Attached to Users | ✅ Yes | ✅ Yes |
| Attached to Roles | ✅ Yes | ✅ Yes |
| Attached to Groups | ✅ Yes | ❌ No |
| Used for Delegation | Limited | Excellent |

---

# 📝 Example

### IAM Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "ec2:*",
        "s3:*"
      ],
      "Resource": "*"
    }
  ]
}
```

### Permission Boundary

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:*",
      "Resource": "*"
    }
  ]
}
```

### Result

| Service | Access |
|----------|--------|
| EC2 | ✅ Allowed |
| S3 | ❌ Denied |

---

# 💼 Real-World Use Cases

### 👨‍💻 Developer Team

Developers can launch EC2 instances but cannot modify IAM resources.

---

### 🏢 Enterprise Organizations

Allow team administrators to create IAM roles while ensuring those roles cannot exceed company-approved permissions.

---

### 🔐 Secure Role Creation

Developers can create new IAM Roles, but every role must remain within the predefined Permission Boundary.

---

# ✅ Advantages

- Prevents privilege escalation
- Supports delegated administration
- Enforces least privilege
- Improves AWS security
- Easy to reuse across multiple IAM identities
- Reduces accidental over-permissioning

---

# ❌ Limitations

- Does **not** grant permissions
- Cannot be attached to IAM Groups
- Applies only to IAM Users and Roles
- Cannot override an explicit **Deny**
- Only limits identity-based policies

---

# 💡 Best Practices

- Use Permission Boundaries when delegating IAM administration.
- Follow the Principle of Least Privilege.
- Create reusable boundary policies.
- Combine with IAM Policies, SCPs, and Resource-based Policies for layered security.
- Regularly review Permission Boundaries to maintain security.

---

# 🧠 Easy Analogy

Imagine entering a shopping mall.

- 📝 **IAM Policy** = Your shopping list (what you are allowed to buy)
- 💳 **Permission Boundary** = Your spending limit (the maximum amount you can spend)

Even if your shopping list includes expensive items, you cannot buy them if they exceed your spending limit.

Similarly, an IAM Policy may allow many AWS services, but the Permission Boundary restricts the maximum permissions available.

---

# 🎯 Key Takeaways

- Permission Boundaries **do not grant permissions**.
- They define the **maximum permissions** an IAM User or IAM Role can have.
- Effective permissions are the **intersection** of the IAM Policy and the Permission Boundary.
- They are ideal for delegated administration and preventing privilege escalation.
- Permission Boundaries can be attached only to **IAM Users** and **IAM Roles**, not IAM Groups.

---

## 📚 Related IAM Topics

- Root User
- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- IAM Permission Boundaries
- IAM Policy Evaluation Logic
- IAM Best Practices

---
**⭐ If this guide helped you, consider giving the repository a Star!**
