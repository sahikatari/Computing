# TYPES OF LOADBALANCER
---
## ⚖️ Application Load Balancer (ALB)

### 📖 What is an Application Load Balancer?

An **Application Load Balancer (ALB)** is an AWS load balancer that works at **Layer 7 (Application Layer)** of the OSI model.

It distributes **HTTP and HTTPS** traffic based on application information such as the **URL path**, **hostname**, **headers**, and **cookies**.

> **Simple Definition:**  
> **An Application Load Balancer (ALB) distributes HTTP/HTTPS traffic to different servers based on application-level rules like URL paths and hostnames.**

### ✨ Key Features

- 🌐 Works at **Layer 7 (Application Layer)**
- 🔒 Supports **HTTP, HTTPS, HTTP/2, WebSocket, and gRPC**
- 🛣️ Supports **Path-based Routing** (e.g., `/api`, `/images`)
- 🌍 Supports **Host-based Routing** (e.g., `api.example.com`, `shop.example.com`)
- ❤️ Manage **Sticky Session** 
- 🖥️ Can route traffic to **EC2 Instances**, **IP Addresses**, and **AWS Lambda**
---
# ⚡ Network Load Balancer (NLB)

### 📖 What is a Network Load Balancer?

A **Network Load Balancer (NLB)** is an AWS load balancer that works at **Layer 4 (Transport Layer)** of the OSI model.

It distributes **TCP, UDP, and TLS** traffic with **high performance** and **ultra-low latency**, making it ideal for applications that handle millions of requests.

> **Simple Definition:**  
> **A Network Load Balancer (NLB) distributes TCP, UDP, and TLS traffic across multiple servers with high speed and low latency.**

### ✨ Key Features

- ⚡ Works at **Layer 4 (Transport Layer)**
- 🌐 Supports **TCP, UDP, and TLS** protocols
- 🚀 Provides **ultra-low latency** and **high performance**
- 📈 Handles **millions of requests per second**
- 🌍 Preserves the **client's source IP address**
- ❤️ Performs **Health Checks** on targets
- 📍 Supports **Static IP Addresses** and **Elastic IPs**
- 📈 Integrates with **Auto Scaling** and **Amazon EC2**

---

# 🛡️ Gateway Load Balancer (GWLB)

### 📖 What is a Gateway Load Balancer?

A **Gateway Load Balancer (GWLB)** is an AWS load balancer designed to **deploy, manage, and scale network security appliances** such as firewalls, intrusion detection systems (IDS), and intrusion prevention systems (IPS).

> **Simple Definition:**  
> **A Gateway Load Balancer (GWLB) distributes network traffic to security appliances like firewalls, IDS, and IPS for inspection and protection.**

### ✨ Key Features

- 🛡️ Works at **Layer 3 (Network Layer)**
- 🌐 Uses the **GENEVE protocol**
- ⚖️ Distributes traffic across multiple security appliances
- 📈 Automatically scales security appliances based on traffic
- ❤️ Performs **Health Checks** on appliances
- 🔍 Supports **transparent traffic inspection**
- 🔗 Integrates with **Amazon VPC** using **Gateway Load Balancer Endpoints (GWLBE)**
---

# 📦 Classic Load Balancer (CLB)

### 📖 What is a Classic Load Balancer?

A **Classic Load Balancer (CLB)** is the **first-generation load balancer** provided by AWS.

It automatically distributes incoming traffic across multiple **EC2 instances** to improve **availability**, **reliability**, and **fault tolerance**.

> **Simple Definition:**  
> **A Classic Load Balancer (CLB) distributes incoming traffic across multiple EC2 instances to improve application availability and reliability.**


### ✨ Key Features

- 📡 Supports **Layer 4 (TCP/SSL)** and **Layer 7 (HTTP/HTTPS)**
- ⚖️ Distributes traffic across multiple **EC2 instances**
- ❤️ Performs **Health Checks** on instances
- 🔒 Supports **SSL/TLS Termination**
- 📈 Integrates with **Auto Scaling**
- 🌍 Distributes traffic across multiple **Availability Zones (AZs)**

---

# ⭐ Easy to Remember

- **ALB** → Best for **Web Applications and APIs** (HTTP/HTTPS).
- **NLB** → Best for **High-Speed Applications** (TCP/UDP).
- **GWLB** → Best for **Network Security Appliances** (Firewalls, IDS, IPS).
- **CLB** → Used for **Older (Legacy) AWS Applications**.
---

# 📊 Difference Between AWS Load Balancers

| Load Balancer | OSI Layer | Supports | Best For |
|---------------|-----------|----------|----------|
| ⚖️ **Application Load Balancer (ALB)** | Layer 7 | HTTP, HTTPS, WebSocket, gRPC | Web Applications, APIs, Microservices |
| ⚡ **Network Load Balancer (NLB)** | Layer 4 | TCP, UDP, TLS | High-performance and Low-Latency Applications |
| 🛡️ **Gateway Load Balancer (GWLB)** | Layer 3 | IP (GENEVE) | Firewalls, IDS, IPS, Security Appliances |
| 📦 **Classic Load Balancer (CLB)** | Layer 4 & 7 | HTTP, HTTPS, TCP, SSL | Legacy (Older) Applications |

---
