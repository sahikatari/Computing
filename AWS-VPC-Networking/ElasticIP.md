# 🌐 AWS Elastic IP (EIP)

> A beginner-friendly guide to understanding **Elastic IP Addresses (EIP)** in AWS.

---

# 📚 Table of Contents

- What is an Elastic IP?
- Why Use an Elastic IP?
- How Elastic IP Works
- Features
- Use Cases
- Summary

---

# 🌐 What is an Elastic IP?

An **Elastic IP (EIP)** is a **static public IPv4 address** provided by AWS.

Unlike a normal public IP, an Elastic IP remains the same even if you stop and start an EC2 instance (when re-associated).

You can associate an Elastic IP with:

- EC2 Instance
- NAT Gateway
- Network Interface (ENI)

> **Simple Definition:**  
> An Elastic IP is a permanent public IP address that you control in AWS.

---

# ❓ Why Use an Elastic IP?

Elastic IPs help you:

- Maintain a fixed public IP address
- Avoid changing IP addresses after instance replacement
- Support DNS and web applications
- Quickly recover from instance failures
- Redirect traffic to another EC2 instance if needed

---


# ⭐ Features

- Static Public IPv4 Address
- Region-specific
- Can be reassociated with another EC2 instance
- Supports high availability and failover
- Used with NAT Gateway
- Managed by AWS

---


# 💼 Common Use Cases

- Hosting Websites
- Bastion Host
- NAT Gateway
- Production EC2 Instances
- Failover and Disaster Recovery

---

# 💰 Pricing

- An Elastic IP is generally **free** when it is associated with a running EC2 instance.
- AWS may charge for:
  - Unassociated (idle) Elastic IPs
  - Additional Elastic IPs beyond the free allocation
  - Excessive remapping

> **Tip:** Release unused Elastic IPs to avoid unnecessary charges.

---

# ✅ Best Practices

- Use Elastic IPs only when a static public IP is required.
- Release unused Elastic IPs.
- Use Route 53 for DNS instead of hardcoding IP addresses.
- Use Elastic IPs for Bastion Hosts and NAT Gateways.
- Avoid assigning Elastic IPs to every EC2 instance.

---


# 📝 Summary

- Elastic IP is a **static public IPv4 address** in AWS.
- It can be reassociated with another resource within the same Region.
- It is commonly used for production servers, Bastion Hosts, and NAT Gateways.
- Unlike a regular Public IP, it does not change after instance replacement or reassociation.
- Release unused Elastic IPs to minimize costs.

---
