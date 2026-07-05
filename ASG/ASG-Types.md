 # 📈 Types of Scaling in AWS

Scaling is the process of **increasing or decreasing computing resources** based on application traffic or workload.

AWS Auto Scaling automatically adjusts resources to maintain application performance while optimizing costs.

There are **two main types of scaling**:

1. 🔄 Horizontal Scaling
2. ⬆️⬇️ Vertical Scaling

---

# 🔄 1. Horizontal Scaling

**Horizontal Scaling** means **adding or removing EC2 instances (servers)** based on application demand.

It is commonly used for web applications and works well with **Elastic Load Balancer (ELB)**.

Horizontal Scaling has **two operations**:

- 📈 Scale Out
- 📉 Scale In

---

## 📈 What is Scale Out?

**Scale Out** means **adding more EC2 instances** when application traffic increases.

Instead of upgrading one server, AWS launches additional EC2 instances to share the workload.

> **Simple Definition:**  
> **Scale Out adds more servers to handle increased traffic.**


## 📉  What is Scale In?

**Scale In** means **removing unnecessary EC2 instances** when traffic decreases.

AWS terminates the extra instances to reduce costs while maintaining application performance.

> **Simple Definition:**  
> **Scale In removes extra servers when traffic is low.**

---

# ⬆️⬇️ 2. Vertical Scaling

**Vertical Scaling** means **increasing or decreasing the resources of an existing EC2 instance**, such as CPU, RAM, or Storage.

Instead of adding more servers, AWS changes the size of the existing server.

Vertical Scaling has **two operations**:

- ⬆️ Scale Up
- ⬇️ Scale Down

---

## ⬆️ Scale Up

### 📖 What is Scale Up?

**Scale Up** means **increasing the CPU, RAM, or Storage** of an existing EC2 instance.

> **Simple Definition:**  
> **Scale Up increases the size or capacity of an existing server.**

### 📊 Diagram

```text
Before

🖥️ EC2
2 vCPU
4 GB RAM

⬇️

After Scale Up

🖥️ EC2
8 vCPU
16 GB RAM
```

## ⬇️ What is Scale Down?

**Scale Down** means **reducing the CPU, RAM, or Storage** of an EC2 instance when fewer resources are needed.

> **Simple Definition:**  
> **Scale Down decreases the size or capacity of an existing server to save costs.**

### 📊 Diagram

```text
Before

🖥️ EC2
8 vCPU
16 GB RAM

⬇️

After Scale Down

🖥️ EC2
2 vCPU
4 GB RAM
```
---

# 🧠 Easy to Remember

```text
Horizontal Scaling
├── 📈 Scale Out  → Add More Servers
└── 📉 Scale In   → Remove Servers

Vertical Scaling
├── ⬆️ Scale Up   → Bigger Server
└── ⬇️ Scale Down → Smaller Server
```

---
