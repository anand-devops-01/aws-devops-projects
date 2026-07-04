# Project 08 - CloudWatch Monitoring & Alerts

## Overview

This project demonstrates how to monitor AWS resources using Amazon CloudWatch. It includes metrics, logs, dashboards, and alarms for proactive monitoring.

---

# AWS Services Used

- Amazon CloudWatch
- Amazon EC2
- Amazon SNS

---

# Architecture

```
                EC2 Instance
                     │
                     ▼
             Amazon CloudWatch
             ├───────────────┐
             │               │
             ▼               ▼
         Metrics         CloudWatch Logs
             │
             ▼
       CloudWatch Alarm
             │
             ▼
         Amazon SNS
             │
             ▼
        Email Notification
```

---

# Prerequisites

- AWS Account
- EC2 Instance
- IAM Permissions

---

# Step 1 - Launch EC2

Launch an EC2 instance if one is not already running.

---

# Step 2 - Open CloudWatch

Navigate to:

AWS Console → CloudWatch

---

# Step 3 - View Metrics

Monitor:

- CPU Utilization
- Disk Read/Write
- Network In
- Network Out
- Status Checks

---

# Step 4 - Create Alarm

Example:

Metric:

CPU Utilization

Condition:

Greater than 70%

Duration:

5 Minutes

---

# Step 5 - Create SNS Topic

Go to:

SNS → Topics

Create Topic:

```
devops-alerts
```

Subscribe using your email address.

---

# Step 6 - Attach SNS to Alarm

Select the SNS Topic while creating the alarm.

CloudWatch will send an email whenever the alarm is triggered.

---

# Step 7 - Install CloudWatch Agent (Optional)

Amazon Linux

```bash
sudo yum install amazon-cloudwatch-agent -y
```

Ubuntu

```bash
sudo apt install amazon-cloudwatch-agent -y
```

---

# Step 8 - Create Dashboard

Create a dashboard displaying:

- CPU Usage
- Memory Usage
- Disk Usage
- Network Traffic

---

# Skills Learned

- CloudWatch Metrics
- CloudWatch Logs
- CloudWatch Alarms
- SNS Notifications
- Monitoring

---

# Best Practices

- Monitor CPU, Memory, and Disk usage.
- Configure alarms for critical metrics.
- Use dashboards for centralized monitoring.
- Review logs regularly for troubleshooting.

---

# Conclusion

Amazon CloudWatch provides real-time monitoring, logging, and alerting capabilities, helping maintain application performance and infrastructure health.