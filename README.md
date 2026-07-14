# 🌐 My Cybersecurity & CompTIA Network+ Journey

This repository serves as my official study notebook and practical portfolio, tracking my progress from foundational security principles to advanced networking and cloud operations.

## 🛡️ Cybersecurity Fundamentals
* **The Three Tiers of Cybersecurity:** Core operational framework focusing on confidentiality, integrity, and availability (CIA Triad) to protect data and assets.
* **Types of Hackers:** Understanding threat actors by motivation and authorization, including White Hat (ethical), Black Hat (malicious), and Grey Hat hackers.

## 🧩 Comprehensive Networking Foundations
* **Seven Layers of Computer Communication:** The 7 layers of the OSI model detailing how data is structured, transmitted, and received across systems.
* **Networking Devices:** Physical and logical infrastructure components (routers, switches, firewalls, and access points) used to connect and segment networks.
* **Networking Functions:** Core transport services and optimizations driving data delivery:
* **CDN (Content Delivery Network):** Distributes content globally to minimize latency.
* **QoS (Quality of Service):** Prioritizes critical traffic (like voice/video) over standard data.
* **VPN (Virtual Private Network):** Establishes encrypted, secure tunnels across public networks.
* **TTL (Time to Live):** Prevents infinite routing loops by setting a packet expiration limit.
* **DNS (Domain Name System):** Resolves human-readable domain names into machine-readable IP addresses.

## ☁️ Cloud Infrastructure Architecture
Modern deployment, containment, and transit models used to design secure virtual environments:
* **Virtual Network & VPC (Virtual Private Cloud):** Logically isolated, private networks built within a public cloud environment.
* **Network Function Virtualization (NFV):** Replacing dedicated physical hardware appliances with software-based virtual instances.
* **Transit Gateway:** Central hub connecting multiple Virtual Private Clouds (VPCs) and on-premises networks together.
* **VPC Gateway & VPC NAT Gateway:** Structural entryways managing inbound internet routing and allowing private subnet resources to reach the internet safely.
* **VPC Endpoint:** Establishes private, secure connections to cloud services without exposing traffic to the public internet.


### ☁️ Cloud Architecture & Deployment Models
*These models define the distribution of management responsibilities and the physical location of infrastructure in cloud computing.*

#### 🏢 Cloud Service Models (The "As a Service" Frameworks)
* **IaaS (Infrastructure as a Service):** The provider hosts the raw hardware, storage, and networking components. You are fully responsible for installing, securing, and maintaining the **Operating System (OS)** and applications.
* **PaaS (Platform as a Service):** The provider manages the hardware and the underlying operating system. They deliver a ready-to-use sandbox framework specifically designed for **software developers** to deploy and run custom application code.
* **SaaS (Software as a Service):** The provider completely builds, hosts, updates, and manages the entire software stack. End-users simply log into a **finished web application** (e.g., Microsoft 365, Gmail) via a browser.

#### 🌐 Cloud Deployment Models (The Physical Environments)
* **Public Cloud:** Computing resources are owned and operated by a third-party vendor (e.g., AWS, Azure, Google Cloud) and shared among multiple organizations over the public internet.
* **Private Cloud:** Computing resources are completely dedicated to, owned by, and operated within a single organization's secure, internal data center.
* **Hybrid Cloud:** A combined infrastructure architecture that securely connects private cloud resources with public cloud platforms to share data and applications.


Core 20 Protocols & Port Dynamics

A comprehensive reference guide for mastering core network protocols, port mappings, and transport layer mechanics required for the CompTIA Network+ exam.

## 🛠️ Core Transport Mechanics

### 1. Delivery Logic
* **TCP (Transmission Protocol):** Connection-oriented. Establishes a session before sending data. Guarantees delivery, performs error-checking, and manages flow control. Slower due to overhead.
* **UDP (User Datagram Protocol):** Connectionless. "Fire-and-forget" delivery logic. No handshake or delivery confirmation. Faster performance with minimal overhead.

### 2. Connection Handshakes
* **The 3-Way Handshake (TCP Establish):** SYN ➡️ SYN-ACK ➡️ ACK
* **The 4-Way Handshake (TCP Teardown/Close):** FIN ➡️ ACK ➡️ FIN ➡️ ACK

---

## 💻 The 10 Core Network Command Prompt Utilities
The definitive suite of native command-line interface tools used for network diagnostics,troubleshooting, security auditing, and verification. (Use the `/?` help switch after any command to view its hidden variety configurations and flags).

