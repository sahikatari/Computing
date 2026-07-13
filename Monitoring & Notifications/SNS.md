# 📢 Amazon Simple Notification Service (SNS)

> Amazon SNS is a fully managed messaging service that enables applications and AWS services to send notifications to multiple subscribers.

---

# 📖 What is Amazon SNS?

Amazon SNS (Simple Notification Service) is a publish/subscribe messaging service.

One publisher sends a message to a Topic.

SNS delivers the message to all subscribers.

---

# 🎯 Why Use SNS?

- Email notifications
- SMS alerts
- Lambda triggers
- CloudWatch alarm notifications
- Fan-out messaging

---

# 🔄 Architecture Flow

```text
Publisher
    │
    ▼
 SNS Topic
 ┌──┼─────┬─────┐
 ▼  ▼     ▼     ▼
Email SMS Lambda SQS
```

---

# 🧩 Components

| Component | Description |
|-----------|-------------|
| Topic | Communication channel |
| Publisher | Sends messages |
| Subscriber | Receives messages |
| Endpoint | Email, SMS, Lambda, HTTP, SQS |

---

# ✨ Features

- Pub/Sub Messaging
- Email
- SMS
- Lambda
- HTTP/HTTPS
- Mobile Push Notifications

---

# 💼 Use Cases

- CloudWatch Alerts
- Order Notifications
- Billing Alerts
- Application Notifications
- Auto Scaling Notifications

---

# ✅ Advantages

- Fully Managed         
- Highly Available      
- Scalable              
- Easy Integration
- Low Latency

---

# ❌ Limitations

- No message persistence
- Message size limit (256 KB)
- Ordering not guaranteed (Standard Topics)

---


# 🎯 Key Takeaways

- SNS is a publish/subscribe service.
- Supports multiple subscribers.
- Integrates with CloudWatch.
- Delivers notifications instantly.
