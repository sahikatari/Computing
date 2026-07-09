# 🌐 AWS VPC Fundamentals

> Learn the core concepts of **Amazon Virtual Private Cloud (VPC)**, including Default VPC, Custom VPC, CIDR Blocks, IPv4, and IPv6. This guide provides the theoretical foundation required before creating AWS networking architectures.

---

# 📚 Table of Contents

- What is a VPC?
- Features of a VPC
- Default VPC
- Custom VPC
- Default VPC vs Custom VPC
- CIDR Blocks
- IPv4 vs IPv6
- Best Practices
- Interview Questions
- Key Takeaways

---

# 🌍 What is a VPC?

**Amazon Virtual Private Cloud (Amazon VPC)** is a logically isolated virtual network within AWS where you can securely launch AWS resources such as:

- 🖥️ EC2 Instances
- 🗄️ RDS Databases
- ⚖️ Load Balancers
- 📦 ECS Tasks
- ⚡ Lambda Functions
- 💾 Storage Services

A VPC provides complete control over your networking environment, including IP addressing, subnets, routing, internet connectivity, and security.

---

# ✨ Features of a VPC

- 🔒 Logically isolated network
- 🌐 Supports IPv4 and IPv6
- 🏗️ Create Public and Private Subnets
- 📡 Route Tables for traffic management
- 🌍 Internet Gateway for internet access
- 🔐 Security Groups and Network ACLs
- 📈 High Availability across Availability Zones
- 🔗 VPN and Direct Connect support
- 📊 VPC Flow Logs for monitoring

---

# 🌍 Default VPC

A **Default VPC** is automatically created by AWS in every Region when an AWS account is created.

It allows users to launch AWS resources immediately without performing any networking configuration.

## Features

| Feature | Description |
|----------|-------------|
| Created By | AWS |
| Internet Gateway | Automatically Attached |
| Public Subnets | Available |
| Route Table | Preconfigured |
| Internet Access | Enabled |
| DNS Resolution | Enabled |
| DNS Hostnames | Enabled |

---

# 🏗️ Custom VPC

A **Custom VPC** is manually created by the user.

It offers complete control over networking, security, routing, and internet connectivity, making it the preferred choice for production environments.


---

# 📊 Default VPC vs Custom VPC

| Feature | Default VPC | Custom VPC |
|----------|-------------|------------|
| Created By | AWS | User |
| Internet Gateway | Automatic | Manual |
| Public Subnets | Yes | User Creates |
| Route Tables | Preconfigured | User Configures |
| Security | Basic | Fully Customizable |
| Best For | Learning | Production |

---

# 🌐 CIDR & Subnet Mask in AWS VPC Networking

> Learn the fundamentals of CIDR and Subnet Masks used in AWS VPC Networking.

---

# 📖 What is CIDR?

**CIDR (Classless Inter-Domain Routing)** is a method of allocating IP addresses and defining the size of a network.

Every **AWS VPC** and **Subnet** requires a **CIDR block**.

**Syntax**

```text
IP Address/Prefix Length
```

Example

```text
10.0.0.0/16
```

- **10.0.0.0** → Network Address
- **/16** → Prefix Length (Network Bits)

---

# 🎯 Why CIDR is Used

- Defines the IP range of a VPC or Subnet.
- Allows subnet creation.
- Prevents overlapping IP ranges.
- Supports efficient IP allocation.

---

# 🛡️ What is a Subnet Mask?

A **Subnet Mask** is a 32-bit number that separates an IP address into:

- 🌐 Network Portion
- 🖥️ Host Portion

Example

```text
IP Address  : 192.168.1.10
Subnet Mask : 255.255.255.0
```

---

# 🔄 CIDR vs Subnet Mask

Both represent the **same network**, but in different formats.

| CIDR | Subnet Mask |
|------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |

Example

```text
10.0.0.0/24 = 255.255.255.0
```

---

# 🏗️ Network Bits & Host Bits

```text
10.0.0.0/24

|<------24 Bits------>|<----8 Bits---->|
+---------------------+----------------+
|    Network Bits     |   Host Bits    |
+---------------------+----------------+
```

- **Network Bits** identify the network.
- **Host Bits** identify devices in that network.

---

# ☁️ CIDR in AWS

Example

```text
VPC CIDR

10.0.0.0/16
```

Available IP Range

```text
10.0.0.0
     ↓
10.0.255.255
```

AWS uses **CIDR notation** instead of subnet masks.

---

# 🚫 AWS Reserved IP Addresses

AWS reserves **5 IP addresses** in every subnet.

| Reserved IP | Purpose |
|-------------|---------|
| First IP | Network Address |
| Second IP | VPC Router |
| Third IP | Amazon DNS |
| Fourth IP | Reserved by AWS |
| Last IP | Reserved |

Example

```text
Subnet: 10.0.1.0/24

Usable IPs:
10.0.1.4 → 10.0.1.254
```

---