1. `ipconfig` — Audits local network interface cards, subnets, and active default gateways.
2. `ping` — Tests device connectivity (tested via loopback 127.0.0.1, the default gateway, and external 8.8.8.8).
3. `tracert` — Traces every hop router path to isolate where traffic drops occur across the WAN.
4. `nslookup` — Interrogates DNS servers to audit name-to-IP resolution mechanics.
5. `netstat` — Audits all active network connections, routing tables, and listening daemon ports on the system.
6. `arp` — Reveals the local network table mapping IP addresses to physical MAC hardware addresses.
7. `route` — Displays and manipulates your computer's internal network traffic routing tables.
8. `hostname` — Instantly prints out the unique network identification name of your computer.
9. `pathping` — A hybrid tool that combines ping and tracert to pinpoint exact packet loss locations.
10. `nbtstat` — Troubleshoots NetBIOS over TCP/IP name resolutions on legacy infrastructure networks.



## 🌐 Protocol & Port Master Matrix

### Web & File Transfer

| Protocol | Full Meaning | Port | Transport | Security Status | Architectural Vulnerability / Security Mechanism |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **HTTP** | Hypertext Transfer Protocol | 80 | TCP | ❌ Not Secure | Transmits data in cleartext; vulnerable to packet sniffing. |
| **HTTPS** | Hypertext Transfer Protocol Secure | 443 | TCP | ✅ Secure | Encrypts all traffic using SSL/TLS algorithms. |
| **FTP** | File Transfer Protocol | 20, 21 | TCP | ❌ Not Secure | Authentication credentials and data payloads move in cleartext. |
| **SFTP** | Secure File Transfer Protocol | 22 | TCP | ✅ Secure | Encrypts both credentials and files inside an SSH tunnel. |
| **TFTP** | Trivial File Transfer Protocol | 69 | UDP | ❌ Not Secure | Zero built-in security; no password authentication or encryption. |

### Remote Management

| Protocol | Full Meaning | Port | Transport | Security Status | Architectural Vulnerability / Security Mechanism |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SSH** | Secure Shell | 22 | TCP | ✅ Secure | Uses public-key cryptography to encrypt command-line sessions. |
| **Telnet** | Telecommunication Network | 23 | TCP | ❌ Not Secure | Transmits administrative credentials in plain text over the wire. |
| **RDP** | Remote Desktop Protocol | 3389 | TCP | ✅ Secure | Uses built-in RSA/AES encryption to secure the graphical stream. |

### Email

| Protocol | Full Meaning | Port | Transport | Security Status | Architectural Vulnerability / Security Mechanism |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SMTP** | Simple Mail Transfer Protocol | 25 | TCP | ❌ Not Secure | Relays messages between mail servers without transport encryption. |
| **POP3** | Post Office Protocol v3 | 110 | TCP | ❌ Not Secure | Downloads email to host while exposing cleartext passwords. |
| **IMAP** | Internet Message Access Protocol | 143 | TCP | ❌ Not Secure | Syncs mailboxes across endpoints but lacks default text encryption. |

### Infrastructure & Directory Services

| Protocol | Full Meaning | Port | Transport | Security Status | Architectural Vulnerability / Security Mechanism |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **DNS** | Domain Name System | 53 | Both | ❌ Not Secure | Queries are unencrypted; vulnerable to eavesdropping and spoofing. |
| **DHCP** | Dynamic Host Config. Protocol | 67, 68 | UDP | ❌ Not Secure | No authentication; vulnerable to rogue servers and MITM attacks. |
| **NTP** | Network Time Protocol | 123 | UDP | ❌ Not Secure | Lacks source validation; vulnerable to time tampering and DDoS amplification. |
| **LDAP** | Lightweight Directory Access Protocol | 389 | TCP | ❌ Not Secure | Active Directory queries and network logins are sent in cleartext. |
| **LDAPS** | Lightweight Directory Access Protocol Secure | 636 | TCP | ✅ Secure | Wraps directory communication inside an SSL/TLS tunnel. |

### Management, Sharing & VoIP

