# Network Protocols: 

Quick notes on network protocols for High-Level Design (HLD) and interviews.

## Table of Contents

1. [What are Network Protocols?](#1-what-are-network-protocols)
2. [Network Models](#2-network-models)
3. [Important Network Protocols](#3-important-network-protocols)
4. [Communication Types](#4-communication-types)
5. [Why Protocols Matter in HLD](#5-why-network-protocols-matter-in-hld)
6. [Interview Questions](#6-interview-questions)
7. [Key Takeaway](#7-key-takeaway)

---

## 1. What are Network Protocols?

Network protocols are a set of standardized rules that define how two or more devices communicate and exchange data over a network.

These rules define:

| Area | Meaning |
|------|---------|
| **Connection Establishment** | How devices start communication |
| **Data Formatting** | How information is structured before sending |
| **Data Transmission** | How data moves between devices |
| **Error Handling** | How lost or corrupted data is handled |
| **Security** | How data is encrypted and authenticated |

> **Example:** When we open a website, the browser talks to the web server using HTTP/HTTPS.

---

## 2. Network Models

Network communication is explained using two models.

### A. OSI Model (Open Systems Interconnection)

A theoretical reference model with **7 layers**.

| Layer | Name | Responsibility |
|:-----:|------|----------------|
| 7 | Application | Network services for applications |
| 6 | Presentation | Data translation, encryption, compression |
| 5 | Session | Start, manage, and end sessions |
| 4 | Transport | End-to-end delivery and reliability |
| 3 | Network | Logical addressing and routing |
| 2 | Data Link | Node-to-node delivery and MAC addressing |
| 1 | Physical | Sends raw bits over physical media |

### B. TCP/IP Model

A practical model used for Internet communication. It has **4 layers**.

| Layer | Responsibility |
|-------|----------------|
| Application | Application-level network communication |
| Transport | End-to-end data transmission |
| Internet | IP addressing and routing |
| Network Access | Physical transmission and local network communication |

### OSI vs TCP/IP

| OSI Model | TCP/IP Model |
|-----------|--------------|
| Application | Application |
| Presentation | Application |
| Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link | Network Access |
| Physical | Network Access |

> **Remember:** OSI is a reference model. TCP/IP is a practical protocol suite used on the Internet.

---

## 3. Important Network Protocols

### A. Application Layer Protocols

| Protocol | Full Form | Purpose |
|----------|-----------|---------|
| **HTTP** | Hypertext Transfer Protocol | Client-server communication |
| **HTTPS** | HTTP Secure | Encrypted HTTP communication |
| **FTP** | File Transfer Protocol | Transfers files between systems |
| **SMTP** | Simple Mail Transfer Protocol | Sends emails |
| **DNS** | Domain Name System | Converts domain names into IP addresses |
| **WebSocket** | - | Persistent, two-way communication between client and server |

### B. Transport Layer Protocols

#### 1. TCP (Transmission Control Protocol)

- Connection-oriented
- Reliable data transmission
- Data arrives in the correct order
- Uses acknowledgements and retransmission
- Best when reliability is important

#### 2. UDP (User Datagram Protocol)

- Connectionless
- No delivery guarantee
- No ordering guarantee
- Lower overhead
- Best when low latency is important

#### TCP vs UDP

| TCP | UDP |
|-----|-----|
| Connection-oriented | Connectionless |
| Reliable delivery | No guaranteed delivery |
| Ordered delivery | No guaranteed ordering |
| Higher overhead | Lower overhead |
| Used in HTTP/HTTPS, FTP | Used in DNS, online gaming, streaming, real-time communication |

---

## 4. Communication Types

### A. Client-Server Communication

A client sends a request. The server processes it and returns a response.

| Protocol | Use |
|----------|-----|
| HTTP/HTTPS | API communication |
| WebSocket | Real-time, two-way communication |
| FTP | File transfer |
| SMTP | Email transmission |

> **Example:** A browser requesting a webpage from a web server.

### B. Peer-to-Peer (P2P) Communication

Two or more systems talk directly, without a central server for every data exchange.

| Technology | Use |
|------------|-----|
| **BitTorrent** | Peer-to-peer file sharing |
| **WebRTC** | Real-time peer-to-peer audio, video, and data |

> TCP and UDP can both be used as transport protocols in P2P communication.

---

## 5. Why Network Protocols Matter in HLD

In HLD, we design the overall architecture of a system and define how components communicate. Protocols help decide **how** that communication happens in a distributed system.

### Example: Chat Application

| Requirement | Protocol / Technology |
|-------------|-----------------------|
| Client-server API communication | HTTP/HTTPS |
| Real-time messaging | WebSocket |
| Reliable data transmission | TCP |
| Domain name resolution | DNS |
| Secure communication | TLS/HTTPS |

### Benefits in HLD

| Benefit | How it helps |
|---------|--------------|
| **Scalability** | Helps design communication between distributed services |
| **Reliability** | Ensures proper data delivery mechanisms |
| **Security** | Supports encrypted and authenticated communication |
| **Performance** | Choose protocols based on latency and throughput needs |
| **Interoperability** | Different systems and technologies can talk using standard rules |

---

## 6. Interview Questions

- [ ] What are network protocols?
- [ ] Why are network protocols necessary in HLD?
- [ ] What is the difference between OSI and TCP/IP models?
- [ ] Explain all seven layers of the OSI model.
- [ ] What is the difference between TCP and UDP?
- [ ] What is the difference between HTTP and HTTPS?
- [ ] What is the difference between HTTP and WebSocket?
- [ ] What is DNS and why is it required?
- [ ] What is the difference between client-server and peer-to-peer communication?
- [ ] Can two systems communicate without using HTTP?
- [ ] Why do we use WebSocket in real-time applications?
- [ ] What is the role of TCP in HTTP communication?

---

## 7. Key Takeaway

Network protocols define the rules of communication between systems.

In HLD, choosing the right protocol is important for building scalable, reliable, secure, and efficient distributed systems.

**Interviewer**: What are network protocols? Why are they necessary in High-Level Design?

Network protocols are a set of standardized rules that define how two or more devices communicate and exchange data over a network.

To understand network communication, we have two important models: OSI and TCP/IP.

The OSI model is a theoretical reference model consisting of seven layers, whereas the TCP/IP model is a practical networking model consisting of four layers, widely used for Internet communication.

In High-Level Design, network protocols are important because they help us decide how different components of a distributed system communicate with each other.

For example:

- We use HTTP/HTTPS for client-server communication.
- We use WebSocket for real-time, two-way communication.
- We use TCP when reliable data delivery is required.
- We use UDP when low-latency communication is preferred.
- We use DNS to resolve domain names into IP addresses.

Similarly, technologies like WebRTC and BitTorrent support peer-to-peer communication.

Therefore, choosing appropriate network protocols helps us design scalable, reliable, secure and efficient distributed systems.

### Quick Recall

| Protocol | Remember as |
|----------|-------------|
| **HTTP/HTTPS** | Request-response communication |
| **WebSocket** | Real-time, two-way communication |
| **TCP** | Reliable data transmission |
| **UDP** | Low-overhead, connectionless transmission |
| **DNS** | Domain name resolution |
| **WebRTC / BitTorrent** | Peer-to-peer communication |
