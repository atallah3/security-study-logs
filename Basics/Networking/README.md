# Network

- A **network** allows multiple systems or devices to communicate and share resources.
- The **OSI (Open Systems Interconnection) Model** is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers.

### OSI Model Layers (from bottom to top):

1. **Physical Layer**
2. **Data Link Layer**
3. **Network Layer**
4. **Transport Layer**
5. **Session Layer**
6. **Presentation Layer**
7. **Application Layer**

---

## Physical Layer (Layer 1)

- Responsible for the transmission and reception of unstructured raw data between a device and a physical transmission medium.
- Defines electrical and physical specifications for devices.
- Examples: cables, switches, voltage levels, and connectors.

### Network Topologies:

### 1. Star Topology

- All devices are connected to a central hub or switch.
- Easy to manage and expand, but the failure of the hub brings down the network.

### 2. Ring Topology

- Each device connects to two other devices, forming a circular path.
- Data travels in one or both directions; failure in one connection can disrupt the network.

### 3. Bus Topology

- All devices share a single communication line.
- Inexpensive and simple but difficult to troubleshoot.

### 4. Mesh Topology

- Every device is connected to every other device.
- Provides high redundancy and fault tolerance but is expensive.

### 5. Hybrid Topology

- A combination of two or more topologies.
- Used in large organizations for scalability and reliability.

---

## Data Link Layer (Layer 2)

- Ensures reliable node-to-node communication within the same network.
- Responsible for MAC (Media Access Control) addressing and error detection.

### Key Concepts:

- **MAC Address**: A unique identifier assigned to network interfaces.
- **Switches** and **Access Points** operate at this layer.
- **Frames** are the units of data at this layer.

### ARP (Address Resolution Protocol):

- Maps IP addresses (Layer 3) to MAC addresses (Layer 2).

**Example Workflow:**

1. Host A sends an ARP request: "Who has IP 192.168.1.3?"
2. Host B responds with its MAC address.
3. Host A stores this mapping and communicates directly via MAC.

### ARP Issues:

- **Broadcast Overhead**: ARP requests are sent to all devices.
- **Spoofing Vulnerability**: No authentication in ARP responses.

---

## Network Layer (Layer 3)

- Handles routing of data (**packets**) across different networks.
- Uses IP addressing to identify devices.

### IPv4 Addressing:

- Format: xxx.xxx.xxx.xxx (0-255 per octet) 32 bit
- Each IP has a **Network** and **Host** portion.

**IPv4 uses decimal notation (e.g., “192.168.** **1.1”), while IPv6 employs hexadecimal format (e.g., “2001:0db8:85a3:0000:0000:8a2e:0370:7334”)**

### Reserved Ranges:

- **Multicast**: 224.0.0.0 – 239.255.255.255
- **Loopback**: 127.0.0.0 – 127.255.255.255
- **Broadcast**: 255.255.255.255

### Subnet Mask:

- Determines how IP address is divided into network and host.
- Examples:
    - Class A: 255.0.0.0
    - Class B: 255.255.0.0
    - Class C: 255.255.255.0

### CIDR (Classless Inter-Domain Routing):

- Alternative to class-based IP addressing.
- Format: `IP_address/PrefixLength` (e.g., 192.168.1.0/24)

### Default Gateway:

- A default gateway is **the IP address of a router that acts as the entry or exit point for network traffic, especially when a device doesn't know the specific route to its destination**
    
    ### Is the default gateway always the first IP?
    
     **Often yes, but not always.**
    
    - It’s **common** for network admins to assign the first usable IP in a subnet to the router.
    - For example, in a home network like `192.168.1.0/24`:
        - The first usable IP is `192.168.1.1`
        - So, the default gateway is **usually** `192.168.1.1`

### What is the **Broadcast Address**?

The **broadcast address** is the **last IP address** in any subnet.

It’s used to **send data to all devices** on the network at once.

### DHCP (Dynamic Host Configuration Protocol):

- Automatically assigns IP, subnet mask, gateway, and DNS.
- It simplifies IP address management by dynamically allocating addresses to devices as they connect to the network.

**DHCP Process:**

