# 🚀 Unit 3 — System Design Core
## 🌐 1. OSI Model (7 Layers)

| Layer        | Function               | Example   |
| ------------ | ---------------------- | --------- |
| Application  | User interaction       | HTTP, FTP |
| Presentation | Encryption, formatting | SSL/TLS   |
| Session      | Session control        | APIs      |
| Transport    | Data transfer          | TCP, UDP  |
| Network      | Routing                | IP        |
| Data Link    | MAC addressing         | Ethernet  |
| Physical     | Hardware               | Cables    |

**Key Insight:**

* OSI = Conceptual model
* Real-world uses TCP/IP

---

## 🌍 2. TCP/IP Model

| Layer          | Includes             |
| -------------- | -------------------- |
| Application    | HTTP, DNS            |
| Transport      | TCP, UDP             |
| Internet       | IP                   |
| Network Access | Physical + Data Link |

**Note:** TCP/IP is the practical implementation.

---

## 📡 3. Network Protocols

* **HTTP/HTTPS** → Web communication
* **TCP** → Reliable (used in banking, login systems)
* **UDP** → Fast, no guarantee (used in streaming, gaming)
* **DNS** → Domain → IP resolution

---

## ⚖️ 4. Load Balancer

**Purpose:** Distributes incoming traffic across multiple servers.

**Types:**

* Round Robin
* Least Connections
* IP Hash

**Benefits:**

* Prevents server overload
* Improves availability

---

## 🧵 5. Process vs Thread

| Feature   | Process  | Thread |
| --------- | -------- | ------ |
| Memory    | Separate | Shared |
| Speed     | Slower   | Faster |
| Isolation | High     | Low    |

**Insight:** Threads are lightweight and faster.

---

## 📊 6. Capacity Estimation

**Key Questions:**

* Users per day?
* Requests per user?
* Data per request?

**Example:**

* 1M users/day
* 10 requests/user
  → 10M requests/day (~115 req/sec)

---

## 🌐 7. HTTP vs HTTPS

| Feature    | HTTP | HTTPS   |
| ---------- | ---- | ------- |
| Security   | ❌    | ✅       |
| Encryption | No   | TLS/SSL |
| Port       | 80   | 443     |

---

## 🔄 8. Stateful vs Stateless

**Stateful:**

* Server remembers client state
* Example: Login sessions

**Stateless:**

* Each request independent
* Example: REST APIs

**Modern systems prefer:** Stateless

---

## ⚡ 9. Cache Memory

**Purpose:** Store frequently accessed data.

**Tools:**

* Redis
* Memcached

**Benefits:**

* Faster response
* Reduced database load

---

## 🗄️ 10. SQL vs NoSQL

| Feature  | SQL      | NoSQL      |
| -------- | -------- | ---------- |
| Schema   | Fixed    | Flexible   |
| Scaling  | Vertical | Horizontal |
| Use Case | Banking  | Big Data   |

---

## 📬 11. Message Queue

**Purpose:** Asynchronous communication between services.

**Examples:**

* Kafka
* RabbitMQ

**Use Case:**

* Order placed → Queue → Email service processes later

---

## 📌 12. Database Indexing

* Improves query performance
* Uses B-Trees

**Trade-offs:**

* Faster reads
* Slower writes
* Extra storage

---

## 🔀 13. Database Sharding

**Definition:** Splitting database into smaller parts.

**Example:**

* A–M → DB1
* N–Z → DB2

**Benefit:** Horizontal scaling

---

## 🔁 14. Consistent Hashing

**Problem:** Data reshuffling when servers change

**Solution:** Minimal redistribution

**Used in:**

* Distributed systems
* Caching systems

---

## 🌐 15. How Web Works

1. DNS resolves domain to IP
2. TCP 3-way handshake
3. HTTP request sent
4. Server responds

---

## 🤝 16. TCP Handshake (3-Way)

**Steps:**

1. SYN → Client initiates connection
2. SYN-ACK → Server acknowledges
3. ACK → Client confirms

**Ensures:**

* Reliability
* Synchronization

---

## 🔗 17. REST APIs

**Principles:**

* Stateless
* Resource-based

**Methods:**

* GET → Fetch
* POST → Create
* PUT → Replace
* PATCH → Partial update
* DELETE → Remove

---

## 🔄 18. GraphQL vs REST

| Feature       | REST     | GraphQL  |
| ------------- | -------- | -------- |
| Data Fetching | Fixed    | Flexible |
| Requests      | Multiple | Single   |
| Overfetching  | Yes      | No       |

---

## ⚡ 19. gRPC

* High-performance communication
* Uses Protocol Buffers
* Faster than REST

---

## ⚙️ 20. HTTP Methods

| Method | Purpose |
| ------ | ------- |
| GET    | Read    |
| POST   | Create  |
| PUT    | Replace |
| PATCH  | Modify  |
| DELETE | Remove  |

---

## 🧠 Quick Revision

* OSI vs TCP/IP → Concept vs Practical
* Load Balancer → Traffic distribution
* Cache → Speed improvement
* Queue → Async processing
* Sharding → DB scaling
* Indexing → Faster queries
* REST → Stateless APIs
* GraphQL → Flexible data fetching
* gRPC → High performance

---
