### 🌐 DNS (Domain Name System)


### 🧩 What is DNS?


DNS (Domain Name System) is a system that translates **domain names** (like `www.google.com`) into **IP addresses** (like `142.250.190.78`) so that computers can locate each other on a network.

DNS হলো এমন একটি সিস্টেম যা **ডোমেইন নাম** (যেমন `www.google.com`) কে **IP address** (যেমন `142.250.190.78`) এ রূপান্তর করে, যাতে কম্পিউটার একে অপরকে খুঁজে পেতে পারে।


### ⚙️ Why DNS is Needed

| Reason | English Explanation | বাংলা ব্যাখ্যা |
|--------|----------------------|----------------|
| **Easy to Remember** | Domain names are human-friendly, IP addresses are not. | ডোমেইন নাম মনে রাখা সহজ, IP address কঠিন। |
| **Dynamic IP Changes** | IP addresses of servers may change, but domain names remain the same. | সার্ভারের IP পরিবর্তন হলেও ডোমেইন নাম অপরিবর্তিত থাকে। |
| **Efficient Communication** | Converts names to IPs automatically for seamless browsing. | নাম থেকে IP রূপান্তর স্বয়ংক্রিয়ভাবে হয়, ফলে ব্রাউজিং সহজ হয়। |



### 🔗 Example

When you type `www.google.com` in your browser:

1. Your computer contacts a **DNS server**.  
2. DNS server looks up the IP for `www.google.com`.  
3. It returns something like `142.250.190.78`.  
4. Your browser then connects to that IP address to load the website.

<br>

### 🧠 DNS Working Process (Step-by-Step)

| Step | Process | Explanation |
|------|----------|-------------|
| 1️⃣ | **User Request** | User enters a domain name (e.g., `www.google.com`). |
| 2️⃣ | **Local DNS Cache Check** | Browser or OS checks if it already knows the IP. |
| 3️⃣ | **DNS Recursive Resolver** | If not found, request goes to a DNS resolver (usually by ISP). |
| 4️⃣ | **Root DNS Server** | Resolver asks the Root Server for top-level domain info (.com, .net). |
| 5️⃣ | **TLD DNS Server** | TLD server gives the address of the authoritative name server. |
| 6️⃣ | **Authoritative DNS Server** | Returns the actual IP address of the domain. |
| 7️⃣ | **Response Returned** | Resolver sends IP back to browser → browser connects to web server. |



### 🌍 DNS Hierarchy (Structure)

```
                ┌─────────────┐
                │ Root Server │
                └──────┬──────┘
                       │
              ┌────────┴────────┐
          (.com) TLD Server   (.org) TLD Server
              │                      │
    ┌─────────┴─────────┐      ┌─────┴─────┐
   google.com Server   yahoo.com Server   wikipedia.org Server

```



### 🧩 Types of DNS Servers

| Type | Function | বাংলা ব্যাখ্যা |
|------|-----------|----------------|
| **Root DNS Server** | Top-level server that directs queries to TLD servers. | শীর্ষ স্তরের সার্ভার যা প্রশ্নকে TLD সার্ভারে পাঠায়। |
| **TLD DNS Server** | Handles domains like `.com`, `.org`, `.net`, etc. | `.com`, `.org`, `.net` ইত্যাদি ডোমেইনের জন্য কাজ করে। |
| **Authoritative DNS Server** | Stores actual IP address of the website. | ওয়েবসাইটের আসল IP ঠিকানা সংরক্ষণ করে। |
| **Recursive Resolver** | Resolves the domain by querying other DNS servers. | ব্যবহারকারীর অনুরোধ অনুযায়ী IP খুঁজে বের করে। |



### 🧱 DNS Record Types

| Record Type | Description | Example |
|--------------|-------------|----------|
| **A Record** | Maps domain name → IPv4 address | `example.com → 192.168.1.1` |
| **AAAA Record** | Maps domain name → IPv6 address | `example.com → 2001:db8::1` |
| **CNAME** | Alias name for another domain | `www.example.com → example.com` |
| **MX Record** | Mail exchange record (for email) | `example.com → mail server` |
| **NS Record** | Nameserver record | Specifies DNS servers for a domain |
| **TXT Record** | Stores text data (e.g., SPF, verification) | Used for authentication, SPF, etc. |



