# 📊 Amazon CloudWatch

---

# 📖 What is Amazon CloudWatch?

Amazon CloudWatch is an AWS monitoring and observability service that collects, monitors, and analyzes metrics, logs, and events from AWS resources and applications.

It helps you monitor system performance, troubleshoot issues, and automate responses.

> **Monitor → Analyze → Alert → Automate**

---

# 🎯 Why Use CloudWatch?

CloudWatch helps you:

- Monitor AWS resources
- Collect metrics
- Store application logs
- Create alarms
- Build dashboards
- Automate actions
- Improve application performance

---

# ⚙️ How CloudWatch Works

1. AWS resources send metrics and logs.
2. CloudWatch stores the data.
3. Alarms monitor thresholds.
4. Notifications are sent using SNS.
5. Automated actions can be triggered.

---


# 🧩 Components

| Component | Purpose |
|------------|---------|
| Metrics | Performance data |
| Logs | Application and system logs |
| Alarms | Threshold-based alerts |
| Dashboards | Visualization |
| Events | Event-driven automation |
| Agent | Collect custom metrics |

---

# ✨ Features

- Metrics Monitoring
- Log Collection
- Custom Metrics
- Dashboards
- Alarms
- EventBridge Integration
- Auto Scaling Integration

---

# 📈 CloudWatch Metrics

Examples:

- CPU Utilization
- Network In/Out
- Disk Read/Write
- Memory (Custom)
- Status Check

---

# 📜 CloudWatch Logs

Stores logs from:

- EC2
- Lambda
- ECS
- Applications
- Custom Servers

---

# 🚨 CloudWatch Alarms

Monitor metrics and perform actions.

Example:

```text
CPU > 80%
      │
      ▼
CloudWatch Alarm
      │
      ▼
SNS Notification
```

---

# 📊 Dashboards

Create customized dashboards to visualize metrics.

---

# 💼 Use Cases

- EC2 Monitoring
- Application Monitoring
- Auto Scaling
- Performance Analysis
- Log Monitoring

---


# ⚖️ CloudWatch vs CloudTrail

| CloudWatch | CloudTrail |
|------------|-----------|
| Monitors performance | Records API activity |
| Metrics & Logs | API Logs |
| Real-time | Audit History |

---



# 🎯 Key Takeaways

- Monitors AWS resources.
- Stores metrics and logs.
- Creates alarms.
- Supports dashboards.
- Integrates with SNS and Auto Scaling.
