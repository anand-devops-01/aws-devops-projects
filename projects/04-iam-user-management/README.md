# Project 04 - IAM User and Role Management

## Overview

This project demonstrates how to create IAM users, groups, roles, and policies to securely manage access to AWS resources.

---

# AWS Services Used

- IAM

---

# Architecture

```
AWS Account
      │
      ▼
     IAM
 ┌─────────────┐
 │ Users       │
 │ Groups      │
 │ Roles       │
 │ Policies    │
 └─────────────┘
      │
      ▼
AWS Resources
```

---

# Prerequisites

- AWS Account
- IAM Administrator Access

---

# Step 1 - Create IAM User

- Open AWS Console
- Go to IAM
- Select Users
- Click Create User
- Enter username
- Create user

---

# Step 2 - Create IAM Group

Example Group:

- Developers
- DevOps
- Administrators

Attach required policies.

---

# Step 3 - Add User to Group

Assign users to the appropriate IAM group.

---

# Step 4 - Create IAM Policy

Example Permissions:

- EC2 Read Only
- S3 Full Access
- CloudWatch Read Only

Attach the policy to users, groups, or roles.

---

# Step 5 - Create IAM Role

Example Roles:

- EC2 Role
- Lambda Role
- EKS Role

Attach required permissions.

---

# Step 6 - Enable MFA

Enable Multi-Factor Authentication for:

- Root Account
- IAM Users

---

# Step 7 - Rotate Credentials

Regularly rotate:

- Passwords
- Access Keys
- Secret Keys

Delete unused credentials.

---

# IAM Best Practices

- Never use the root account for daily tasks.
- Follow the Principle of Least Privilege.
- Use IAM Roles instead of storing long-term credentials.
- Enable MFA for privileged accounts.
- Regularly review and remove unused users, roles, and policies.

---

# Skills Learned

- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- MFA
- AWS Security

---

# Conclusion

IAM is the foundation of AWS security. Proper identity and access management helps protect cloud resources and ensures users have only the permissions they require.