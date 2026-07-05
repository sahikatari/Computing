# 🚀 AWS Auto Scaling & Launch Templates

## 📖 What is Auto Scaling?

**AWS Auto Scaling** automatically adjusts the number of **EC2 instances** based on application demand. It helps maintain high availability, improves performance, and reduces costs by adding or removing instances as needed.

### 💡 Simple Definition
> **Auto Scaling automatically adds EC2 instances when traffic increases and removes them when traffic decreases.**


### 🎯 Benefits of Auto Scaling

- ✅ Automatically handles traffic spikes
- ✅ Improves application availability
- ✅ Replaces unhealthy EC2 instances
- ✅ Reduces infrastructure cost
- ✅ Integrates seamlessly with Load Balancers
- ✅ Ensures high availability across multiple Availability Zones

---

# ⚙️ Auto Scaling Group (ASG)

An **Auto Scaling Group (ASG)** manages a group of EC2 instances using a **Launch Template**.

### ASG Configuration

| Setting | Description |
|----------|-------------|
| **Minimum Capacity** | Minimum number of EC2 instances that always run |
| **Desired Capacity** | Target number of running EC2 instances |
| **Maximum Capacity** | Maximum number of EC2 instances Auto Scaling can launch |

### Example

```text
Minimum Capacity : 2
Desired Capacity : 3
Maximum Capacity : 6

Traffic Low  → 2–3 Instances
Traffic High → Up to 6 Instances
```

---

