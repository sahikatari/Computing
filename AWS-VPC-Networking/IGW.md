# 🌍 Internet Gateway (IGW)

> Connect your VPC to the Internet.

## 📖 What is an Internet Gateway?

An **Internet Gateway (IGW)** enables communication between a VPC and the Internet.

It is attached to a VPC.

## Features

- Allows inbound traffic
- Allows outbound traffic
- Highly Available
- Horizontally Scaled

## Requirements

- Attach IGW to VPC
- Public Subnet Route Table must contain:

| Destination | Target |
|-------------|--------|
| 0.0.0.0/0 | IGW |

## Used For

- Public EC2 Instances
- Load Balancers
- Bastion Hosts

## Summary

- Provides Internet connectivity.
- Required for Public Subnets.
