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

| Layer No | Layer Name | Main Function | Example Protocols / Devices |   ব্যাখ্যা |
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
### 🧠 Simple Mnemonic (Easier to Remember)

**Top to Bottom:**  
👉 *All People Seem To Need Data Processing*  
(Application → Presentation → Session → Transport → Network → Data Link → Physical)

**Bottom to Top:**  
👉 *Please Do Not Throw Sausage Pizza Away*

<br>

### ⚙️ OSI Model Function Flow (Example)

1. **Sender:**  
   - Application → Physical (Data moves downward through layers)
2. **Transmission:**  
   - Data travels through the network medium
3. **Receiver:**  
   - Physical → Application (Data moves upward and reconstructed)

### 🧠 Example

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

<br>

💡 **Analogy (সহজ উদাহরণ):**  
OSI = “Blueprint” → conceptually shows how things work  
TCP/IP = “Actual Building” → what is actually implemented on the Internet

<br>
