# 🌐 CIDR Blocks & Subnet Masks in AWS VPC

> A concise guide to understanding **CIDR Blocks** and **Subnet Masks** for AWS VPC Networking.

---

# 📚 Table of Contents

- What is CIDR?
- What is a Subnet Mask?
- CIDR Format
- Network & Host Bits
- CIDR vs Subnet Mask
- Common CIDR & Subnet Mask Table
- AWS Reserved IP Addresses
- CIDR in AWS VPC
- CIDR Rules
- Summary

---

# 🌐 What is CIDR?

**CIDR (Classless Inter-Domain Routing)** is a method of defining an IP address range using a **prefix length**.

### Format

```text
IP Address/Prefix Length
```

### Example

```text
10.0.0.0/16
```

- **10.0.0.0** → Network Address
- **/16** → Network Prefix (16 network bits)

> **Simple Definition:** CIDR determines the size of a network and the number of available IP addresses.

---

# 🛡️ What is a Subnet Mask?

A **Subnet Mask** is a **32-bit number** that separates an IP address into:

- 🌐 Network Portion
- 💻 Host Portion

Example:

```text
IP Address  : 10.0.1.15
Subnet Mask : 255.255.255.0
```

Here:

- **Network** → `10.0.1`
- **Host** → `15`

---

# 🧠 Network & Host Bits

An IPv4 address contains **32 bits**.

Example:

```text
10.0.0.0/24
```

| Network Bits | Host Bits |
|--------------|-----------|
| 24 | 8 |

Available IPs:

```text
2⁸ = 256 IP Addresses
```

---

# 🔄 CIDR vs Subnet Mask

| CIDR | Subnet Mask |
|------|-------------|
| /16 | 255.255.0.0 |
| /20 | 255.255.240.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |

> AWS uses **CIDR notation**, while the subnet mask is its equivalent dotted-decimal representation.

---

# 📊 Common CIDR & Subnet Mask Table

| CIDR | Subnet Mask | Total IPs | AWS Usable IPs |
|------|-------------|-----------|----------------|
| /16 | 255.255.0.0 | 65,536 | 65,531 |
| /20 | 255.255.240.0 | 4,096 | 4,091 |
| /24 | 255.255.255.0 | 256 | 251 |
| /25 | 255.255.255.128 | 128 | 123 |
| /26 | 255.255.255.192 | 64 | 59 |
| /27 | 255.255.255.224 | 32 | 27 |
| /28 | 255.255.255.240 | 16 | 11 |

> **AWS reserves 5 IP addresses** in every subnet.

---

# ☁️ CIDR in AWS VPC

When creating a VPC, you define a CIDR block.

Example:

```text
VPC CIDR
10.0.0.0/16
```

You can divide it into multiple subnets:

| Subnet | CIDR |
|---------|------|
| Public Subnet 1 | 10.0.1.0/24 |
| Public Subnet 2 | 10.0.2.0/24 |
| Private Subnet 1 | 10.0.3.0/24 |
| Private Subnet 2 | 10.0.4.0/24 |

---

# ⚠️ Important AWS CIDR Rules

- ✅ A subnet CIDR must be within the VPC CIDR.
- ✅ Subnet CIDR blocks cannot overlap.
- ✅ Each subnet belongs to a single Availability Zone.
- ✅ Plan CIDR ranges for future expansion.
- ✅ AWS reserves the first **4 IP addresses** and the **last IP address** in every subnet.

---

# 📝 Summary

- **CIDR** defines the IP address range of a VPC or subnet.
- **Subnet Mask** separates the network and host portions of an IP address.
- AWS primarily uses **CIDR notation** (e.g., `/24`), while subnet masks are its dotted-decimal equivalent (e.g., `255.255.255.0`).
- Every IPv4 address has **32 bits** divided into **network** and **host** bits.
- AWS reserves **5 IP addresses** in every subnet.
- Proper CIDR planning is essential for scalable, secure, and well-organized VPC networking.

---
