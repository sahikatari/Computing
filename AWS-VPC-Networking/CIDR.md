# 🌐 CIDR Blocks in AWS VPC

> A beginner-friendly guide to understanding **CIDR (Classless Inter-Domain Routing)** and how it is used in AWS VPC networking.

---

# 📚 Table of Contents

- What is CIDR?
- Why CIDR is Important
- CIDR Block Format
- Network & Host Bits
- CIDR Prefix Table
- Private IPv4 Address Ranges
- CIDR in AWS VPC
- CIDR Examples
- Summary

---

# 🌐 What is CIDR?

**CIDR (Classless Inter-Domain Routing)** is a method of allocating IP addresses and defining network ranges using a **prefix length**.

Instead of using traditional IP classes (Class A, B, and C), CIDR provides a more flexible and efficient way to assign IP addresses.

### Simple Definition

> CIDR specifies how many bits belong to the **network** and how many belong to **hosts**.

---

# ❓ Why is CIDR Important?

CIDR helps to:

- 📌 Define the IP range of a VPC
- 🌐 Create subnets from a network
- 🚀 Reduce IP address wastage
- 🔒 Organize networks efficiently
- ⚡ Improve routing performance

---

# 📝 CIDR Block Format

A CIDR block consists of:

```
IP Address / Prefix Length
```

### Example

```
10.0.0.0/16
```

Where:

- **10.0.0.0** → Network Address
- **/16** → Prefix Length (Network Bits)

---

# 🧠 Understanding Network & Host Bits

An IPv4 address has **32 bits**.

The prefix length (`/`) determines how many bits are reserved for the network.

Example:

```
10.0.0.0/24
```

| Part | Bits |
|------|------|
| Network Bits | 24 |
| Host Bits | 8 |

Number of possible addresses:

```
2^8 = 256 IP Addresses
```

---

# 📊 Common CIDR Prefix Table

| Prefix | Subnet Mask | Total IPs | Usable IPs* |
|---------|-------------|-----------|-------------|
| /16 | 255.255.0.0 | 65,536 | 65,531 |
| /17 | 255.255.128.0 | 32,768 | 32,763 |
| /18 | 255.255.192.0 | 16,384 | 16,379 |
| /19 | 255.255.224.0 | 8,192 | 8,187 |
| /20 | 255.255.240.0 | 4,096 | 4,091 |
| /21 | 255.255.248.0 | 2,048 | 2,043 |
| /22 | 255.255.252.0 | 1,024 | 1,019 |
| /23 | 255.255.254.0 | 512 | 507 |
| /24 | 255.255.255.0 | 256 | 251 |
| /25 | 255.255.255.128 | 128 | 123 |
| /26 | 255.255.255.192 | 64 | 59 |
| /27 | 255.255.255.224 | 32 | 27 |
| /28 | 255.255.255.240 | 16 | 11 |

> **Note:** AWS reserves **5 IP addresses** in every subnet, so usable IPs are Total IPs − 5.

---



# ☁️ CIDR in AWS VPC

When creating a VPC, you must specify a CIDR block.

Example:

```
VPC CIDR:
10.0.0.0/16
```

You can then divide it into smaller subnets.

Example:

| Subnet | CIDR |
|---------|------|
| Public Subnet 1 | 10.0.1.0/24 |
| Public Subnet 2 | 10.0.2.0/24 |
| Private Subnet 1 | 10.0.3.0/24 |
| Private Subnet 2 | 10.0.4.0/24 |

---

# ⚠️ CIDR Rules in AWS

- A subnet CIDR must be within the VPC CIDR range.
- Subnet CIDR blocks cannot overlap.
- Each subnet belongs to only one Availability Zone.
- Plan CIDR blocks carefully to allow future expansion.
- AWS reserves 5 IP addresses in every subnet.

---

# 📝 Summary

- CIDR defines the IP address range for VPCs and subnets.
- It uses the format **IP Address/Prefix Length**.
- The prefix length determines the number of network and host bits.
- AWS VPCs use private IPv4 address ranges by default.
- Proper CIDR planning helps create scalable, organized, and conflict-free networks.
- AWS reserves **5 IP addresses** in every subnet.

---

