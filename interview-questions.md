# AWS DevOps Interview Questions

## AWS Basics

### 1. What is AWS?

Amazon Web Services (AWS) is a cloud computing platform that provides on-demand services such as compute, storage, networking, databases, and security.

---

### 2. What are the main AWS service categories?

- Compute
- Storage
- Networking
- Database
- Security
- Monitoring
- Containers
- Analytics

---

### 3. What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) provides scalable virtual servers in the cloud.

---

### 4. What is Amazon S3?

Amazon S3 (Simple Storage Service) is an object storage service used for storing files, backups, logs, and hosting static websites.

---

### 5. What is IAM?

IAM (Identity and Access Management) controls authentication and authorization for AWS resources.

---

## Networking

### 6. What is a VPC?

A Virtual Private Cloud (VPC) is an isolated virtual network where AWS resources are deployed.

---

### 7. Difference between Security Group and NACL?

| Security Group | NACL |
|---------------|------|
| Instance Level | Subnet Level |
| Stateful | Stateless |
| Allow Rules Only | Allow & Deny Rules |

---

### 8. What is an Internet Gateway?

An Internet Gateway allows communication between a VPC and the internet.

---

### 9. What is a NAT Gateway?

A NAT Gateway allows private subnet resources to access the internet without exposing them publicly.

---

## Compute

### 10. What are EC2 Instance Types?

Examples:

- General Purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized

---

### 11. What is Auto Scaling?

Auto Scaling automatically adds or removes EC2 instances based on demand.

---

### 12. What is an AMI?

An Amazon Machine Image (AMI) is a template used to launch EC2 instances.

---

## Storage

### 13. What is an EBS Volume?

Elastic Block Store (EBS) provides persistent block storage for EC2 instances.

---

### 14. Difference between EBS and S3?

| EBS | S3 |
|-----|----|
| Block Storage | Object Storage |
| Attached to EC2 | Accessible via API |
| Low Latency | Highly Scalable |

---

## Database

### 15. What is Amazon RDS?

Amazon RDS is a managed relational database service.

Supported databases include:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- SQL Server

---

## Monitoring

### 16. What is CloudWatch?

CloudWatch monitors AWS resources using metrics, logs, alarms, and dashboards.

---

### 17. What is CloudTrail?

CloudTrail records AWS API activity for auditing and security.

---

## DevOps

### 18. What is Infrastructure as Code (IaC)?

IaC is the practice of provisioning infrastructure using code instead of manual configuration.

Example Tool:

- Terraform

---

### 19. What is CI/CD?

CI (Continuous Integration) automates code integration and testing.

CD (Continuous Delivery/Deployment) automates software releases.

---

### 20. Which DevOps tools are commonly used with AWS?

- Git
- GitHub
- Docker
- Kubernetes
- Terraform
- Jenkins
- GitHub Actions
- Ansible

---

## Containers

### 21. What is Amazon ECR?

Amazon Elastic Container Registry stores Docker images.

---

### 22. What is Amazon ECS?

Amazon ECS is a managed container orchestration service.

---

### 23. What is Amazon EKS?

Amazon EKS is a managed Kubernetes service.

---

## Security

### 24. What is the Principle of Least Privilege?

Grant users only the permissions required to perform their tasks.

---

### 25. Why should MFA be enabled?

Multi-Factor Authentication adds an extra layer of account security.

---

# Bonus Interview Tips

- Understand AWS core services.
- Practice launching EC2 and creating S3 buckets.
- Learn IAM policies and roles.
- Understand VPC networking.
- Practice Terraform basics.
- Learn Docker and Kubernetes fundamentals.
- Be comfortable explaining CI/CD pipelines.

---

# Conclusion

These questions cover common AWS and DevOps interview topics. Continue practicing hands-on projects to strengthen your understanding and prepare for real-world scenarios.