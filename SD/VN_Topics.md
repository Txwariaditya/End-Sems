# 🚀 UNIT 3 — SYSTEM DESIGN

---

## 🌐 1. How Google Works (DNS + Handshake)

### 🔹 Step 1: DNS Resolution

You type: `google.com`

* Browser asks: *“What is the IP?”*
* DNS (Domain Name System) translates:

```
google.com → 142.250.xxx.xxx
```

**📌 Think:** DNS = Internet’s phonebook

---

### 🔹 Step 2: TCP Handshake (3-Way)

**Connection setup between client & server:**

1. **SYN** → Client: “Can we connect?”
2. **SYN-ACK** → Server: “Yes, I’m ready”
3. **ACK** → Client: “Let’s go”

**📌 Ensures:**

* Reliability
* Synchronization

---

### 🔹 Step 3: HTTP Request/Response

* Browser sends request
* Server returns HTML, CSS, JS

---

### 🔹 TLS (HTTPS)

* Encryption layer added after TCP
* Protects sensitive data (passwords, etc.)

---

## 🤝 2. Two-Way vs Three-Way Handshake

### 🔹 2-Way Handshake

* SYN → SYN-ACK

**❌ Problems:**

* No confirmation from client
* Can cause **half-open connections**

---

### 🔹 3-Way Handshake (Used)

* SYN → SYN-ACK → ACK

**✅ Reliable because:**

* Both sides confirm readiness

**📌 Interview Line:**

> 3-way handshake prevents stale or duplicate connections.

---

## 🧠 3. Database Indexing

### 🔹 What is it?

A data structure that improves search speed.

**Without index:**

* Full table scan → slow

**With index:**

* Direct lookup → fast

---

### 🔹 Example

```sql
SELECT * FROM students WHERE roll_no = 101;
```

* Without index → scans entire table
* With index → jumps directly

---

### 🔹 Types

* Primary Index
* Secondary Index
* B-Tree Index (most common)
* Hash Index

---

### 🔹 Trade-offs

* ✔ Fast reads
* ❌ Slower writes (index updates required)
* ❌ Extra storage

---

## 🔥 4. Thrashing (OS Concept)

### 🔹 What is it?

System spends more time swapping pages than executing.

---

### 🔹 Why it happens?

* Too many processes
* Insufficient RAM
* High page fault rate

---

### 🔹 Result

* ❌ Low CPU utilization
* ❌ System slowdown

---

### 🔹 Solution

* Increase RAM
* Reduce multiprogramming
* Use better page replacement (e.g., LRU)

---

## 🗄️ 5. Database Sharing

### 🔹 Meaning

Multiple users/applications accessing the same database.

---

### 🔹 Types

1. **Centralized DB**

   * Single server

2. **Distributed DB**

   * Data spread across multiple locations

3. **Cloud DB**

   * Shared over internet (AWS, GCP)

---

### 🔹 Problems

* Concurrency issues
* Data consistency challenges
* Deadlocks

---

## 🧾 6. SQL vs NoSQL

### 🔹 SQL (Relational)

* Structured tables
* Fixed schema

**Examples:**

* MySQL
* PostgreSQL

✔ Strong consistency
✔ ACID properties

---

### 🔹 NoSQL (Non-Relational)

* Flexible schema
* JSON-like data

**Examples:**

* MongoDB
* Cassandra

✔ Scalable
✔ Handles large data efficiently

---

## ⚖️ 7. Consistent Hashing

### 🔹 What is it?

Technique to distribute data across servers efficiently.

---

### 🔹 Problem it solves

When servers are added/removed:

* Normal hashing → massive reshuffling ❌
* Consistent hashing → minimal redistribution ✅

---

### 🔹 How it works

* Data and servers mapped on a circular ring
* Data assigned to nearest server clockwise

---

### 🔹 Benefits

* ✔ Load balancing
* ✔ Fault tolerance
* ✔ Scalability

**📌 Used in:**

* Distributed caches
* CDNs
* Databases (e.g., Cassandra)

---

## ⚡ Final Revision (Quick Recall)

* DNS → Domain to IP
* 3-way handshake → Reliable connection
* Indexing → Faster queries
* Thrashing → Excessive paging
* DB sharing → Multi-user access issues
* SQL vs NoSQL → Structure vs flexibility
* Consistent hashing → Efficient scaling

---
