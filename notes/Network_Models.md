## 🔹 What is a Network Model?


A **network model** is a conceptual framework that describes **how data is transmitted and received** across a network.  
It helps standardize communication between different devices and vendors.

 
নেটওয়ার্ক মডেল হলো একটি ধারাবাহিক কাঠামো, যা দেখায় কিভাবে ডেটা নেটওয়ার্কের মধ্যে পাঠানো এবং গ্রহণ করা হয়।  
এটি বিভিন্ন ডিভাইস ও ভেন্ডরের মধ্যে standard communication নিশ্চিত করে।

<br>

### 🔹 Networking Model Types

Networking models are mainly of **two types**:
1.  OSI Model
2.  TCP/IP Model


| Model | Purpose | Layers | Usage | Standard |
|-------|---------|--------|-------|---------|
| **OSI Model** (Open Systems Interconnection) | Conceptual / Educational | 7 (Physical, Data Link, Network, Transport, Session, Presentation, Application) | Understanding and standardizing communication between devices | ISO Standard |
| **TCP/IP Model** (Transmission Control Protocol / Internet Protocol) | Practical / Real-world | 4 (Network Interface / Link, Internet, Transport, Application) | Used in real-world networking | IETF Standard |

<br>


### 🌐 Network Models — OSI & TCP/IP 


### 1️⃣ OSI Model (Open Systems Interconnection)

The **OSI Model** is a conceptual framework used to understand how different networking protocols interact across seven layers.


OSI Model হলো একটি ধারণাগত ফ্রেমওয়ার্ক যা দেখায় কিভাবে বিভিন্ন নেটওয়ার্ক প্রোটোকল একে অপরের সাথে সাতটি স্তরের মাধ্যমে কাজ করে।  



### 🪜 The 7 Layers of OSI Model (Top to Bottom)

| Layer No | Layer Name | Main Function | Example Protocols / Devices | বাংলা ব্যাখ্যা |
|-----------|-------------|----------------|-----------------------------|----------------|
| **7** | **Application Layer** | Interface between user and network. Provides services like email, web browsing, file transfer. (Provides network services to end-users )| HTTP, HTTPS, FTP, SMTP, DNS | ব্যবহারকারী ও নেটওয়ার্কের মধ্যে সংযোগ তৈরি করে; যেমন ওয়েব ব্রাউজিং, ফাইল ট্রান্সফার। |
| **6** | **Presentation Layer** | Translates data formats, encryption & compression. | SSL, TLS, JPEG, MPEG | ডেটা এনক্রিপশন, কমপ্রেশন ও ফরম্যাট রূপান্তর করে। |
| **5** | **Session Layer** | Manages sessions (start, maintain, end connections). | NetBIOS, RPC | দুটি ডিভাইসের মধ্যে যোগাযোগ সেশন শুরু, বজায় রাখা ও বন্ধ করা। |
| **4** | **Transport Layer** | Ensures reliable data delivery with error control and segmentation. | TCP, UDP | ডেটাকে ভাগ করা, পুনরায় একত্র করা, ও নির্ভরযোগ্যভাবে পাঠানো নিশ্চিত করে। |
| **3** | **Network Layer** | Determines best path for data and handles logical addressing. | IP, ICMP, Router | প্যাকেট রাউটিং ও IP অ্যাড্রেসের মাধ্যমে ডেটা প্রেরণ। |
| **2** | **Data Link Layer** | Provides node-to-node delivery using MAC addresses. | Ethernet, Switch, PPP | ফ্রেম আকারে ডেটা পাঠানো ও error detection করে। |
| **1** | **Physical Layer** | Transmits raw bits (0s and 1s) over cables/wireless. | Cables, Hubs, Repeaters | কেবল বা সিগনালের মাধ্যমে ডেটা পাঠানো (ফিজিক্যাল ট্রান্সমিশন)। |

