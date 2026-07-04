# Project 06 - Auto Scaling Group (ASG)

## Overview

This project demonstrates how to configure an AWS Auto Scaling Group (ASG) to automatically increase or decrease the number of EC2 instances based on application demand.

Auto Scaling improves availability, fault tolerance, and cost optimization.

---

# AWS Services Used

- Amazon EC2
- Auto Scaling Group
- Launch Template
- Application Load Balancer
- CloudWatch

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
     Auto Scaling Group (ASG)
          │
   ┌──────┴──────┐
   ▼             ▼
EC2 Instance 1  EC2 Instance 2
       │
       ▼
Amazon CloudWatch
```

---

# Prerequisites

- AWS Account
- Existing VPC
- Public Subnets
- Application Load Balancer
- EC2 Launch Template

---

# Step 1 - Create Launch Template

Go to:

EC2 → Launch Templates

Configure:

- Amazon Linux 2023
- t2.micro
- Security Group
- Key Pair
- User Data (Optional)

---

# Step 2 - Create Auto Scaling Group

Navigate to:

EC2 → Auto Scaling Groups

Choose:

- Launch Template
- VPC
- Public Subnets

---

# Step 3 - Attach Load Balancer

Select the existing Target Group created for the Application Load Balancer.

---

# Step 4 - Configure Scaling

Example:

Minimum Capacity:

2

Desired Capacity:

2

Maximum Capacity:

5

---

# Step 5 - Configure Scaling Policy

Example Policy:

Scale Out

- CPU > 70%

Scale In

- CPU < 30%

---

# Step 6 - Monitor

Use Amazon CloudWatch to monitor:

- CPU Utilization
- Network Traffic
- Instance Count

---

# Step 7 - Test Auto Scaling

Generate traffic using tools such as:

- Apache Bench (ab)
- hey
- JMeter

Observe new EC2 instances launching automatically.

---

# Benefits

- Automatic Scaling
- High Availability
- Fault Tolerance
- Cost Optimization

---

# Skills Learned

- Launch Templates
- Auto Scaling Groups
- Scaling Policies
- CloudWatch Metrics
- High Availability

---

# Best Practices

- Use Launch Templates instead of Launch Configurations.
- Distribute instances across multiple Availability Zones.
- Configure health checks for applications.
- Monitor scaling events using CloudWatch.

---

# Conclusion

Auto Scaling Groups automatically adjust application capacity based on demand, ensuring high availability while optimizing infrastructure costs.