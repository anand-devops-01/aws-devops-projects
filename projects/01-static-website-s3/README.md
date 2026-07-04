# Project 01 - Static Website Hosting on Amazon S3

## Overview

This project demonstrates how to host a static website using Amazon S3.

It is one of the easiest and most popular AWS beginner projects.

---

# AWS Services Used

- Amazon S3
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
Amazon S3 Bucket
   │
   ▼
Static Website
```

---

# Prerequisites

- AWS Account
- IAM User with S3 permissions
- HTML, CSS, and JavaScript files

---

# Step 1: Create an S3 Bucket

- Open AWS Console
- Go to Amazon S3
- Click **Create Bucket**
- Enter a unique bucket name
- Select your preferred AWS Region
- Create the bucket

---

# Step 2: Upload Website Files

Upload:

- index.html
- style.css
- script.js
- images

---

# Step 3: Enable Static Website Hosting

Navigate to:

Properties → Static Website Hosting

Choose:

- Enable
- Index document: index.html

Save the configuration.

---

# Step 4: Configure Bucket Permissions

Disable Block Public Access (only for learning purposes).

Attach a bucket policy that allows public read access.

---

# Step 5: Test the Website

Open the S3 Website Endpoint in your browser.

Verify that your website loads successfully.

---

# Folder Structure

```
website/

├── index.html
├── style.css
├── script.js
└── images/
```

---

# Best Practices

- Enable Versioning
- Enable Server-Side Encryption
- Use HTTPS with CloudFront
- Restrict permissions using IAM
- Enable Access Logging

---

# Skills Learned

- Amazon S3
- Static Website Hosting
- Bucket Policies
- IAM Permissions
- Object Storage

---

# Conclusion

This project introduces the fundamentals of AWS storage and website hosting. It provides a strong foundation for learning more advanced AWS services.