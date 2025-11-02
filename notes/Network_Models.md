## 🔹 What is a Network Model?

**English:**  
A network model is a conceptual framework that describes how data is transmitted and received across a network.  
It helps standardize communication between different devices and vendors.

**বাংলা:**  
নেটওয়ার্ক মডেল হলো একটি ধারাবাহিক কাঠামো, যা দেখায় কিভাবে ডেটা নেটওয়ার্কের মধ্যে পাঠানো এবং গ্রহণ করা হয়।  
এটি বিভিন্ন ডিভাইস ও ভেন্ডরের মধ্যে standard communication নিশ্চিত করে।


---

## 🔹 Networking Model Types

Networking models are mainly of **two types**:
- 1 : OSI Model
- 2 : TCP/IP Model


| Model | Purpose | Layers | Usage | Standard |
|-------|---------|--------|-------|---------|
| **OSI Model** (Open Systems Interconnection) | Conceptual / Educational | 7 (Physical, Data Link, Network, Transport, Session, Presentation, Application) | Understanding and standardizing communication between devices | ISO Standard |
| **TCP/IP Model** (Transmission Control Protocol / Internet Protocol) | Practical / Real-world | 4 (Network Interface / Link, Internet, Transport, Application) | Used in real-world networking | IETF Standard |


# 🌐 Network Models — OSI & TCP/IP 

---

## 1️⃣ OSI Model (Open Systems Interconnection)

**English:**  
The OSI Model is a conceptual framework used to understand how different networking protocols interact across seven layers.

**বাংলা:**  
OSI Model হলো একটি ধারণাগত ফ্রেমওয়ার্ক যা দেখায় কিভাবে বিভিন্ন নেটওয়ার্ক প্রোটোকল একে অপরের সাথে সাতটি স্তরের মাধ্যমে কাজ করে।  

**7 Layers of OSI Model:**

| Layer No | Layer Name | English Description | বাংলা ব্যাখ্যা |
|----------|------------|-------------------|----------------|
| 7 | Application | Provides network services to end-users (HTTP, FTP, SMTP) | ব্যবহারকারীর জন্য নেটওয়ার্ক সার্ভিস সরবরাহ করে |
| 6 | Presentation | Translates data formats, encryption/decryption | ডেটা ফরম্যাট রূপান্তর, এনক্রিপশন/ডিক্রিপশন |
| 5 | Session | Manages sessions and connections | সেশন বা সংযোগ পরিচালনা করে |
| 4 | Transport | Ensures reliable data transfer (TCP/UDP) | নির্ভরযোগ্য ডেটা ট্রান্সফার নিশ্চিত করে |
| 3 | Network | Determines paths and logical addressing (IP) | ডেটা গন্তব্য ঠিক করে, লজিক্যাল অ্যাড্রেসিং |
| 2 | Data Link | Handles MAC addresses, error detection | ডিভাইস লেভেল ঠিকানা ও error detection |
| 1 | Physical | Transmits raw bits over physical medium | ফিজিক্যাল মাধ্যমে বিট ট্রান্সমিশন |

**Key Points:**

- Layered approach → easier troubleshooting  
- Each layer serves the layer above it and is served by the layer below  

---

## 2️⃣ TCP/IP Model (Transmission Control Protocol / Internet Protocol)

**English:**  
TCP/IP Model is a practical model used in real-world networking, focusing on the protocols used on the Internet.

**বাংলা:**  
TCP/IP Model হলো বাস্তব নেটওয়ার্কে ব্যবহৃত মডেল, যা ইন্টারনেটে ব্যবহৃত প্রোটোকলগুলোর উপর গুরুত্ব দেয়।  

**4 Layers of TCP/IP Model:**

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