### 📊 Simple Diagram (Top to Bottom)
```
    +----------------------+
            | 
    7. Application Layer 
            |
    6. Presentation Layer
            |
    5. Session Layer     
            |
    4. Transport Layer 
            |
    3. Network Layer 
            |
    2. Data Link Layer 
            |
    1. Physical Layer 
            |
    +----------------------+
```
## 🧠 Simple Mnemonic (Easier to Remember)

**Top to Bottom:**  
👉 *All People Seem To Need Data Processing*  
(Application → Presentation → Session → Transport → Network → Data Link → Physical)

**Bottom to Top:**  
👉 *Please Do Not Throw Sausage Pizza Away*

---

## ⚙️ OSI Model Function Flow (Example)

1. **Sender:**  
   - Application → Physical (Data moves downward through layers)
2. **Transmission:**  
   - Data travels through the network medium
3. **Receiver:**  
   - Physical → Application (Data moves upward and reconstructed)

## 🧠 Example

যখন তুমি একটি ওয়েবসাইট ওপেন করো:
1. Browser → Application Layer (HTTP request)
2. Data → Presentation Layer (encrypted via TLS)
3. Session Layer → maintains connection
4. Transport Layer → TCP breaks data into segments
5. Network Layer → IP address দিয়ে route নির্ধারণ
6. Data Link Layer → ফ্রেম তৈরি হয় MAC address সহ
7. Physical Layer → bits send হয় কেবলের মাধ্যমে

### 💡 Quick Summary
- **Upper Layers (5–7):** Deal with software and user interaction.  
- **Lower Layers (1–4):** Deal with data transmission and network operations.  
- Helps standardize communication between different network devices and protocols.

**Key Points:**

- Layered approach → easier troubleshooting  
- Each layer serves the layer above it and is served by the layer below  

<br>

### 2️⃣ TCP/IP Model (Transmission Control Protocol / Internet Protocol)

TCP/IP Model is a practical model used in real-world networking, focusing on the protocols used on the Internet.

 
TCP/IP Model হলো বাস্তব নেটওয়ার্কে ব্যবহৃত মডেল, যা ইন্টারনেটে ব্যবহৃত প্রোটোকলগুলোর উপর গুরুত্ব দেয়।  

🔹 **4 Layers of TCP/IP Model:**

| Layer | English Description | বাংলা ব্যাখ্যা | Example Protocols |
|-------|-------------------|----------------|-----------------|
| 4 | Application | Provides services to applications | ব্যবহারকারীর জন্য সার্ভিস | HTTP, FTP, SMTP, DNS |
| 3 | Transport | Ensures end-to-end communication | এন্ড-টু-এন্ড কমিউনিকেশন | TCP, UDP |
| 2 | Internet | Logical addressing & routing | লজিক্যাল অ্যাড্রেসিং ও রাউটিং | IP, ICMP |
| 1 | Network Access / Link | Physical addressing & data transfer | ফিজিক্যাল লেভেল ট্রান্সফার | Ethernet, WiFi |

**Key Points:**

- TCP/IP is simpler & widely used in the Internet  
- OSI is conceptual, TCP/IP is practical  
- OSI → 7 layers, TCP/IP → 4 layers  

---

💡 **Analogy (সহজ উদাহরণ):**  
OSI = “Blueprint” → conceptually shows how things work  
TCP/IP = “Actual Building” → what is actually implemented on the Internet


---
# 🚚 Transport Layer — OSI Model (Layer 4)

---

## 🧩 Overview

**English:**  
The **Transport Layer** is the 4th layer of the OSI model.  
It is responsible for **end-to-end communication**, **data segmentation**, **error control**, and **flow control** between devices.

**বাংলা:**  
Transport Layer হলো OSI Model-এর ৪র্থ স্তর।  
এই স্তরের কাজ হলো ডেটা এক প্রান্ত থেকে অন্য প্রান্তে নির্ভরযোগ্যভাবে পাঠানো, ডেটাকে ছোট ছোট অংশে ভাগ করা (segmentation), এবং error ও flow control করা।

---