| Protocol | Full Meaning | Port | Transport | Security Status | Architectural Vulnerability / Security Mechanism |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SNMP** | Simple Network Management Protocol | 161, 162 | UDP | ❌ Not Secure | Versions 1 and 2 pass passwords in plain text. (v3 adds encryption). |
| **SMB** | Server Message Block | 445 | TCP | ❌ Not Secure | Legacy versions (SMBv1) lack encryption and contain exploits. (v3 encrypts). |
| **Syslog** | System Log | 514 | UDP | ❌ Not Secure | Transmits highly sensitive network system logs completely unencrypted. |
| **SIP** | Session Initiation Protocol | 5060, 5061 | Both | Mixed | Port 5060 sets up VoIP sessions in cleartext. Port 5061 uses TLS to encrypt. |

---

## 💡 Rapid Identification Mental Models

1. **The "S" Suffix Rule:** If the acronym ends with **S**, it relies on **SSL/TLS encryption** (e.g., HTTPS, LDAPS).
2. **The "S" Prefix Rule:** If it handles file or console interaction and begins with **S**, it relies on **SSH tunnel encryption** (e.g., SSH, SFTP).
3. **The RDP Outlier:** **RDP (3389)** features no "S" in its name but natively enforces transport-layer encryption.
4. **Core UDP Exceptions:** **DHCP (67/68)**, **TFTP (69)**, **NTP (123)**, **SNMP (161/162)**, and **Syslog (514)** do not establish TCP sessions due to overhead speed constraints or architectural limitations.


### 🌐 other Networking Protocols
- **ICMP (Internet Control Message Protocol):** Learned how ICMP is used for network diagnostics, error reporting, and connectivity testing through tools like `ping`.
- **GRE (Generic Routing Encapsulation):** Studied how GRE creates tunnels to encapsulate different network protocols across IP networks.
- **IPsec (Internet Protocol Security):** Explored how IPsec secures network communications by providing confidentiality, integrity, and authentication.
- **IKE Phase 1 & Phase 2:** Learned how Internet Key Exchange (IKE) negotiates secure connections and establishes cryptographic keys for IPsec tunnels.
- **ESP (Encapsulating Security Payload):** Provides encryption, authentication, and data integrity for secure communication.
- **AH (Authentication Header):** Provides authentication and integrity verification without encrypting the data.

### 📡 Network Communication Methods
- **Unicast:** One sender communicates with one receiver.
- **Broadcast:** One sender communicates with every device on the local network.
- **Multicast:** One sender communicates with a selected group of receivers.
- **Anycast:** Multiple devices share the same address, and traffic is delivered to the nearest or best destination.

### 🔌 Fiber Optic Networking
- **Single-Mode Fiber (SMF):** Supports long-distance communication using a narrow core and laser light.
- **Multi-Mode Fiber (MMF):** Designed for shorter distances using a wider core and LED or VCSEL light sources.
- **Fiber Transceivers:** Learned how SFP, SFP+, and QSFP modules convert electrical signals into optical signals for fiber communication.

### 🕸️ Network Topologies
- **Bus Topology:** All devices share a single communication cable.
- **Star Topology:** Devices connect through a central switch or hub.
- **Ring Topology:** Devices form a circular path for data transmission.
- **Mesh Topology:** Multiple redundant connections improve reliability and fault tolerance.
- **Tree Topology:** A Hierarchy topology that connects multiple star networks, making it scalable for large oragnization
- **Hybrid Topology:** A combination of two or more top[ology desinged to meet organization requirement 

### 🧮 Binary Mathematics
- Strengthened my understanding of decimal-to-binary and binary-to-decimal conversions.
- Practiced binary arithmetic and bit values used in IPv4 addressing and subnetting.

### 🌍 IPv4 Addressing & Classful Subnetting
- Learned the structure of IPv4 addresses and the purpose of subnet masks.
- Studied Class A, Class B, and Class C networks and their default subnet masks.
- Practiced identifying network and host portions of IP addresses using classful subnetting.
- Learned the purpose of IPv4 subnet masks and how they separate network and host portions of an IP address.
- Studied CIDR notation and converted prefix lengths into their corresponding subnet masks.
- Calculated borrowed bits, remaining host bits, number of subnets, and usable hosts using subnetting formulas.
- Identified the interesting octet and applied the Magic Number Method to determine subnet boundaries.
- Practiced calculating network addresses, broadcast addresses, first usable hosts, and last usable hosts for Class B and Class C networks.
- Strengthened subnetting skills through repeated hands-on exercises, improving both accuracy and confidence in subnet calculations.
- Explored the concept of Seven-Second Subnetting and understood how subnetting speed techniques are built upon strong subnetting fundamentals.

