# 🔐 AWS Security Token Service (AWS STS)

  ---

# 📖 What is AWS Security Token Service (AWS STS)?

**AWS Security Token Service (STS)** is a web service that allows you to request **temporary security credentials** for AWS resources.

These credentials consist of:

- Access Key ID
- Secret Access Key
- Session Token

Unlike IAM User credentials, STS credentials are **temporary** and automatically expire after a specified duration.

> **AWS STS improves security by eliminating the need for long-term access keys.**

---

# 🎯 Why Use AWS STS?

AWS STS is commonly used to:

- Provide temporary access to AWS resources
- Allow users to assume IAM Roles
- Enable cross-account access
- Support Single Sign-On (SSO)
- Provide temporary credentials to applications
- Improve security by avoiding permanent credentials

---

# 🔄 AWS STS Workflow

```text
        User / Application
                 │
                 ▼
      Request Temporary Credentials
                 │
                 ▼
          AWS Security Token Service
                 │
                 ▼
 Temporary Credentials Issued
 (Access Key + Secret Key + Session Token)
                 │
                 ▼
      Access AWS Resources
                 │
                 ▼
     Credentials Expire Automatically
```

---

# ✨ Key Features

- Temporary security credentials
- Automatic credential expiration
- Supports IAM Roles
- Enables cross-account access
- Supports Multi-Factor Authentication (MFA)
- Works with AWS Identity Center and federated identities

---


# 💼 Real-World Use Cases

### 👨‍💻 Temporary Administrator Access

Provide administrators temporary elevated permissions without creating permanent credentials.

---

### 🏢 Cross-Account Access

Allow an IAM Role in **Account A** to securely access resources in **Account B**.

---

### 🌐 Single Sign-On (SSO)

Employees authenticate through a corporate identity provider and receive temporary AWS credentials.

---

### 📱 Mobile Applications

Mobile apps receive temporary credentials instead of storing AWS access keys.

---

# 📝 Example Workflow

Suppose a developer needs temporary administrator access.

### Step 1

The developer requests access using:

```text
AssumeRole
```

### Step 2

AWS STS verifies the request.

### Step 3

STS returns:

```text
Access Key ID
Secret Access Key
Session Token
```

### Step 4

The developer performs AWS operations.

### Step 5

After one hour (or configured duration), the credentials expire automatically.

---

# 💡 Best Practices

- Prefer IAM Roles with AWS STS over IAM User access keys.
- Use the shortest session duration that meets your needs.
- Enable MFA for sensitive operations.
- Avoid storing temporary credentials in code.
- Monitor STS activity using AWS CloudTrail.
- Rotate long-term credentials when they are required.

---

# 🧠 Easy Analogy

Imagine visiting a company office.

- 🪪 **IAM User Credentials** = Permanent Employee ID Card
- 🎫 **AWS STS Credentials** = Temporary Visitor Pass

A visitor pass allows access only for a limited time. Once it expires, it becomes invalid.

Similarly, AWS STS provides temporary credentials that automatically expire, improving security.

---

# 📊 Summary

| Feature | AWS STS |
|----------|----------|
| Purpose | Provides temporary AWS credentials |
| Credential Type | Temporary |
| Automatically Expires | ✅ Yes |
| Supports IAM Roles | ✅ Yes |
| Cross-Account Access | ✅ Yes |
| Session Token | ✅ Yes |
| Best For | Temporary, secure access |

---

# 🎯 Key Takeaways

- AWS STS provides **temporary security credentials**.
- Credentials include an **Access Key ID**, **Secret Access Key**, and **Session Token**.
- Temporary credentials automatically expire.
- AWS STS is commonly used with **IAM Roles**, **SSO**, and **cross-account access**.
- Using AWS STS is more secure than sharing long-term IAM User access keys.

---

