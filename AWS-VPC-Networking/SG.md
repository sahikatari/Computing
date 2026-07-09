# 🔐 AWS Security Groups

> Instance-level virtual firewall for AWS resources.

## 📖 What is a Security Group?

A **Security Group (SG)** is a stateful virtual firewall that controls inbound and outbound traffic for EC2 instances and other AWS resources.

## Features

- Stateful
- Allow Rules Only
- Attached to EC2, RDS, ALB, Lambda (ENI), etc.
- Multiple Security Groups can be attached to one instance

## Rules

### Inbound Rules

Traffic entering an instance.

Example:

| Type | Port | Source |
|------|------|--------|
| SSH | 22 | My IP |
| HTTP | 80 | 0.0.0.0/0 |
| HTTPS | 443 | 0.0.0.0/0 |

### Outbound Rules

Traffic leaving an instance.

By default:

- Allow All Outbound

## Security Group vs NACL

| Security Group | NACL |
|---------------|------|
| Stateful | Stateless |
| Instance Level | Subnet Level |
| Allow Rules Only | Allow & Deny Rules |

## Summary

- Acts as a virtual firewall.
- Controls traffic to AWS resources.
- Stateful and more secure than traditional firewalls.
