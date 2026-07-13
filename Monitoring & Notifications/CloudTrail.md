# 📜 AWS CloudTrail

> AWS CloudTrail records and tracks API activity and account events across your AWS environment for auditing, governance, and security.

---

# 📖 What is AWS CloudTrail?

AWS CloudTrail records AWS API calls made by users, applications, IAM roles, and AWS services.

It helps with:

- Security
- Auditing
- Compliance
- Troubleshooting

---

# 🎯 Why Use CloudTrail?

- Audit AWS activity
- Monitor account changes
- Investigate security incidents
- Compliance reporting

---

# 🔄 Architecture Flow

```text
User / CLI / SDK
        │
        ▼
 AWS API Calls
        │
        ▼
 CloudTrail
        │
        ▼
   S3 Bucket
        │
        ▼
 CloudWatch Logs
```

---

# 🧩 Components

| Component | Purpose |
|-----------|---------|
| Trail | Records events |
| Event History | Last 90 days |
| S3 | Stores logs |
| CloudWatch | Monitoring |
| EventBridge | Automation |

---

# 📂 Event Types

- Management Events
- Data Events
- Insights Events

---

# ✨ Features

- API Logging
- Event History
- Multi-region Trails
- Log Integrity Validation
- CloudWatch Integration

---

# 💼 Use Cases

- Compliance
- Security Auditing
- Troubleshooting
- Governance
- Change Tracking

---

# ✅ Advantages

- Free 90-day Event History
- Secure Logging
- AWS-wide Coverage
- Easy Integration

---

# ❌ Limitations

- Not real-time monitoring
- Data events incur additional cost
- Requires S3 for long-term storage

---

# ⚖️ CloudTrail vs CloudWatch

| CloudTrail | CloudWatch |
|------------|------------|
| API Activity | Performance Monitoring |
| Audit | Metrics |
| Security | Monitoring |

---

# 💡 Best Practices

- Enable multi-region trails.
- Store logs in encrypted S3 buckets.
- Enable log validation.
- Integrate with CloudWatch.
- Restrict log access using IAM.

---


# 🎯 Key Takeaways

- CloudTrail records AWS API activity.
- Supports auditing and compliance.
- Stores logs in Amazon S3.
- Integrates with CloudWatch and EventBridge.
- Essential for security investigations.
