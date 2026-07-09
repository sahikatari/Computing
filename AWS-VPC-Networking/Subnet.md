# 🌐 AWS Subnets


## 📖 What is a Subnet?

A **Subnet** is a logical subdivision of a VPC. Each subnet belongs to a **single Availability Zone (AZ)** and has its own CIDR block.

### Why Use Subnets?

- Separate public and private resources
- Improve security
- Better network organization
- High Availability across AZs

## Types of Subnets

### 🌍 Public Subnet

- Route to Internet Gateway (IGW)
- Can have Public IP
- Used for:
  - Web Servers
  - Load Balancers
  - Bastion Hosts

### 🔒 Private Subnet

- No direct Internet access
- Uses NAT Gateway for outbound traffic
- Used for:
  - Application Servers
  - Databases

## Example

| Subnet | CIDR |
|---------|------|
| Public-1 | 10.0.1.0/24 |
| Public-2 | 10.0.2.0/24 |
| Private-1 | 10.0.3.0/24 |
| Private-2 | 10.0.4.0/24 |

## AWS Rules

- Subnet CIDR must be within the VPC CIDR.
- Subnets cannot overlap.
- One subnet belongs to one AZ.
- AWS reserves 5 IPs per subnet.

## Summary

- Subnets divide a VPC into smaller networks.
- Public Subnets connect to the Internet.
- Private Subnets protect internal resources.
