# Project 09 - Provision AWS EC2 using Terraform

## Overview

This project demonstrates how to provision AWS infrastructure using Terraform. It creates an EC2 instance in AWS using Infrastructure as Code (IaC).

---

# AWS Services Used

- Amazon EC2
- Amazon VPC
- Security Groups
- IAM

---

# Tools Used

- Terraform
- AWS CLI

---

# Project Structure

```
terraform/

├── provider.tf
├── variables.tf
├── main.tf
└── outputs.tf
```

---

# Prerequisites

- AWS Account
- AWS CLI Configured
- Terraform Installed

Verify installation:

```bash
terraform version
```

---

# Step 1 - Configure AWS CLI

```bash
aws configure
```

Provide:

- Access Key
- Secret Key
- Region

---

# Step 2 - Initialize Terraform

```bash
terraform init
```

---

# Step 3 - Review Execution Plan

```bash
terraform plan
```

---

# Step 4 - Deploy Infrastructure

```bash
terraform apply
```

Type:

```
yes
```

---

# Step 5 - Verify Resources

Go to AWS Console.

EC2 → Instances

Verify the instance has been created.

---

# Step 6 - Destroy Infrastructure

```bash
terraform destroy
```

---

# Skills Learned

- Infrastructure as Code
- Terraform
- AWS EC2
- AWS Provider
- Resource Management

---

# Best Practices

- Store state securely.
- Use variables.
- Keep reusable modules.
- Never hardcode secrets.

---

# Conclusion

Terraform enables consistent, repeatable, and automated infrastructure deployment on AWS.