## ⚙️ Main Functions of Transport Layer

| Function | English Explanation | বাংলা ব্যাখ্যা |
|-----------|---------------------|----------------|
| **Segmentation & Reassembly** | Divides data into smaller segments before transmission, and reassembles them at destination. | ডেটাকে ছোট ছোট অংশে ভাগ করে পাঠানো এবং গন্তব্যে পৌঁছে আবার একত্র করা। |
| **End-to-End Delivery** | Ensures data is delivered from one device to another device correctly. | এক ডিভাইস থেকে অন্য ডিভাইসে ডেটা সঠিকভাবে পৌঁছানো নিশ্চিত করে। |
| **Error Control** | Detects and retransmits lost or corrupted data segments. | ডেটা হারালে বা নষ্ট হলে পুনরায় পাঠায়। |
| **Flow Control** | Controls the rate of data transmission so that receiver is not overloaded. | রিসিভার যেন অতিরিক্ত ডেটা না পায়, তা নিশ্চিত করে। |
| **Connection Control** | Can provide connection-oriented (reliable) or connectionless (fast) service. | সংযোগযুক্ত (TCP) বা সংযোগবিহীন (UDP) পরিষেবা প্রদান করে। |

---

## 🔗 Protocols Used in Transport Layer

| Protocol | Type | Description | বাংলা ব্যাখ্যা |
|-----------|------|-------------|----------------|
| **TCP (Transmission Control Protocol)** | Connection-Oriented | Reliable, ensures error-free, ordered delivery. | নির্ভরযোগ্য প্রোটোকল; ডেটা ঠিকঠাক ও ক্রম অনুসারে পৌঁছে দেয়। |
| **UDP (User Datagram Protocol)** | Connectionless | Faster, but no guarantee of delivery. | দ্রুত কিন্তু ডেটা হারানোর সম্ভাবনা থাকে। |

---

## 🧠 Difference Between TCP and UDP

| Feature | **TCP** | **UDP** |
|----------|----------|----------|
| Type | Connection-oriented | Connectionless |
| Reliability | Reliable (acknowledgment-based) | Unreliable |
| Speed | Slower | Faster |
| Error Control | Yes | No |
| Example Uses | Web browsing (HTTP), Email (SMTP), File transfer (FTP) | Video streaming, Online games, VoIP |

---

## 🧭 Example Flow

### 🖥️ Example: Sending an Email
1. Data created in Application Layer (SMTP).
2. Transport Layer breaks it into **segments** using TCP.
3. Each segment gets a **port number** (e.g., port 25 for SMTP).
4. Network Layer adds IP address.
5. Data travels through the network.
6. Receiver’s Transport Layer reassembles segments → passes to Application Layer.

---

## 🔢 Important Terms

| Term | Meaning | বাংলা ব্যাখ্যা |
|------|----------|----------------|
| **Port Number** | Identifies a specific application/service on a device. | ডিভাইসের নির্দিষ্ট সার্ভিস বা অ্যাপকে চিহ্নিত করে। |
| **Segment** | Data unit at Transport Layer (in TCP). | Transport Layer-এ ডেটার ইউনিট। |
| **Datagram** | Data unit at Transport Layer (in UDP). | UDP তে ডেটার ইউনিট। |
| **Socket** | Combination of IP address + Port number. | IP ঠিকানা ও পোর্ট নাম্বারের মিশ্রণ। |

---

## 🧩 Common Port Numbers

| Protocol | Port | Description |
|-----------|------|-------------|
| HTTP | 80 | Web traffic |
| HTTPS | 443 | Secure web traffic |
| FTP | 21 | File transfer |
| SMTP | 25 | Email sending |
| DNS | 53 | Domain name resolution |

---

## 💡 Summary

- Layer 4 of OSI Model.  
- Ensures **reliable, ordered, and error-free** delivery (TCP).  
- Provides **fast, lightweight communication** when reliability isn’t critical (UDP).  
- Handles **ports, segmentation, and flow control.**