### 🧠 Example DNS Resolution Flow
```
User → Browser → Local Cache
↓
DNS Resolver → Root Server
↓
TLD Server (.com)
↓
Authoritative Server (google.com)
↓
Returns IP (142.250.190.78)
↓
Browser connects to the Web Server

```


### 🔒 DNS Security (DNSSEC)

**DNSSEC (Domain Name System Security Extensions)**  
Adds a layer of security to DNS by verifying that responses come from legitimate DNS servers and are not tampered with.


DNSSEC DNS সিস্টেমে অতিরিক্ত নিরাপত্তা যোগ করে, যাতে ভুল বা হ্যাকড সার্ভার থেকে ভুয়া IP না আসে।



### 💡 Summary

- DNS translates domain names into IP addresses.  
- Works through Root → TLD → Authoritative servers.  
- Uses records like A, MX, CNAME, NS.  
- Makes internet browsing human-friendly.  
- DNSSEC ensures security and authenticity.

<br>
<br>

### 🔒 SSL & TLS (Secure Communication Protocols)


### 🧠 What is SSL / TLS?

**SSL (Secure Sockets Layer)** এবং **TLS (Transport Layer Security)** — এই দুটো প্রোটোকল ব্যবহার হয় **internet communication কে secure করার জন্য**।  
এগুলো data কে **encrypt** করে, যাতে কেউ মাঝপথে data intercept বা read করতে না পারে।

- 🔹 **SSL →** পুরনো version  
- 🔹 **TLS →** SSL এর আপডেটেড ও নিরাপদ version  

<br>

### ⚙️ How It Works (কাজ করার পদ্ধতি)

যখন তুমি একটি secure website (যেমন `https://`) visit করো:

1. **Client (Browser)** সার্ভারে request পাঠায়।  
2. **Server** তার digital certificate (SSL/TLS certificate) পাঠায়, যেখানে **public key** থাকে।  
3. **Browser** সেই certificate verify করে (trusted CA থেকে ইস্যু করা কিনা)।  
4. এরপর **Secure Connection (Handshake)** হয়।  
5. সবশেষে, **Data Encrypt হয়ে পাঠানো হয়** — অর্থাৎ কেউ মাঝপথে পেলেও পড়তে পারবে না।

<br>

### 🔑 Example

| Website | Protocol | Secure? |
|----------|-----------|---------|
| `http://example.com` | HTTP | ❌ No encryption |
| `https://example.com` | HTTPS (HTTP + SSL/TLS) | ✅ Encrypted |

<br>

### 🧩 Difference Between SSL and TLS

| Feature | SSL | TLS |
|----------|-----|-----|
| **Full Form** | Secure Sockets Layer | Transport Layer Security |
| **Developed By** | Netscape (1995) | IETF (1999) |
| **Security Level** | Less Secure | More Secure |
| **Handshake Speed** | Slower | Faster |
| **Current Use** | Deprecated | Widely Used |



### 💬 In Short

**TLS** is the modern, secure version of **SSL** —  
used to protect sensitive data (like passwords, payment info) between **client and server**.



### 📘 Real-Life Example

🔐 যখন তুমি লগইন করো **Facebook**, **Gmail**, বা **Bank Website** এ,  
তোমার **password বা personal data TLS encryption দিয়েই যায়**,  
যাতে কোনো attacker সেটা **চুরি বা পরিবর্তন** করতে না পারে।


### ⚙️ How SSL/TLS Works (Step-by-Step)

| Step | Process | Description |
|------|----------|-------------|
| 1️⃣ | **Client Hello** | Browser requests a secure connection from the server. |
| 2️⃣ | **Server Hello** | Server sends its SSL/TLS certificate (contains public key). |
| 3️⃣ | **Certificate Verification** | Browser verifies if the certificate is valid & trusted. |
| 4️⃣ | **Session Key Creation** | Browser and server agree on an encryption key. |
| 5️⃣ | **Secure Communication** | All data is now encrypted and securely transferred. |

