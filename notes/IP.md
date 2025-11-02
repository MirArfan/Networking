### 🌐 What is IP (Internet Protocol)?



**IP (Internet Protocol)** is a set of rules that defines how data is sent and received over the Internet or any network.  
It ensures that data packets are delivered from the source device to the destination device correctly.

Every device connected to a network has a unique **IP address** that identifies it — just like a house has a unique address.

Example: `192.168.1.1` or `2001:0db8:85a3::8a2e:0370:7334`

<br>
 

### 🔹 Types of IP

| Type | Description | Example |
|------|--------------|----------|
| **IPv4** | 32-bit address; written as 4 numbers separated by dots. | `192.168.0.1` |
| **IPv6** | 128-bit address; written in hexadecimal with colons. | `2001:0db8:85a3::8a2e:0370:7334` |

<br>

| Feature | IPv4 | IPv6 |
|---------|------|------|
| **Address Length** | 32-bit | 128-bit |
| **Format** | Dotted decimal (e.g., `192.168.1.1`) | Hexadecimal (e.g., `2001:db8::1`) |
| **Address Space** | ~4.3 billion addresses (limited) | Almost unlimited (≈ 3.4 × 10³⁸ addresses) |
| **Performance** | Slower (due to NAT and smaller space) | Better (more efficient routing, no NAT) |
| **Usage** | Still widely used | Growing adoption (supports coexistence with IPv4) |
| **Configuration** | Manual or DHCP (Easy and simple) | Auto-configuration supported (require new training infracturcture) |
| **Security** | Optional (IPSec can be added) | Built-in IPSec (mandatory support) |
| **Authentication** | Not built-in | Built-in authentication and encryption ( Secure ) |
| **Header Size** | 20 bytes (variable) | 40 bytes (fixed) |
| **Example Use** | Most existing networks | Modern networks, IoT, future internet |


## 🔹 IP Address Classes (IPv4)

| Class | Range | Used For |
|-------|--------|-----------|
| **A** | 1.0.0.0 – 126.255.255.255 | Large networks |
| **B** | 128.0.0.0 – 191.255.255.255 | Medium networks |
| **C** | 192.0.0.0 – 223.255.255.255 | Small networks |
| **D** | 224.0.0.0 – 239.255.255.255 | Multicasting |
| **E** | 240.0.0.0 – 255.255.255.255 | Experimental |

---

## 🔹 Private vs Public IP

| Type | Description | Example |
|------|--------------|----------|
| **Private IP** | Used within local networks (LAN), not accessible from the Internet. | `192.168.x.x`, `10.x.x.x` |
| **Public IP** | Used on the Internet, globally unique. | `8.8.8.8` (Google DNS) |

---

## 🔹 How IP Works (Simple Flow)

**Example Scenario:**
1. You send a message from your computer to another computer on the Internet.  
2. Your computer’s **IP** acts as the **source address**.  
3. The receiver’s **IP** acts as the **destination address**.  
4. Routers read these IPs and forward data to the correct location.

---

### 🔹 Bengali Summary

- **IP** হলো এমন একটি প্রোটোকল যা নেটওয়ার্কে ডেটা পাঠানো ও গ্রহণের নিয়ম ঠিক করে।  
- প্রতিটি ডিভাইসের একটি **IP address** থাকে, যা তার ইউনিক ঠিকানা।  
- **IPv4** পুরনো এবং 32-bit, **IPv6** নতুন এবং 128-bit।  
- **Private IP** শুধু LAN-এ ব্যবহার হয়, **Public IP** ইন্টারনেটের জন্য।  
- Routers IP address দেখে ডেটা কোথায় পাঠাতে হবে তা নির্ধারণ করে।


# 🌐 Public, Private, Static & Dynamic IP — Explained (Bangla + English)

---

## 🧩 What is an IP Address?

**English:**  
An IP (Internet Protocol) Address is a unique numerical label assigned to each device connected to a network.  
It helps identify and locate devices in a network.

**বাংলা:**  
IP Address হলো একটি অনন্য সংখ্যা যা প্রতিটি ডিভাইসকে দেওয়া হয়,  
যাতে নেটওয়ার্কে সেই ডিভাইসকে চেনা ও যোগাযোগ করা যায়।

---

## 🌍 1️⃣ Public IP Address

**English:**  
A Public IP is an address that is **accessible from the Internet**.  
It is unique globally and assigned by your **Internet Service Provider (ISP)**.  
It identifies your network to the outside world.

**Example:** `103.120.56.22`

**বাংলা:**  
Public IP হলো এমন একটি IP যা **ইন্টারনেট থেকে অ্যাক্সেস করা যায়**।  
এটি **ISP (Internet Service Provider)** দ্বারা নির্ধারিত হয় এবং পুরো পৃথিবীতে একটিই ইউনিক থাকে।  
এটি তোমার নেটওয়ার্ককে বাইরের পৃথিবীতে চিহ্নিত করে।

**Used for:**  
- Web servers  
- Routers connected to the Internet  
- Any device that needs global access  

---

## 🏠 2️⃣ Private IP Address

**English:**  
A Private IP is used **inside a local network (LAN)**.  
It **cannot be accessed directly from the Internet**.  
Used for communication between internal devices.

**Example Ranges:**
- `10.0.0.0` → `10.255.255.255`  
- `172.16.0.0` → `172.31.255.255`  
- `192.168.0.0` → `192.168.255.255`