1. Client sends DHCP Discover
2. Server replay with DHCP Offer
3. Client sends DHCP Request
4. Server replay with the parameters DHCP Acknowledge

### Routing:

- **the process of selecting a path for data packets to travel from their source to their destination across a network**
- Directs packets across networks using routers.
- **Routing Table**: Guides packets to next hop.
- **TTL (Time To Live)**: Prevents infinite loops.

### Routing Protocols:

- **RIP (Routing Information Protocol)**
- **OSPF (Open Shortest Path First)**
- **BGP (Border Gateway Protocol)**

### NAT (Network Address Translation):

- Converts private IPs to public for internet communication.
- **When a device on the private network sends data to a device on the public network, the router intercepts the data and replaces the source IP address with its own public IP address**

---

## Transport Layer (Layer 4)

- Ensures complete data transfer.
- Manages error detection, retransmission, and flow control.

### Protocols:

### TCP (Transmission Control Protocol)

- Reliable, connection-oriented.
- Three-Way Handshake:
    1. SYN
    2. SYN-ACK
    3. ACK

### UDP (User Datagram Protocol)

- Unreliable, connectionless.
- Faster but no guarantee of delivery.

---

##  **Session Layer (Layer 5)**

###  **What it does:**

- Establishes, manages, and terminates **communication sessions** between two devices.
- Ensures **synchronized and organized communication**.
- Manages **session recovery** (resumes a broken connection without restarting from scratch).
- Supports **duplex or half-duplex** data transmission (who talks when).

### **Real-world examples:**

- Think of a Zoom call, online game, or any app that needs a **persistent session** between two endpoints.

### **Responsibilities:**

- Session establishment, maintenance, and teardown.
- Token management (who can speak).
- Synchronization (checkpoints in large data transfers).

---

## **Presentation Layer (Layer 6)**

### **What it does:**

- Converts data into a format that the **Application Layer** can understand.
- Responsible for **data representation, encoding, and decoding**.
- Applies **encryption**, **compression**, or **format translation**.

### **Real-world examples:**

- Converts video/audio into proper codecs for communication (e.g., `.mp4`, `.aac`).
- Handles SSL/TLS encryption before data is handed off to the application.
- Converts between different character sets (ASCII, Unicode).

### **Responsibilities:**

- Encryption/Decryption (e.g., TLS/SSL).
- Compression/Decompression (e.g., zlib).
- Data translation (e.g., encoding formats for media, XML, JSON parsing).

---

## **Application Layer (Layer 7)**

### **What it does:**

- Closest to the **end user**.
- Provides interfaces for user applications to access the network.
- Interacts with lower layers to complete tasks like **sending emails**, **browsing the web**, or **transferring files**.

### **Real-world examples:**

- When you open a browser and access `www.google.com` — your browser is an Application Layer client using HTTP.

### **Responsibilities:**

- Identifying communication partners
- Resource availability checking
- Ensuring authentication and privacy
- Managing application-level data integrity

---

---

---

---

### What is SSH?

**SSH** stands for **Secure Shell**.

It’s a **protocol** (like HTTP or FTP) used to **securely connect** from one computer to another — usually to control a remote machine (like a server).

---

---

### What does SSH let you do?

With SSH, you can:

- **Login to a remote computer** (like a server on the cloud)
- **Run commands** on that remote computer
- **Transfer files** securely (with tools like `scp` or `sftp`)
- **Create tunnels** to encrypt traffic (used in DevOps and hacki

### SSH has two ways to authenticate:

### Option 1: **Password-based login**

- You type your password manually when connecting:
    
    ```bash
    ssh user@server
    ```
    
    and it asks:
    
    ```css
    user@server's password:
    ```
    

> In this case, the password is not stored anywhere unless you're using a password manager or some automation script.
> 

---

### Option 2: **Key-based login (no password needed)**

- You use a private key (`id_rsa`), like:
    
    ```bash
    ssh -i id_rsa user@server
    ```
    
- If the key is set up properly, no password is asked at all.
- 🔒 **Sometimes**, the key itself is protected by a passphrase. You'd be asked:
    
    ```css
    Enter passphrase for key 'id_rsa':
    ```
    

---

---

## **Most Famous Networking Protocols (with Explanation)**

### 1. **HTTP (HyperText Transfer Protocol)**

**Definition:**

HTTP is a request-response protocol used by web browsers and servers to exchange text, media, and documents over the web.

- **Port:** 80 (TCP)
- **Purpose:** Transfers web pages and resources (HTML, CSS, JS, images).
- **Note:** Stateless and unencrypted — doesn't maintain user session or protect data.
- **stateless means a system doesn't store information about past interactions or transactions**
- **Vulnerabilities:** Sensitive data exposure, injection attacks, CSRF.

---

### 2. **HTTPS (HTTP Secure)**

**Definition:**

HTTPS is the encrypted version of HTTP that uses SSL/TLS to secure the communication channel between client and server.

- **Port:** 443 (TCP)
- **Purpose:** Secure communication over the web (e.g., logins, transactions).
- **Note:** Ensures encryption, authentication, and integrity.
- **Vulnerabilities:** SSL misconfigurations, expired certificates, downgrade attacks.

---

### 3. **FTP (File Transfer Protocol)**

**Definition:**

FTP is a protocol for transferring files between a client and server on a network.

- **Ports:** 21 (control), 20 (data) — TCP
- **Purpose:** Upload and download files from/to a server.
- **Note:** Transmits credentials and data in plaintext.
- **Secure Alternatives:** FTPS (FTP over SSL), SFTP (over SSH).
- **Vulnerabilities:** Credential sniffing, brute-force, directory traversal.

---

### 4. **SSH (Secure Shell)**

**Definition:**

SSH is a secure protocol for remotely accessing and managing devices using encrypted communication.

- **Port:** 22 (TCP)
- **Purpose:** Remote login, file transfer (SCP/SFTP), and secure tunneling.
- **Note:** Strong encryption but may be vulnerable to brute-force if weak passwords used.
- **Vulnerabilities:** Brute force attacks, poor key management, outdated algorithms.

---

### 5. **DNS (Domain Name System)**

**Definition:**

DNS is a system that translates human-readable domain names (like `google.com`) into IP addresses used by computers.

- **Port:** 53 (UDP for queries, TCP for zone transfers)
- **Purpose:** Resolves domain names to IPs.
- **Note:** Critical for internet navigation.
- **Vulnerabilities:** DNS spoofing, cache poisoning, subdomain enumeration, zone transfer attacks.

---

### 6. **SMTP (Simple Mail Transfer Protocol)**

**Definition:**

SMTP is used to send outgoing emails from a client to a mail server or between mail servers.

- **Ports:** 25 (standard), 587 (with STARTTLS), 465 (SMTPS)
- **Purpose:** Email delivery across servers.
- **Note:** Needs encryption (STARTTLS or SMTPS) to avoid plain text exposure.
- **Vulnerabilities:** Open relays, email spoofing, spam relay, lack of encryption.

---

### 7. **POP3 (Post Office Protocol v3)**

**Definition:**

POP3 is used by email clients to retrieve emails from the server and download them locally.

- **Port:** 110 (TCP), 995 (with SSL/TLS)
- **Purpose:** Access emails in a download-and-delete model.
- **Note:** Suitable for single-device access; lacks sync support.
- **Vulnerabilities:** Plaintext authentication unless SSL is enforced.

---

### 8. **IMAP (Internet Message Access Protocol)**

**Definition:**

IMAP allows an email client to access and manage emails stored on a mail server, supporting multiple devices and syncing.

- **Port:** 143 (TCP), 993 (with SSL/TLS)
- **Purpose:** View, organize, and manage emails without downloading them.
- **Note:** Allows full mailbox access across devices.
- **Vulnerabilities:** Similar to POP3 unless SSL/TLS is used.

---

### 9. **DHCP (Dynamic Host Configuration Protocol)**

**Definition:**

DHCP is used to automatically assign IP addresses and other network configuration settings to devices on a network.

- **Ports:** 67 (server), 68 (client) — UDP
- **Purpose:** Automatically assigns IP, subnet mask, default gateway, and DNS server.
- **Note:** Essential for large networks to avoid manual IP configuration.
- **Vulnerabilities:** Rogue DHCP servers, DHCP starvation, IP conflicts.
