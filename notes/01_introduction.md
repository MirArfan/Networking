# 🌐 Computer Networking
### 🔹 What is Networking?


**Computer Networking** is the process of **connecting two or more computers or devices** to **share data and resources** (like files, printers, or the internet).




### 🔹 Types of Networks

| Type | Full Form | English Description | বাংলা ব্যাখ্যা | Example |
|------|------------|----------------------|----------------|----|
| **PAN** | Personal Area Network | Very small network like Bluetooth | ছোট পরিসরের নেটওয়ার্ক, যেমন Bluetooth |  Bluetooth between phone & earphone ,USB tethering between mobile & laptop|
| **LAN** | Local Area Network | Within a building or office | এক বিল্ডিং বা অফিসের মধ্যে ব্যবহৃত নেটওয়ার্ক | Office or university lab network, Home Wi-Fi router|
| **MAN** | Metropolitan Area Network | Covers a city area | শহরজুড়ে সংযোগ প্রদানকারী নেটওয়ার্ক |  City-wide Wi-Fi (e.g., Dhaka City Wi-Fi) , ISP connecting multiple offices in a city|
| **WAN** | Wide Area Network | Covers countries or continents | দেশ বা মহাদেশব্যাপী নেটওয়ার্ক (যেমন Internet) | The Internet 🌎,  Bank branch networks across countries|

<br>

### 🔹 Why is Networking Important?


**Networking** is essential because it allows computers and devices to communicate with each other, share data, and access resources efficiently. Without networking, every computer would work in isolation, and sharing information or accessing the internet would not be possible.



### 🔹 Main Reasons for Using Networking

| Purpose | English Description |
|---------|--------------------|
| **1. Communication** | Enables devices to send/receive data |
| **2. Resource Sharing** | Share printers, files, and storage |
| **3. Internet Access** | Connects systems to the global internet |
| **4. Data Sharing** | Easy transfer of files between devices |
| **5. Centralized Management** | Manage data and users from a single place |
| **6. Cost Efficiency** | Saves hardware and maintenance cost |
| **7. Collaboration** | Helps teams work together in real-time |


<br>

### 🌐 How Networking Works ?



1. **Data is Divided into Packets**  
   When you send a file or message, the data is broken into small units called packets.

2. **Packets Travel Through Network Devices**  
   Devices like routers, switches, and hubs guide the packets to their destination.

3. **IP & MAC Address Helps Delivery**  
   Each device has a unique IP address (logical) and MAC address (physical) to identify it.

4. **Protocols Ensure Proper Communication**  
   Rules called protocols (TCP, UDP, HTTP, FTP) make sure data is sent, received, and interpreted correctly.

5. **Data Reassembled at Destination** (ডেটা পুনরায় একত্রিত করা)

   Packets arrive at the target device and are reassembled to form the original message or file. ( প্যাকেটগুলো গন্তব্যে পৌঁছে পুনরায় একত্রিত হয়ে মূল ফাইল বা মেসেজ তৈরি হয়।)

<br>



### 🔹 Simple Diagram
```
[Sender Device] 
      │
      ▼
   [Packets Created]
      │
      ▼
[Switch / Router / Hub]
      │
      ▼
  [Internet / LAN]
      │
      ▼
[Receiver Device]
      │
      ▼
  [Packets Reassembled]
      │
      ▼
  [Original Data Received]

```


**ব্যাখ্যা :**  
- **Sender Device** → প্যাকেট তৈরি করে  
- **Switch/Router/Hub** → নেটওয়ার্কের মধ্য দিয়ে ডেলিভারি  
- **Receiver Device** → প্যাকেট পুনঃসংযোজন করে মূল ডেটা পায়

<br>
<br>

### 🌐 Networking Devices — Hub, Switch, Router

### 1️⃣ Hub

 
A hub is a basic networking device that connects multiple computers in a LAN.  
It broadcasts data to all devices connected to it, regardless of the destination.  
No intelligence, cannot filter or manage traffic.  
Used mostly in old networks.


Hub হলো একটি সাধারণ ডিভাইস যা একাধিক কম্পিউটারকে LAN-এ সংযুক্ত করে।  
এটি ডেটা সব ডিভাইসে পাঠায়, ঠিক কোন ডিভাইসের জন্য তা দেখেনা।  
বুদ্ধিমত্তা নেই, ট্রাফিক নিয়ন্ত্রণ করতে পারে না।  
পুরনো নেটওয়ার্কে বেশি ব্যবহৃত হতো।

**Example:**  
```
[PC1]---\
[PC2]----[Hub]---[PC3]
[PC4]---/
```


### 2️⃣ Switch
 
A switch is smarter than a hub.  
It forwards data only to the device it is intended for using MAC addresses.  
Reduces network congestion and increases efficiency.  
Commonly used in modern LANs.

 
Switch হলো Hub-এর চেয়ে বুদ্ধিমান।  
এটি ডেটা শুধু সেই ডিভাইসে পাঠায়, যার জন্য তা নির্ধারিত (MAC address ব্যবহার করে)।  
নেটওয়ার্কে congestion কমায় এবং efficiency বাড়ায়।  
আধুনিক LAN-এ Switch বেশি ব্যবহৃত হয়।