**ব্যাখ্যা:**

1️⃣ ক্লায়েন্ট (ব্রাউজার) সার্ভারকে বলে — “আমি নিরাপদ সংযোগ চাই।”  
2️⃣ সার্ভার তার **SSL সার্টিফিকেট** পাঠায় (যেখানে public key থাকে)।  
3️⃣ ব্রাউজার সার্টিফিকেট যাচাই করে, সেটা trusted কিনা দেখে।  
4️⃣ উভয়ে **Session Key** তৈরি করে, যা দিয়ে ডেটা এনক্রিপ্ট হয়।  
5️⃣ এখন থেকে সব ডেটা **Encrypted** অবস্থায় আদান-প্রদান হয়।



### 🧠 Key Concepts

| Concept | English | বাংলা ব্যাখ্যা |
|----------|----------|----------------|
| **Encryption** | Converts readable data into secret code. | পাঠযোগ্য ডেটাকে গোপন কোডে রূপান্তর করে। |
| **Decryption** | Converts secret code back to readable data. | কোডকে আবার আসল ডেটায় রূপান্তর করে। |
| **Certificate** | Digital proof that a website is authentic. | একটি ওয়েবসাইট আসল তা প্রমাণ করার ডিজিটাল সার্টিফিকেট। |
| **Public Key** | Used to encrypt data. | ডেটা এনক্রিপ্ট করার জন্য ব্যবহৃত। |
| **Private Key** | Used to decrypt data. | ডেটা ডিক্রিপ্ট করার জন্য ব্যবহৃত। |



### 🧩 SSL vs TLS

