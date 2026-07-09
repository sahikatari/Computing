# 🛣️ AWS Route Tables

> Learn how Route Tables control network traffic inside a VPC.

## 📖 What is a Route Table?

A **Route Table** contains rules (routes) that determine where network traffic is directed.

Every subnet must be associated with a Route Table.

## Components

- Destination
- Target

Example:

| Destination | Target |
|-------------|--------|
| 10.0.0.0/16 | Local |
| 0.0.0.0/0 | Internet Gateway |

## Types

### Main Route Table

- Created automatically
- Default for all subnets

### Custom Route Table

- Created by users
- Used for Public and Private Subnets

## Common Targets

- Local
- Internet Gateway (IGW)
- NAT Gateway
- VPC Peering
- Transit Gateway

## Summary

- Controls traffic flow.
- Every subnet uses one Route Table.
- Routes determine where packets are sent.
