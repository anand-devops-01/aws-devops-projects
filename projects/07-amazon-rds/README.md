# Project 07 - Amazon RDS (MySQL Database)

## Overview

This project demonstrates how to create and manage a MySQL database using Amazon RDS. Amazon RDS is a managed database service that automates backups, patching, monitoring, and scaling.

---

# AWS Services Used

- Amazon RDS
- Amazon EC2
- Security Groups
- Amazon VPC

---

# Architecture

```
               Internet
                   │
                   ▼
              EC2 Instance
                   │
          MySQL Port (3306)
                   │
                   ▼
              Amazon RDS
```

---

# Prerequisites

- AWS Account
- Existing VPC
- EC2 Instance
- Security Groups

---

# Step 1 - Create Database

Go to:

AWS Console → RDS → Create Database

Choose:

- Standard Create
- MySQL
- Free Tier (for practice)

---

# Step 2 - Configure Database

Example:

Database Name:

```
devopsdb
```

Master Username:

```
admin
```

Create a secure password.

---

# Step 3 - Network Configuration

- Select your VPC.
- Choose the appropriate subnet group.
- Disable Public Access for production environments.
- Attach the correct Security Group.

---

# Step 4 - Configure Security Group

Allow MySQL traffic:

| Type | Port | Source |
|------|------|--------|
| MySQL/Aurora | 3306 | EC2 Security Group |

---

# Step 5 - Connect from EC2

Install MySQL client:

Amazon Linux:

```bash
sudo yum install mariadb105 -y
```

Ubuntu:

```bash
sudo apt update
sudo apt install mysql-client -y
```

Connect:

```bash
mysql -h <RDS-ENDPOINT> -u admin -p
```

---

# Step 6 - Create Database

```sql
CREATE DATABASE company;
```

Use Database:

```sql
USE company;
```

Create Table:

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    department VARCHAR(50)
);
```

Insert Data:

```sql
INSERT INTO employees VALUES
(1,'Anand','DevOps');
```

Query Data:

```sql
SELECT * FROM employees;
```

---

# Skills Learned

- Amazon RDS
- MySQL
- Security Groups
- Database Connectivity
- SQL Basics

---

# Best Practices

- Enable automated backups.
- Enable Multi-AZ for production.
- Use strong passwords.
- Restrict database access using Security Groups.
- Enable monitoring with Amazon CloudWatch.

---

# Conclusion

Amazon RDS simplifies database administration by handling backups, updates, and scaling, allowing you to focus on application development.