**Example:**  
```
[PC1]---\
[PC2]----[Switch]----[PC3]
[PC4]---/
```


### 3️⃣ Router

 
A router connects multiple networks together (e.g., LAN ↔ WAN).  
It routes data packets between networks using IP addresses.  
Can provide Internet access to LAN devices.  
Has advanced features like NAT, firewall, DHCP.

Router একাধিক নেটওয়ার্ককে সংযুক্ত করে (যেমন LAN ↔ WAN)।  
এটি IP address ব্যবহার করে নেটওয়ার্কের মধ্যে ডেটা পাঠায়।  
LAN ডিভাইসকে ইন্টারনেট সংযোগ দিতে পারে।  
NAT, firewall, DHCP এর মতো advanced feature থাকে।

**Example:**  
```
[LAN Devices] --- [Router] --- [Internet]
```

### 🔹 Key Differences (Hub vs Switch vs Router)

| Feature          | Hub                 | Switch                        | Router                        |
|-----------------|-------------------|-------------------------------|-------------------------------|
| Works at        | Physical Layer      | Data Link Layer               | Network Layer                 |
| Intelligence    | None               | Medium (MAC based)            | High (IP based)               |
| Traffic         | Broadcasts to all  | Sends to specific device      | Routes between networks       |
| Common Use      | Old LANs           | Modern LANs                   | LAN ↔ WAN / Internet


### 🌐 Network Flow with Hub, Switch & Router



**Hub**  
- Connects multiple devices in a LAN.  
- Broadcasts data to all devices.  
- Simple, no intelligence.  

**Switch**  
- Connects multiple devices in a LAN.  
- Sends data only to the intended device using MAC addresses.  
- Reduces congestion, more efficient.  

**Router**  
- Connects LAN to other networks or the Internet.  
- Routes data using IP addresses.  
- Provides features like NAT, DHCP, firewall.  

**Flow of Data:**  
User sends data from a device → Hub/Switch forwards inside LAN → Router sends to Internet or another network → Destination device receives.


<br>

### 🔹 Diagram — Network Flow
```
[PC1]        [PC2]        [PC3]
   \           |           /
    \          |          /
     \         |         /
      ----[Switch]------
             |
             |
           [Router]------[Internet]
             |
        [Other LAN/Devices]
```

**Explanation:**  
- **PC1, PC2, PC3** → LAN devices  
- **Switch** → Sends data only to correct device inside LAN  
- **Router** → Routes data outside LAN (Internet / another network)  
- **Internet** → External network or another office

<br>
<br>

### 🔹 What is Network Topology?

**English:**  
**Network Topology** is the physical or logical layout of devices (computers, printers, switches, routers) in a network and how they are connected to each other.

 
নেটওয়ার্ক টপোলজি হলো নেটওয়ার্কের ডিভাইস (কম্পিউটার, প্রিন্টার, সুইচ, রাউটার) গুলোর ভৌত বা লজিক্যাল বিন্যাস এবং তারা একে অপরের সাথে কিভাবে সংযুক্ত আছে।



### 🔹 Types of Network Topology

| Topology |  Description | ব্যাখ্যা | Example |
|----------|-------------------|----------------|----------------|
| Bus | All devices share a single backbone cable. | সব ডিভাইস একটিমাত্র কেবলের সাথে সংযুক্ত। | পুরনো LAN networks (Ethernet 10Base2, 10Base5), Small office networks using coaxial cable |
| Star | All devices connect to a central hub/switch. | প্রতিটি ডিভাইস একটি কেন্দ্রীয় হাব/সুইচের সাথে সংযুক্ত। | আধুনিক অফিস বা ঘরের LAN (Wi-Fi router বা switch দ্বারা),  Example: অফিসে সব কম্পিউটার switch এ যুক্ত |
| Ring | Devices connected in a circular path. | ডিভাইসগুলো একটি বৃত্তাকার পথে সংযুক্ত। | IBM Token Ring Network, কিছু মেট্রো রেল নেটওয়ার্কে fiber optic ring ব্যবহার |
| Mesh | Every device connected to every other device. | প্রতিটি ডিভাইস অন্য প্রতিটি ডিভাইসের সাথে সংযুক্ত। |Internet backbone networks,  Military communication networks (redundancy দরকার বলে)|
| Tree | Hierarchical structure; multiple star topologies connected. | একাধিক Star topology-এর হায়ারার্কিকাল সংযোগ। | University networks (Central router → department switches → lab PCs),  Corporate branch network |
| Hybrid | Combination of two or more topologies. | বিভিন্ন ধরনের টপোলজির সংমিশ্রণ। | Large enterprise networks (Star + Bus বা Star + Mesh), Internet service provider (ISP) networks |



### 🔹 Advantages & Disadvantages

| Topology | Advantage | Disadvantage |
|----------|-----------|--------------|
| Bus | Simple & cheap | Hard to troubleshoot, congestion |
| Star | Easy to manage, failure of one device doesn’t affect others | Needs more cable, central hub dependency |
| Ring | Data flows in one direction, orderly | Failure in one node can disrupt network |
| Mesh | Highly reliable, fault tolerant | Expensive, complex |
| Tree | Scalable, hierarchical | If root fails, whole network affected |
| Hybrid | Flexible & scalable | Complex to design |




