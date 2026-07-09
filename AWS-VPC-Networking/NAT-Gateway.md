# 🌍 NAT Gateway

> Enable Private Subnets to access the Internet securely.

## 📖 What is a NAT Gateway?

A **NAT (Network Address Translation) Gateway** allows resources in a **Private Subnet** to access the Internet without exposing them to inbound Internet traffic.

## Features

- Outbound Internet only
- Managed AWS Service
- Highly Available
- Requires an Elastic IP

## Architecture

Internet

↓

Internet Gateway

↓

Public Subnet

↓

NAT Gateway

↓

Private Subnet

## Route Table

| Destination | Target |
|-------------|--------|
| 0.0.0.0/0 | NAT Gateway |

## Common Uses

- Software Updates
- Package Installation
- Download Dependencies

## Summary

- Used by Private Subnets.
- Blocks unsolicited inbound traffic.
