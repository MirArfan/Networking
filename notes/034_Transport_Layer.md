
### 🚚 Transport Layer — OSI Model (Layer 4)


### 🧩 Overview
 
The **Transport Layer** is the 4th layer of the OSI model.  
It is responsible for **end-to-end communication**, **data segmentation**, **error control**, and **flow control** between devices.

 
Transport Layer হলো OSI Model-এর ৪র্থ স্তর।  
এই স্তরের কাজ হলো ডেটা এক প্রান্ত থেকে অন্য প্রান্তে নির্ভরযোগ্যভাবে পাঠানো, ডেটাকে ছোট ছোট অংশে ভাগ করা (segmentation), এবং error ও flow control করা।



### ⚙️ Main Functions of Transport Layer

| Function |  Explanation |  ব্যাখ্যা |
|-----------|---------------------|----------------|
| **Segmentation & Reassembly** | Divides data into smaller segments before transmission, and reassembles them at destination. | ডেটাকে ছোট ছোট অংশে ভাগ করে পাঠানো এবং গন্তব্যে পৌঁছে আবার একত্র করা। |
| **End-to-End Delivery** | Ensures data is delivered from one device to another device correctly. | এক ডিভাইস থেকে অন্য ডিভাইসে ডেটা সঠিকভাবে পৌঁছানো নিশ্চিত করে। |
| **Error Control** | Detects and retransmits lost or corrupted data segments. | ডেটা হারালে বা নষ্ট হলে পুনরায় পাঠায়। |
| **Flow Control** | Controls the rate of data transmission so that receiver is not overloaded. | রিসিভার যেন অতিরিক্ত ডেটা না পায়, তা নিশ্চিত করে। |
| **Connection Control** | Can provide connection-oriented (reliable) or connectionless (fast) service. | সংযোগযুক্ত (TCP) বা সংযোগবিহীন (UDP) পরিষেবা প্রদান করে। |

<br>

### 🔗 Protocols Used in Transport Layer

| Protocol | Type | Description | বাংলা ব্যাখ্যা |
|-----------|------|-------------|----------------|
| **TCP (Transmission Control Protocol)** | Connection-Oriented | Reliable, ensures error-free, ordered delivery. | নির্ভরযোগ্য প্রোটোকল; ডেটা ঠিকঠাক ও ক্রম অনুসারে পৌঁছে দেয়। |
| **UDP (User Datagram Protocol)** | Connectionless | Faster, but no guarantee of delivery. | দ্রুত কিন্তু ডেটা হারানোর সম্ভাবনা থাকে। |



### 🧠 Difference Between TCP and UDP

| Feature | **TCP** | **UDP** |
|----------|----------|----------|
| Type | Connection-oriented | Connectionless |
| Reliability | Reliable (acknowledgment-based) | Unreliable |
| Speed | Slower | Faster |
| Error Control | Yes | No |
| Example Uses | Web browsing (HTTP), Email (SMTP), File transfer (FTP) | Video streaming, Online games, VoIP |



### 🧭 Example Flow

### 🖥️ Example: Sending an Email
1. Data created in Application Layer (SMTP).
2. Transport Layer breaks it into **segments** using TCP.
3. Each segment gets a **port number** (e.g., port 25 for SMTP).
4. Network Layer adds IP address.
5. Data travels through the network.
6. Receiver’s Transport Layer reassembles segments → passes to Application Layer.



### 🔢 Important Terms

| Term | Meaning |  ব্যাখ্যা |
|------|----------|----------------|
| **Port Number** | Identifies a specific application/service on a device. | ডিভাইসের নির্দিষ্ট সার্ভিস বা অ্যাপকে চিহ্নিত করে। |
| **Segment** | Data unit at Transport Layer (in TCP). | Transport Layer-এ ডেটার ইউনিট। |
| **Datagram** | Data unit at Transport Layer (in UDP). | UDP তে ডেটার ইউনিট। |
| **Socket** | Combination of IP address + Port number. | IP ঠিকানা ও পোর্ট নাম্বারের মিশ্রণ। |



### 🧩 Common Port Numbers

| Protocol | Port | Description |
|-----------|------|-------------|
| HTTP | 80 | Web traffic |
| HTTPS | 443 | Secure web traffic |
| FTP | 21 | File transfer |
| SMTP | 25 | Email sending |
| DNS | 53 | Domain name resolution |


### 💡 Summary

- Layer 4 of OSI Model.  
- Ensures **reliable, ordered, and error-free** delivery (TCP).  
- Provides **fast, lightweight communication** when reliability isn’t critical (UDP).  
- Handles **ports, segmentation, and flow control.**
