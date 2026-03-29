# Cloud Computing Notes (IAM, Policies, RDS)


# 🔐 1. IAM (Identity and Access Management)

## 📌 Definition

IAM is a service that allows you to **securely control access** to cloud resources. It helps you decide:

* **Who** can access resources
* **What** actions they can perform
* **Which** resources they can access

---

## 🧠 Core Components of IAM

### 1. Users

* Represents an individual (developer, admin, app)
* Has **credentials** (password, access key)

👉 Example:

* Aditya → IAM User with login access

---

### 2. Groups

* Collection of users
* Permissions assigned at group level

👉 Example:

* "Developers" group → Read-only access to database

---

### 3. Roles

* Temporary access (no permanent credentials)
* Used by services, apps, or external users

👉 Example:

* EC2 instance accessing S3 using IAM Role

---

### 4. Policies

* JSON documents defining permissions
* Attached to users, groups, or roles

---

## 🔑 IAM Key Concepts

### ✔ Authentication vs Authorization

| Type           | Meaning          |
| -------------- | ---------------- |
| Authentication | Who are you?     |
| Authorization  | What can you do? |

---

### ✔ Principle of Least Privilege

* Give **minimum required permissions**
* Reduces security risks

---

### ✔ Multi-Factor Authentication (MFA)

* Extra layer of security (OTP, authenticator app)

---

### ✔ Access Keys

* Used for programmatic access (CLI, API)
* Consists of:

  * Access Key ID
  * Secret Access Key

---

## 🔥 IAM Best Practices

* Never use root account daily
* Enable MFA for all users
* Rotate access keys regularly
* Use roles instead of hardcoding credentials
* Follow least privilege principle

---

# 📜 2. IAM Policies

## 📌 Definition

Policies are **JSON-based permission documents** that define what actions are allowed or denied.

---

## 🧾 Structure of a Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::example-bucket/*"
    }
  ]
}
```

---

## 🧠 Policy Elements

### 1. Effect

* `Allow` → Permission granted
* `Deny` → Permission blocked

---

### 2. Action

* Specifies allowed operations
* Example:

  * `s3:GetObject`
  * `ec2:StartInstances`

---

### 3. Resource

* Defines the target resource
* Example:

  * S3 bucket
  * EC2 instance

---

### 4. Condition (Optional)

* Adds restrictions

👉 Example:

```json
"Condition": {
  "IpAddress": {
    "aws:SourceIp": "192.168.1.0/24"
  }
}
```

---

## 🔄 Types of Policies

### 1. Managed Policies

* Predefined or reusable
* Easier to manage

---

### 2. Inline Policies

* Attached directly to one entity
* Not reusable

---

## ⚖️ Policy Evaluation Logic

1. Default → Deny everything
2. If explicitly allowed → Allow
3. If explicitly denied → Deny (overrides allow)

---

## 🔐 Example Scenario

👉 Goal:

* Allow user to read S3 but not delete

✔ Allow:

```json
"s3:GetObject"
```

❌ Deny:

```json
"s3:DeleteObject"
```

---

# 🗄️ 3. RDS (Relational Database Service)

## 📌 Definition

RDS is a managed service that allows you to **set up, operate, and scale relational databases** in the cloud.

---

## 🧠 Key Features

### ✔ Managed Service

* No need to handle:

  * OS updates
  * Patching
  * Backups

---

### ✔ Automated Backups

* Daily backups + transaction logs

---

### ✔ Scalability

* Vertical scaling (increase CPU/RAM)
* Read replicas for scaling reads

---

### ✔ High Availability (Multi-AZ)

* Data replicated across availability zones
* Automatic failover

---

## 🧾 Supported Databases

* MySQL
* PostgreSQL
* MariaDB
* Oracle
* SQL Server

---

## 🔧 RDS Components

### 1. DB Instance

* Actual database server

---

### 2. DB Engine

* Type of database (MySQL, PostgreSQL)

---

### 3. Storage

* SSD-backed storage

---

### 4. Endpoint

* URL to connect to database

---

## 🔐 Security in RDS

* IAM authentication (optional)
* Security groups (firewall)
* Encryption at rest and in transit

---

## ⚙️ RDS Deployment Types

### 1. Single AZ

* One instance
* Lower cost
* No failover

---

### 2. Multi-AZ

* Primary + standby instance
* Automatic failover

---

### 3. Read Replicas

* Copies of DB for read scaling

---

## 🔄 Backup Types

### ✔ Automated Backups

* Retention period (1–35 days)

### ✔ Manual Snapshots

* Stored until deleted

---

## ⚡ Example Workflow

1. Create RDS instance (MySQL)
2. Configure storage, CPU, RAM
3. Set username/password
4. Connect using endpoint
5. Run queries

---

## 🚀 Advantages of RDS

* Easy to use
* Fully managed
* Highly scalable
* Secure
* Cost-efficient

---

## ⚠️ Limitations

* Less control compared to self-hosted DB
* Costs increase with scaling
* Limited OS-level access

---

# 🧩 Quick Revision Summary

## IAM

* Controls access
* Users, Groups, Roles, Policies

## Policies

* JSON permission documents
* Allow / Deny logic

## RDS

* Managed relational DB
* Scalable, secure, automated

---

# 🎯 Exam-Oriented Key Points

* IAM = Security backbone
* Policy = Permission logic (JSON)
* RDS = Managed SQL database service
* Least privilege principle is critical
* Deny overrides Allow
* Multi-AZ ensures high availability

---

✅ **End of MST Notes**
