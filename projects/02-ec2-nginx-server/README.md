# Project 02 - Deploy Nginx Web Server on Amazon EC2

## Overview

This project demonstrates how to launch an Amazon EC2 instance, connect using SSH, install Nginx, and host a web server.

---

# AWS Services Used

- Amazon EC2
- Security Groups
- IAM

---

# Architecture

```
User
   │
   ▼
Internet
   │
   ▼
Security Group
   │
   ▼
Amazon EC2
   │
   ▼
Nginx Web Server
```

---

# Prerequisites

- AWS Account
- EC2 Key Pair
- Basic Linux Commands

---

# Step 1 – Launch EC2 Instance

- Open AWS Console
- Go to EC2
- Launch Instance
- Choose Amazon Linux 2023 or Ubuntu
- Select t2.micro (Free Tier)
- Create or Select Key Pair
- Allow HTTP (80)
- Allow SSH (22)

Launch the instance.

---

# Step 2 – Connect to EC2

```bash
ssh -i my-key.pem ec2-user@<Public-IP>
```

Ubuntu:

```bash
ssh -i my-key.pem ubuntu@<Public-IP>
```

---

# Step 3 – Update Packages

Amazon Linux:

```bash
sudo yum update -y
```

Ubuntu:

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Step 4 – Install Nginx

Amazon Linux:

```bash
sudo yum install nginx -y
```

Ubuntu:

```bash
sudo apt install nginx -y
```

---

# Step 5 – Start Nginx

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

# Step 6 – Verify Status

```bash
sudo systemctl status nginx
```

---

# Step 7 – Test Website

Open:

```
http://<EC2-Public-IP>
```

You should see the default Nginx welcome page.

---

# Skills Learned

- Amazon EC2
- SSH
- Security Groups
- Linux Administration
- Nginx Installation

---

# Best Practices

- Use IAM Roles instead of long-term credentials.
- Restrict SSH access to trusted IPs.
- Keep the operating system updated.
- Enable HTTPS using a reverse proxy or certificate service when exposing applications publicly.

---

# Conclusion

This project demonstrates the basic deployment of a web server on AWS using Amazon EC2 and Nginx, providing a foundation for hosting web applications.