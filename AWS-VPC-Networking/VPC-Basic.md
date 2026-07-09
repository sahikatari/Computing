# 🌐 AWS VPC Basics
---

# 📚 Table of Contents

- What is a VPC?
- Why Do We Need a VPC?
- Features of VPC
- Default VPC
- Custom VPC
- CIDR Block
- IPv4 & IPv6
- VPC Components
- VPC Limits
- Best Practices
- Interview Questions
- Summary

---

# 🌐 What is a VPC?

**Amazon Virtual Private Cloud (VPC)** is a logically isolated virtual network within AWS where you can launch and manage AWS resources securely.

Think of a VPC as your **private data center in the AWS Cloud**, where you have complete control over:

- IP Address Range
- Subnets
- Route Tables
- Internet Connectivity
- Security Rules

> **Simple Definition:**  
> A VPC is your own private network inside AWS.

---

# ❓ Why Do We Need a VPC?

- ✅ Isolated environment
- ✅ Better security
- ✅ Private & Public networks
- ✅ Full networking control
- ✅ Highly scalable

---

# ⭐ Features of Amazon VPC

- 🔒 Network Isolation
- 🌍 Public & Private Subnets
- 📌 Custom IP Address Range (CIDR)
- 🔄 Route Tables
- 🌐 Internet Gateway
- 🔐 Security Groups
- 🚧 Network ACLs
- 🔗 VPN Connectivity
- 🏢 AWS Direct Connect Support
- 🌍 IPv4 & IPv6 Support

---

# 🏠 Default VPC

Every AWS Region comes with a **Default VPC**.

### Characteristics

- Already created by AWS
- Easy to use
- Public subnet available
- Internet Gateway attached
- Default Route Table
- Default Security Group
- Default Network ACL

### Default CIDR

```
172.31.0.0/16
```

### Best For

- Learning AWS
- Quick Testing
- Small Applications

---

# 🛠️ Custom VPC

A **Custom VPC** is created manually by the user.

You decide:

- CIDR Block
- Number of Subnets
- Route Tables
- Security Groups
- Network ACLs
- Internet Gateway
- NAT Gateway

### Best For

- Production Applications
- Enterprise Networks
- Secure Infrastructure

---

# 📍 CIDR Block

A **CIDR (Classless Inter-Domain Routing)** block defines the range of IP addresses available in a VPC.

### Example

```
10.0.0.0/16
```

Meaning:

- Network Address → `10.0.0.0`
- Prefix → `/16`
- Total IP Addresses → 65,536

Common VPC CIDR Blocks:

| CIDR | Total IPs |
|------|-----------|
| /16 | 65,536 |
| /20 | 4,096 |
| /24 | 256 |
| /28 | 16 |

---

# 🌍 IPv4 & IPv6

## IPv4

- 32-bit address
- Four octets
- Example:

```
192.168.1.10
```

Supports approximately:

```
4.3 Billion Addresses
```

---

## IPv6

- 128-bit address
- Hexadecimal format

Example:

```
2001:db8::1
```

Supports:

```
340 Undecillion Addresses
```

AWS supports both IPv4 and IPv6 in VPCs.

---

# 🧩 Core Components of a VPC

| Component | Purpose |
|-----------|----------|
| VPC | Virtual Network |
| Subnet | Divides the VPC into smaller networks |
| Route Table | Controls network traffic |
| Internet Gateway | Provides Internet access |
| NAT Gateway | Allows private instances to access the Internet |
| Security Group | Instance-level firewall |
| Network ACL | Subnet-level firewall |
| Elastic IP | Static Public IP |
| VPN Gateway | Secure connection to on-premises |
| VPC Peering | Connects two VPCs |

---

# 📊 Basic VPC Architecture

```text
                    AWS Cloud
                        │
               ┌────────▼────────┐
               │      VPC        │
               │   10.0.0.0/16   │
               └────────┬────────┘
                        │
        ┌───────────────┴───────────────┐
        │                               │
 ┌──────▼──────┐                 ┌──────▼──────┐
 │ Public      │                 │ Private     │
 │ Subnet      │                 │ Subnet      │
 └──────┬──────┘                 └──────┬──────┘
        │                               │
 Internet Gateway                 NAT Gateway
        │                               │
     Internet                    Private Resources
```



---


# 📝 Summary

- Amazon VPC provides an isolated virtual network in AWS.
- Every AWS account includes a Default VPC in each Region.
- Custom VPCs offer complete control over networking.
- CIDR blocks define the available IP address range.
- VPC supports both IPv4 and IPv6.
- Security Groups and Network ACLs protect network traffic.
- Public and Private Subnets improve security and organization.
- A well-designed VPC is the foundation of secure and scalable AWS architectures.

---

