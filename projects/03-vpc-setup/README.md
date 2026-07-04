# Project 03 - Build a Custom VPC in AWS

## Overview

This project demonstrates how to create a custom Virtual Private Cloud (VPC) with public and private subnets for secure and scalable application deployment.

---

# AWS Services Used

- Amazon VPC
- Subnets
- Route Tables
- Internet Gateway
- NAT Gateway
- Security Groups

---

# Architecture

```
                 Internet
                     │
                     ▼
            Internet Gateway
                     │
             ┌───────────────┐
             │      VPC      │
             └───────────────┘
               │           │
               ▼           ▼
        Public Subnet   Private Subnet
               │           │
            EC2(Web)    EC2(App/DB)
```

---

# Prerequisites

- AWS Account
- IAM User
- Basic Networking Knowledge

---

# Step 1 - Create VPC

- CIDR Block: 10.0.0.0/16
- Enable DNS Hostnames

---

# Step 2 - Create Public Subnet

Example:

- 10.0.1.0/24

---

# Step 3 - Create Private Subnet

Example:

- 10.0.2.0/24

---

# Step 4 - Create Internet Gateway

- Create Internet Gateway
- Attach it to the VPC

---

# Step 5 - Create Route Tables

Public Route Table

```
Destination    Target

0.0.0.0/0      Internet Gateway
```

Associate the public subnet with this route table.

---

# Step 6 - Create NAT Gateway

Deploy NAT Gateway in the public subnet.

Purpose:

- Allow private subnet instances to access the internet for updates without being publicly reachable.

---

# Step 7 - Configure Private Route Table

```
Destination    Target

0.0.0.0/0      NAT Gateway
```

Associate the private subnet with this route table.

---

# Step 8 - Launch EC2 Instances

Public Subnet:

- Bastion Host
- Web Server

Private Subnet:

- Application Server
- Database Server

---

# Skills Learned

- Amazon VPC
- CIDR Blocks
- Public & Private Subnets
- Internet Gateway
- NAT Gateway
- Route Tables
- Network Design

---

# Best Practices

- Use private subnets for databases.
- Restrict SSH access with Security Groups.
- Avoid placing sensitive workloads in public subnets.
- Use separate route tables for public and private traffic.

---

# Conclusion

A well-designed VPC provides secure networking, proper traffic routing, and a scalable foundation for AWS applications.