| Feature | SSL | TLS |
|----------|-----|-----|
| **Full Form** | Secure Sockets Layer | Transport Layer Security |
| **Developed By** | Netscape (1990s) | IETF (as SSL's successor) |
| **Version** | Outdated (SSL 2.0, 3.0) | Modern (TLS 1.2, TLS 1.3) |
| **Security** | Less Secure | More Secure |
| **Used Today** | No (deprecated) | Yes (standard today) |

**Summary:**  
👉 TLS is the **updated and secure version** of SSL.  
Nowadays, when we say "SSL certificate", we actually mean **TLS certificate**.



### 🔒 Types of SSL/TLS Certificates

| Type | Use Case | Example |
|------|-----------|----------|
| **Domain Validated (DV)** | Basic encryption for small sites | personal blogs |
| **Organization Validated (OV)** | Validates company identity | business websites |
| **Extended Validation (EV)** | Highest level of trust (green bar) | banks, e-commerce |
| **Wildcard SSL** | Secures subdomains | `*.example.com` |
| **Multi-Domain (SAN)** | Secures multiple domains | `example.com`, `myapp.com` |


### 🧱 Why SSL/TLS is Important

| Benefit | English Explanation | বাংলা ব্যাখ্যা |
|----------|----------------------|----------------|
| 🔐 **Data Protection** | Encrypts all transmitted data. | ট্রান্সমিশনের সময় ডেটা এনক্রিপ্ট করে। |
| ✅ **Authentication** | Ensures the website is genuine. | ওয়েবসাইট আসল কিনা যাচাই করে। |
| 🚫 **Prevents Attacks** | Protects against man-in-the-middle attacks. | মাঝখানে আক্রমণ (MITM) প্রতিরোধ করে। |
| 🌍 **Trust & SEO** | Secure sites rank higher and gain user trust. | নিরাপদ সাইট ব্যবহারকারীর আস্থা ও SEO র‍্যাংক বাড়ায়। |


### 🧠 Simple Diagram: SSL/TLS Working Flow
```
[Browser] → Request Secure Page (https)
↓
[Server] → Sends Certificate (Public Key)
↓
[Browser] → Verifies Certificate
↓
[Browser + Server] → Create Session Key
↓
🔐 Encrypted Data Exchange Begins
```
<br><br>

### ⚙️ Common Protocols and Ports

### 🌍 1. HTTP — HyperText Transfer Protocol

**🔹 Purpose:**  
ওয়েব পেজ ডেটা আদান-প্রদানের জন্য ব্যবহৃত হয়।  
When you browse a website using `http://`, your browser and the web server communicate using HTTP.

**🔹 Port Number:** 80  
**🔹 Layer:** Application Layer  
**🔹 Secure?** ❌ No (data not encrypted)

**🔹 Example:**  
```
http://example.com
```

➡️ Sends/receives text, images, HTML files in plain text.



### 🔐 2. HTTPS — HyperText Transfer Protocol Secure

**🔹 Purpose:**  
HTTP + Security (via SSL/TLS).  
It encrypts the data between client and server, ensuring privacy and security.

**🔹 Port Number:** 443  
**🔹 Layer:** Application Layer  
**🔹 Secure?** ✅ Yes (encrypted using SSL/TLS)

**🔹 Example:**  
```
https://google.com
```


➡️ Safe for login, banking, payments, etc.


### 📂 3. FTP — File Transfer Protocol

**🔹 Purpose:**  
Server থেকে ফাইল upload/download করার জন্য ব্যবহৃত হয়।  
Used for transferring files between computers over a network.

**🔹 Port Numbers:**  
- Command (control): 21  
- Data transfer: 20

**🔹 Layer:** Application Layer  
**🔹 Secure Version:** SFTP (Secure FTP) or FTPS

**🔹 Example:**  
```
ftp://example.com
```


➡️ Developers use FTP to upload website files to hosting servers.


### 🧰 4. SSH — Secure Shell

**🔹 Purpose:**  
Server-এ secure remote login করার জন্য ব্যবহৃত হয়।  
It provides encrypted command-line access to a remote machine.

**🔹 Port Number:** 22  
**🔹 Layer:** Application Layer  
**🔹 Secure?** ✅ Yes (uses encryption)

**🔹 Example:**  
```
ssh user@192.168.1.10
```

➡️ Developers and sysadmins use SSH to configure or manage servers.



### 🌐 5. DNS — Domain Name System

**🔹 Purpose:**  
Domain name (যেমন google.com) কে IP address (যেমন 142.250.183.14) এ রূপান্তর করে।  
It translates human-readable domain names into machine-readable IP addresses.

**🔹 Port Number:** 53  
**🔹 Layer:** Application Layer  
**🔹 Protocol Used:** UDP (mostly), TCP (for large queries or zone transfers)

**🔹 Example:**  
```
User types → google.com
DNS converts → 142.250.183.14
```




### ✉️ 6. SMTP — Simple Mail Transfer Protocol

**🔹 Purpose:**  
Email পাঠানোর জন্য ব্যবহৃত হয় (Sending Mail)।  
Used by mail servers to send outgoing emails.

**🔹 Port Numbers:**  
- 25 → Default SMTP (non-secure)  
- 465 → Secure SMTP (SMTPS)  
- 587 → Modern secure submission port

**🔹 Layer:** Application Layer  
**🔹 Secure?** ✅ Yes, with SSL/TLS

**🔹 Example:**  
```
Mail servers like Gmail, Yahoo use SMTP to send emails.
````


### 🧭 Summary Table

| Protocol | Full Form | Default Port | Purpose | Secure? |
|----------|-----------|--------------|--------|---------|
| HTTP     | HyperText Transfer Protocol | 80 | Web browsing | ❌ No |
| HTTPS    | HyperText Transfer Protocol Secure | 443 | Secure web browsing | ✅ Yes |
| FTP      | File Transfer Protocol | 20, 21 | File upload/download | ❌ No |
| SSH      | Secure Shell | 22 | Secure remote login | ✅ Yes |
| DNS      | Domain Name System | 53 | Domain to IP resolution | ⚙️ Partially |
| SMTP     | Simple Mail Transfer Protocol | 25 / 465 / 587 | Send emails | ✅ Yes (with TLS/SSL) |



### 💡 Extra Tip for Interviews

- “Which layer of OSI does HTTP/FTP/SMTP belong to?” — ✅ Application Layer  
- “Which port does DNS use?” — ✅ 53 (UDP/TCP both)  
- “Which protocol is used for secure file transfer?” — ✅ SFTP (over SSH)