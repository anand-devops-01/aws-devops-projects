# Project 05 - Application Load Balancer (ALB)

## Overview

This project demonstrates how to configure an AWS Application Load Balancer (ALB) to distribute incoming HTTP traffic across multiple EC2 instances.

This setup improves application availability, scalability, and fault tolerance.

---

# AWS Services Used

- Amazon EC2
- Application Load Balancer (ALB)
- Target Groups
- Security Groups

---

# Architecture

```
               Internet
                   │
                   ▼
      Application Load Balancer
                   │
         ┌─────────┴─────────┐
         ▼                   ▼
     EC2 Instance 1      EC2 Instance 2
        (Nginx)             (Nginx)
```

---

# Prerequisites

- AWS Account
- Two EC2 Instances
- Same VPC
- Security Groups

---

# Step 1 - Launch EC2 Instances

Launch two EC2 instances.

Example:

- Web-Server-1
- Web-Server-2

Install Nginx on both servers.

---

# Step 2 - Create Target Group

Navigate to:

EC2 → Target Groups

Configure:

- Target Type: Instances
- Protocol: HTTP
- Port: 80

Register both EC2 instances.

---

# Step 3 - Create Application Load Balancer

Go to:

EC2 → Load Balancers

Choose:

- Application Load Balancer
- Internet Facing
- IPv4

Select your VPC and Public Subnets.

---

# Step 4 - Configure Listener

Protocol:

HTTP

Port:

80

Forward traffic to the Target Group.

---

# Step 5 - Configure Security Group

Allow:

- HTTP (80)
- HTTPS (443)
- SSH (22) (only from trusted IPs)

---

# Step 6 - Test Load Balancer

Copy the ALB DNS Name.

Open:

```
http://ALB-DNS-Name
```

Refresh the page multiple times to verify traffic reaches different EC2 instances.

---

# Benefits

- High Availability
- Fault Tolerance
- Traffic Distribution
- Scalability

---

# Skills Learned

- Application Load Balancer
- Target Groups
- Health Checks
- EC2 Integration
- High Availability

---

# Best Practices

- Enable HTTPS using ACM certificates.
- Configure health checks for application endpoints.
- Deploy instances across multiple Availability Zones.
- Monitor ALB metrics with Amazon CloudWatch.

---

# Conclusion

Application Load Balancers improve the reliability and scalability of web applications by distributing traffic across multiple healthy EC2 instances.