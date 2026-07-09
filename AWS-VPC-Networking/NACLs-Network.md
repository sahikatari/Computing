# 🚧 AWS Network ACLs (NACL)

> A beginner-friendly guide to understanding **Network Access Control Lists (NACLs)** in AWS VPC.

---

# 📚 Table of Contents

- What is a Network ACL?
- Why Use a NACL?
- How NACL Works
- NACL Rules
- Inbound & Outbound Rules
- Stateless Nature
- Default vs Custom NACL
- Security Group vs NACL
- Summary

---

# 🚧 What is a Network ACL?

A **Network Access Control List (NACL)** is a **subnet-level firewall** that controls inbound and outbound traffic for one or more subnets in a VPC.

Unlike Security Groups, NACLs can **allow** or **deny** traffic based on rules.

> **Simple Definition:**  
> A NACL acts as the first line of defense for an entire subnet.

---

# ❓ Why Use a NACL?

Network ACLs help you:

- Protect an entire subnet
- Control incoming and outgoing traffic
- Allow or deny specific IP addresses
- Add an extra layer of network security
- Block unwanted traffic before it reaches instances

---

# ⚙️ How NACL Works

A NACL evaluates traffic based on **rule numbers**, starting from the **lowest number**.

- The first matching rule is applied.
- If no rule matches, the traffic is denied.

Example:

| Rule # | Type | Protocol | Port | Source | Action |
|--------|------|----------|------|--------|--------|
| 100 | HTTP | TCP | 80 | 0.0.0.0/0 | ALLOW |
| 110 | HTTPS | TCP | 443 | 0.0.0.0/0 | ALLOW |
| 120 | SSH | TCP | 22 | My IP | ALLOW |
| * | ALL | ALL | ALL | 0.0.0.0/0 | DENY |

---

# 🔄 Stateless Firewall

Network ACLs are **Stateless**.

This means:

- Incoming traffic must be explicitly allowed.
- Outgoing response traffic must also be explicitly allowed.

Example:

```
Client
   │
   ▼
Inbound Rule → ALLOW
   │
EC2 Instance
   │
Outbound Rule → ALLOW
   ▼
Client
```

If the outbound rule is missing, the response is blocked.

---

# 📋 Default vs Custom NACL

| Feature | Default NACL | Custom NACL |
|----------|--------------|-------------|
| Inbound Rules | Allow All | User Defined |
| Outbound Rules | Allow All | User Defined |
| Allow Rules | ✅ | ✅ |
| Deny Rules | ❌ (Implicit only) | ✅ |
| Best For | Testing | Production |

---

# 🔐 Security Group vs NACL

| Feature | Security Group | Network ACL |
|----------|---------------|-------------|
| Level | Instance | Subnet |
| Stateful | ✅ Yes | ❌ No |
| Allow Rules | ✅ Yes | ✅ Yes |
| Deny Rules | ❌ No | ✅ Yes |
| Rule Evaluation | All Rules | Rule Number Order |
| Default Behavior | Deny Inbound, Allow Outbound | Allow All (Default NACL) |

---

# 🏗️ Example Architecture

```text
                  Internet
                      │
              Internet Gateway
                      │
        ┌─────────────────────────┐
        │     Public Subnet        │
        │     Network ACL          │
        │  Allow HTTP/HTTPS/SSH    │
        └─────────────┬────────────┘
                      │
                 EC2 Instance
```

---


# 📝 Summary

- Network ACLs are **subnet-level firewalls**.
- They are **stateless**, requiring separate inbound and outbound rules.
- Rules are processed in **ascending rule number** order.
- NACLs support both **ALLOW** and **DENY** actions.
- Use NACLs along with Security Groups for layered security.

---
