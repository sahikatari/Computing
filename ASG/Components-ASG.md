# ⚙️ Components of an Auto Scaling Group (ASG)

An **Auto Scaling Group (ASG)** automatically adds or removes EC2 instances to maintain application performance and availability.

The main components of an ASG are:

1. 🖥️ Launch Template (or Launch Configuration)
2. 👥 Auto Scaling Group (ASG)
3. 📈 Scaling Policies
4. ❤️ Health Checks
5. ⚖️ Elastic Load Balancer (ELB) *(Optional but commonly used)*
6. 📊 Amazon CloudWatch

---

# 📚 Summary

| Component | Purpose |
|-----------|---------|
| 📜 Launch Template | Blueprint for launching EC2 instances |
| 👥 Auto Scaling Group | Manages EC2 instances automatically |
| 📈 Scaling Policies | Decides when to scale in or out |
| ❤️ Health Checks | Detects and replaces unhealthy instances |
| ⚖️ Elastic Load Balancer | Distributes traffic across EC2 instances |
| 📊 Amazon CloudWatch | Monitors metrics and triggers scaling |
