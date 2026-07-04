# AWS Services Overview

## What is AWS?

Amazon Web Services (AWS) is the world's leading cloud computing platform that provides on-demand infrastructure and cloud services.

AWS helps organizations build, deploy, and scale applications without managing physical hardware.

---

# Core AWS Services

## 1. Amazon EC2

Elastic Compute Cloud (EC2) provides virtual servers in the cloud.

### Use Cases

- Hosting websites
- Running applications
- CI/CD Servers
- Jenkins Server

---

## 2. Amazon S3

Simple Storage Service (S3) is an object storage service.

### Use Cases

- Static website hosting
- Backup
- File storage
- Log storage

---

## 3. IAM

Identity and Access Management (IAM) controls access to AWS resources.

### Features

- Users
- Groups
- Roles
- Policies

---

## 4. Amazon VPC

Virtual Private Cloud (VPC) provides isolated networking in AWS.

Components:

- VPC
- Subnets
- Route Tables
- Internet Gateway
- NAT Gateway
- Security Groups
- NACL

---

## 5. Amazon RDS

Managed relational database service.

Supported databases:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- SQL Server

---

## 6. Elastic Load Balancer (ELB)

Distributes incoming traffic across multiple EC2 instances.

Types:

- Application Load Balancer
- Network Load Balancer
- Gateway Load Balancer

---

## 7. Auto Scaling

Automatically increases or decreases EC2 instances based on demand.

Benefits:

- High Availability
- Cost Optimization

---

## 8. CloudWatch

Monitoring service for AWS resources.

Features:

- Metrics
- Logs
- Dashboards
- Alarms

---

## 9. Route 53

AWS DNS service.

Supports:

- Domain Registration
- DNS Routing
- Health Checks

---

## 10. ECR

Elastic Container Registry stores Docker images.

---

## 11. ECS

Elastic Container Service manages Docker containers.

---

## 12. EKS

Elastic Kubernetes Service provides managed Kubernetes clusters.

---

## 13. Lambda

Serverless compute service.

No server management required.

---

## 14. SNS

Simple Notification Service.

Used for:

- Email Notifications
- SMS
- Event Notifications

---

## 15. SQS

Simple Queue Service.

Used for asynchronous messaging between applications.

---

# AWS DevOps Workflow

Developer

↓

GitHub

↓

GitHub Actions / Jenkins

↓

Docker Build

↓

Amazon ECR

↓

Amazon EKS / ECS / EC2

↓

CloudWatch Monitoring

---

# Conclusion

AWS offers a wide range of cloud services that enable scalable, secure, and cost-effective application deployment. Learning these core services is essential for every DevOps Engineer.