**বাংলা:**  
Private IP শুধু **লোকাল নেটওয়ার্কের (LAN)** মধ্যে ব্যবহৃত হয়।  
এটি সরাসরি ইন্টারনেট থেকে অ্যাক্সেস করা যায় না।  
একই লোকাল নেটওয়ার্কে থাকা কম্পিউটার/ডিভাইসগুলোর মধ্যে যোগাযোগে ব্যবহৃত হয়।

**Used for:**  
- Computers, mobiles, printers inside home/office  
- Routers assign these using DHCP  

---

## 🧱 3️⃣ Static IP Address

**English:**  
A Static IP does **not change** over time.  
It is **manually assigned** to a device and remains constant.  
Best for servers and hosting.

**বাংলা:**  
Static IP হলো এমন IP যা **স্থায়ী** — সময়ের সাথে পরিবর্তন হয় না।  
এটি **ম্যানুয়ালি সেট করা হয়** এবং সবসময় একই থাকে।  
সার্ভার ও ওয়েব হোস্টিংয়ের জন্য এটি আদর্শ।

**Example:**  
A company’s web server IP → `103.25.88.14`

**Used for:**  
- Web servers  
- Database servers  
- Email servers  

---

## 🔁 4️⃣ Dynamic IP Address

**English:**  
A Dynamic IP is **automatically assigned** by a DHCP server or ISP.  
It **changes** every time the device reconnects to the network.  
Commonly used for home internet connections.

**বাংলা:**  
Dynamic IP হলো এমন IP যা **স্বয়ংক্রিয়ভাবে DHCP সার্ভার বা ISP দ্বারা দেওয়া হয়**।  
প্রতিবার নেটওয়ার্কে যুক্ত হলে IP পরিবর্তিত হতে পারে।  
বাড়ির ইন্টারনেট কানেকশনে এটি সবচেয়ে বেশি ব্যবহৃত হয়।

**Used for:**  
- Home networks  
- Regular users (non-server)  
- Saves IP allocation cost  

---

## ⚖️ Comparison Table

| Feature | Public IP | Private IP | Static IP | Dynamic IP |
|----------|------------|-------------|------------|-------------|
| **Access** | Accessible from Internet | Local network only | Fixed | Changes automatically |
| **Assigned by** | ISP | Router (DHCP) | Manually | DHCP Server |
| **Uniqueness** | Globally unique | Unique within LAN | Permanent | Temporary |
| **Use Case** | Web servers, routers | Home/office LAN | Servers | Home users |
| **Security** | Less secure | More secure (internal) | Depends on setup | More secure (changes) |

---

## 🧠 Key Points Summary

- 🌍 **Public IP:** Global, Internet-visible  
- 🏠 **Private IP:** Local, internal use only  
- 📡 **Static IP:** Permanent, fixed manually  
- 🔁 **Dynamic IP:** Temporary, auto-assigned  

---

💡 **Example (Home Network):**
Your ISP gives your router a **Public IP**.  
Your router gives your computer a **Private Dynamic IP** like `192.168.0.5`.  
If you host a website, you might use a **Static Public IP**.


# 🌐 Static IP vs Dynamic IP 

---

## 🧩 What is Static IP?

**English:**  
A Static IP Address is a fixed IP that does **not change** over time.  
It is manually configured for a specific device or server.

**বাংলা:**  
Static IP Address হলো এমন একটি স্থায়ী IP যা সময়ের সাথে **পরিবর্তিত হয় না**।  
এটি নির্দিষ্ট ডিভাইস বা সার্ভারের জন্য **ম্যানুয়ালি সেট করা হয়**।

**Example:**  
- A company’s web server IP: `103.25.88.14`

**Used For:**  
- Web servers  
- Database servers  
- Email servers  
- CCTV or Remote access devices  

---

## 🔁 What is Dynamic IP?

**English:**  
A Dynamic IP Address is **automatically assigned** by a DHCP server or ISP.  
It **changes** each time the device reconnects to the network.

**বাংলা:**  
Dynamic IP Address হলো এমন IP যা **DHCP সার্ভার বা ISP স্বয়ংক্রিয়ভাবে দেয়**।  
প্রতিবার ডিভাইস নেটওয়ার্কে যুক্ত হলে IP **পরিবর্তিত হতে পারে**।

**Example:**  
- Home internet connections usually use dynamic IPs.

**Used For:**  
- Home users  
- Office computers  
- Mobile and WiFi connections  

---

## ⚖️ Difference Between Static and Dynamic IP

| Feature | 🧱 Static IP | 🔁 Dynamic IP |
|----------|--------------|----------------|
| **Assignment** | Manually assigned | Automatically assigned (by DHCP) |
| **Change** | Remains fixed | Changes each time device reconnects |
| **Configuration** | Requires manual setup | No manual setup needed |
| **Cost** | Usually costs more | Generally cheaper |
| **Best For** | Servers, hosting, remote devices | Regular users, home networks |
| **Reliability** | High (same address always) | Medium (address changes) |
| **Security** |( Less ) More exposed to attacks | More secure (changes frequently) |
| **Uses** |Servers | Home devices  |
| **Example** | Web Server IP: `203.45.22.10` | Laptop IP: `192.168.0.5` |

---

## 🧠 Summary

- 📡 **Static IP** → Fixed, manually set, used for servers and remote access.  
- 🔁 **Dynamic IP** → Auto-assigned, changes regularly, used for general users.  

---

💡 **Simple Analogy (সহজ তুলনা):**  
Static IP = তোমার **স্থায়ী ঠিকানা** (যেখানে চিঠি সবসময় যাবে)  
Dynamic IP = তোমার **অস্থায়ী অবস্থান** (যখন যেখানে থাকো, ঠিকানা বদলায়)
