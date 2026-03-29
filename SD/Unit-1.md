# 🚀 UNIT 1 — SYSTEM DESIGN FUNDAMENTALS

---

## 🔹 1. What is System Design?

System Design is the process of designing architecture, components, and data flow of a system to meet specific requirements.

**Goal:**

* Build scalable
* Reliable
* Efficient systems

---

## 🔹 2. Importance of System Design

* Handles large-scale applications
* Improves performance
* Ensures reliability
* Enables scalability

**Real-world systems:**

* Facebook
* Google
* Netflix

---

## 🔹 3. Evolution of Systems

### 🖥️ Single Machine System

* All operations on one machine
* Easy to manage
* ❌ Not scalable

---

### 🌐 Distributed System

* Multiple machines working together
* Data + workload distributed

* ✔ Scalable
* ✔ Fault tolerant
* ❌ Complex

---

## 🔹 4. Key Concepts

---

### ⚖️ Scalability

Ability to handle increasing load.

#### Types:

* **Vertical Scaling (Scale Up)**

  * Increase power of single machine
  * Example: more RAM, CPU

* **Horizontal Scaling (Scale Out)**

  * Add more machines
  * Used in modern systems

---

### 🔒 Reliability & Fault Tolerance

* **Reliability:** System works correctly over time
* **Fault Tolerance:** System continues working even if some components fail

📌 Example:

* Server crash → system still runs

---

### ⏱️ Availability & Uptime

* Availability = % time system is operational

| Availability | Downtime/year |
| ------------ | ------------- |
| 99%          | ~3.65 days    |
| 99.9%        | ~8.7 hours    |
| 99.99%       | ~52 minutes   |

---

### ⚡ Performance & Latency

* **Performance:** overall system efficiency
* **Latency:** time taken to respond

📌 Lower latency = better user experience

---

### 🔄 Consistency

Ensures all users see same data.

#### Types:

* Strong consistency
* Eventual consistency

---

## 🔹 5. Architecture Patterns

---

### 🧱 Monolithic Architecture

* Single unified codebase

✔ Simple
✔ Easy to deploy
❌ Hard to scale

---

### 🧩 Microservices Architecture

* System split into small independent services

✔ Scalable
✔ Flexible
❌ Complex

---

### 🖥️ Client-Server Architecture

* Client sends request
* Server processes and responds

📌 Example:

* Web browser ↔ server

---

## 🔹 6. Understanding Requirements

---

### ✅ Functional Requirements

What system should do.

**Examples:**

* User login
* Upload post
* Search feature

---

### ⚙️ Non-Functional Requirements

How system should perform.

**Examples:**

* Scalability
* Performance
* Security
* Availability

---

## 🔹 7. Real-World Example (Connecting Everything)

### Example: Instagram

* Millions of users → need scalability
* Images/videos → need storage + CDN
* High uptime → reliability
* Fast loading → low latency

---

## ⚡ Quick Revision

* System Design → architecture planning
* Scalability → handle growth
* Reliability → works correctly
* Availability → uptime %
* Latency → response time
* Monolith vs Microservices
* Functional vs Non-functional

