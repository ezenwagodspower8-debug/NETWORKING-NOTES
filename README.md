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



Modern Network Architecture Documentation
Overview
Modern networks have evolved from traditional hardware-based architectures into software-driven, automated, and security-focused environments. Technologies such as Software-Defined Networking (SDN), Software-Defined Wide Area Networking (SD-WAN), Data Center Interconnect (DCI), VXLAN, Secure Access Service Edge (SASE), and Infrastructure as Code (IaC) are designed to improve scalability, flexibility, automation, and security.

1. Software-Defined Networking (SDN)
Definition
Software-Defined Networking (SDN) is a network architecture that separates the control plane from the data plane.

Traditional networks have each device making independent decisions. SDN centralizes network intelligence into a software-based controller that manages network devices.

SDN Components
Control Plane
The control plane makes decisions about where traffic should go.

Example:

Routing decisions
Network policies
Traffic management
Data Plane
The data plane is responsible for forwarding packets based on instructions from the control plane.

Example:

Switches forwarding traffic
Routers moving packets between networks
SDN Controller
The SDN controller acts as the brain of the network. It communicates with network devices and applies policies across the infrastructure.

Examples of SDN controllers:

OpenDaylight
Cisco DNA Center
Benefits of SDN
Centralized network management
Easier automation
Improved scalability
Faster network configuration
Better visibility and monitoring
Importance in Cybersecurity
SDN improves security by allowing administrators to create centralized security policies, monitor traffic patterns, and quickly isolate suspicious devices.

2. Software-Defined Wide Area Networking (SD-WAN)
Definition
SD-WAN is a software-based approach to managing Wide Area Networks. It uses centralized control to manage connections between different locations such as branch offices, data centers, and cloud environments.

Traditional WANs often rely on expensive MPLS connections. SD-WAN can intelligently use multiple connections such as:

MPLS
Broadband Internet
LTE/5G
How SD-WAN Works
SD-WAN uses software intelligence to select the best path for traffic based on:

Latency
Bandwidth
Packet loss
Application requirements
Example:

A video conference may use the fastest available connection, while email traffic may use a cheaper path.

Benefits of SD-WAN
Reduced WAN costs
Improved application performance
Centralized management
Better cloud connectivity
Automatic traffic optimization
SD-WAN and Security
Many SD-WAN solutions include security features such as encryption, firewalls, and integration with SASE architectures.

3. Data Center Interconnect (DCI)
Definition
Data Center Interconnect (DCI) is a technology used to connect multiple data centers together over high-speed networks.

Organizations use DCI to allow different data centers to communicate and share resources.

Why DCI is Needed
Large organizations may have:

Primary data centers
Backup data centers
Disaster recovery locations
Cloud environments
DCI allows these locations to operate together.

DCI Technologies
Examples include:

Optical fiber connections
MPLS
Ethernet-based connections
VPN technologies
Benefits of DCI
Disaster recovery
Data replication
High availability
Load balancing between data centers
4. VXLAN (Virtual Extensible LAN)
Definition
VXLAN is a network virtualization technology that extends Layer 2 networks across Layer 3 networks.

Traditional VLANs have a limitation of approximately 4,000 VLAN IDs. VXLAN increases scalability by supporting millions of virtual networks.

How VXLAN Works
VXLAN creates a virtual tunnel between network devices using VXLAN Tunnel Endpoints (VTEPs).

The original Ethernet frame is encapsulated inside a UDP packet and transported across an IP network.

VXLAN Components
VTEP (VXLAN Tunnel Endpoint)
A device responsible for:

Encapsulating traffic
Decapsulating traffic
Mapping VLANs to VXLAN segments
VNI (VXLAN Network Identifier)
The VNI identifies the VXLAN segment.

Benefits of VXLAN
Large-scale network virtualization
Data center scalability
Supports cloud environments
Allows workload mobility
Relationship Between VXLAN and DCI
DCI connects different data centers, while VXLAN allows virtual networks to extend across those data centers.

5. Secure Access Service Edge (SASE)
Definition
Secure Access Service Edge (SASE) is a cybersecurity architecture that combines networking and security services into a cloud-based solution.

SASE was created because users and applications are no longer located only inside traditional corporate networks.

SASE Components
SD-WAN
Provides intelligent network connectivity.

Security Services
Examples:

Secure Web Gateway (SWG)
Cloud Access Security Broker (CASB)
Zero Trust Network Access (ZTNA)
Firewall as a Service (FWaaS)
Benefits of SASE
Cloud-based security
Secure remote access
Reduced complexity
Identity-based security
Improved visibility
Importance in Cybersecurity
SASE supports the Zero Trust security model by verifying users and devices before granting access.

6. Infrastructure as Code (IaC)
Definition
Infrastructure as Code (IaC) is the practice of managing and deploying infrastructure using machine-readable configuration files instead of manually configuring hardware.

Instead of manually creating servers, networks, and security policies, engineers define them using code.

Examples of IaC Tools
Terraform
Ansible
AWS CloudFormation
How IaC Works
Example workflow:

Engineer writes infrastructure configuration code.
The IaC tool reads the configuration.
Resources are automatically created or modified.
The infrastructure becomes repeatable and consistent.
Benefits of IaC
Automation
Faster deployment
Reduced human errors
Version control
Consistent environments
IaC and Cybersecurity
IaC improves security by allowing security policies and configurations to be reviewed, tested, and tracked like software code.

Summary
Modern networking is moving toward automation, virtualization, and security-driven architectures.

SDN separates network control from packet forwarding and enables centralized management.
SD-WAN improves WAN connectivity using intelligent software-based routing.
DCI connects multiple data centers for availability and disaster recovery.
VXLAN provides scalable network virtualization for modern data centers.
SASE combines networking and security into a cloud-delivered architecture.
IaC automates infrastructure deployment through code.
Together, these technologies form the foundation of modern enterprise networks and are important concepts for network engineers, cloud engineers, and cybersecurity professionals.



IPv6 Addressing, Subnetting, Transition Technologies and Routing Documentation
Overview
IPv6 (Internet Protocol version 6) was created to replace IPv4 because of IPv4 address exhaustion. IPv6 provides a much larger address space, improved network efficiency, simplified routing, and better support for modern technologies such as IoT, cloud computing, and large enterprise networks.

IPv6 uses a 128-bit address format, compared to IPv4’s 32-bit address format.

Example IPv6 address:

2001:0db8:85a3:0000:0000:8a2e:0370:7334
IPv6 addresses are written using hexadecimal values separated by colons.

1. IPv6 Address Structure
An IPv6 address contains:

128 bits
8 groups called hextets
Each hextet contains 16 bits
Each hextet is represented by 4 hexadecimal digits
Example:

2001:0DB8:0000:0000:0000:0000:1428:57AB
Breakdown:

2001 | 0DB8 | 0000 | 0000 | 0000 | 0000 | 1428 | 57AB
Each section represents 16 bits:

8 × 16 bits = 128 bits
2. IPv6 Address Types
Unicast
A unicast address identifies a single interface.

Example:

2001:db8::1
Traffic is delivered from one device to another device.

Multicast
A multicast address identifies multiple devices.

Example:

FF02::1
Used for communication with a group of devices.

Anycast
Anycast uses the same address on multiple devices, but traffic is delivered to the closest device based on routing.

Used for:

DNS servers
Content delivery networks
3. IPv6 Address Expansion
IPv6 addresses can be expanded by adding missing zeros.

Example:

Compressed:

2001:db8::1
Expanded:

2001:0db8:0000:0000:0000:0000:0000:0001
Rules:

Each hextet must contain 4 hexadecimal digits.
Add zeros until all 8 hextets are present.
4. IPv6 Address Compression
IPv6 compression reduces the size of addresses.

Rule 1: Remove Leading Zeros
Example:

Before:

2001:0db8:0001:0000:0000:0000:0000:0001
After:

2001:db8:1:0:0:0:0:1
Leading zeros inside each hextet can be removed.

Rule 2: Replace Consecutive Zero Groups With ::
Example:

Before:

FE80:0000:0000:0000:0202:B3FF:FE1E:8329
After:

FE80::202:B3FF:FE1E:8329
Important:

The double colon (::) can only be used once in an IPv6 address.

5. IPv6 Subnetting
IPv6 subnetting is different from IPv4 subnetting.

IPv6 does not focus on conserving addresses because IPv6 has a massive address space.

The most common IPv6 subnet is:

/64
A /64 means:

First 64 bits = network prefix
Last 64 bits = interface ID
Example:

2001:db8:1234:5678::/64
Network portion:

2001:db8:1234:5678
Interface portion:

0000:0000:0000:0000
6. IPv6 Prefix Lengths
Common IPv6 prefixes:

/48
Used by organizations.

Example:

2001:db8:1234::/48
Provides many /64 networks.

/64
Standard LAN subnet.

Example:

2001:db8:1234:1::/64
Used for:

Enterprise networks
Home networks
VLANs
/128
A single IPv6 address.

Example:

2001:db8::1/128
7. IPv6 Subnet Calculation Example
Given:

2001:db8:abcd::/48
Create /64 networks.

The organization can use the next 16 bits for subnetting.

Example:

2001:db8:abcd:0001::/64
2001:db8:abcd:0002::/64
2001:db8:abcd:0003::/64
This creates thousands of possible networks.

8. IPv6 Transition Technologies
Because the world cannot immediately move from IPv4 to IPv6, transition technologies allow both protocols to operate together.

The main transition methods are:

Dual Stack
Tunneling
NAT64/DNS64
9. Dual Stack Routing
Definition
Dual Stack allows devices to run IPv4 and IPv6 simultaneously.

A device can communicate using:

IPv4
IPv6
Example:

A computer may have:

IPv4:

192.168.1.10
IPv6:

2001:db8::10
The device chooses which protocol to use depending on the destination.

Advantages
Smooth migration to IPv6
Supports both protocols
No translation required
Disadvantages
Requires managing two networks
More configuration complexity
10. IPv6 Tunneling
Definition
IPv6 tunneling allows IPv6 traffic to travel through an IPv4 network.

IPv6 packets are encapsulated inside IPv4 packets.

Example:

IPv6 Packet
     |
Encapsulation
     |
IPv4 Network
     |
Decapsulation
     |
IPv6 Destination
Types of IPv6 Tunneling
Manual Tunnels
Configured manually between two IPv6 networks.

Example:

GRE tunnels
6to4 Tunneling
Allows IPv6 communication over IPv4 infrastructure.

Uses IPv4 addresses to create IPv6 prefixes.

ISATAP
Allows IPv6 hosts to communicate over IPv4-based networks.

11. NAT64
Definition
NAT64 allows IPv6-only devices to communicate with IPv4-only devices.

It performs translation between IPv6 and IPv4 addresses.

Example:

IPv6 Client:

2001:db8::10
communicates with:

IPv4 Server:

192.0.2.10
NAT64 translates the traffic between both protocols.

Why NAT64 is Needed
During IPv6 migration:

Some networks are IPv6-only
Some servers remain IPv4-only
NAT64 provides communication between them.

12. DNS64
Definition
DNS64 works with NAT64 to allow IPv6-only clients to access IPv4 resources.

DNS64 creates synthetic IPv6 addresses from IPv4 addresses.

Example:

IPv4 address:

192.0.2.1
DNS64 creates:

64:ff9b::192.0.2.1
The IPv6 client connects using the generated IPv6 address, and NAT64 translates the traffic.

13. IPv6 Routing
IPv6 routing works similarly to IPv4 routing but uses IPv6 addresses.

Examples of IPv6 routing protocols:

RIPng
IPv6 version of RIP.

Features:

Distance vector protocol
Uses hop count
Maximum 15 hops
OSPFv3
IPv6 version of OSPF.

Features:

Link-state routing
Builds a network topology map
Uses cost as a metric
BGP for IPv6
Used between autonomous systems.

Used by:

Internet service providers
Large organizations
14. IPv6 Security Considerations
IPv6 includes security improvements but still requires proper configuration.

Security technologies include:

IPsec support
Secure Neighbor Discovery (SEND)
Firewall policies
Access Control Lists (ACLs)
Common IPv6 security risks:

Rogue Router Advertisements
Neighbor Discovery attacks
Incorrect firewall rules
Summary
IPv6 provides a scalable solution to IPv4 exhaustion through a 128-bit addressing system.

Important concepts learned:

IPv6 address structure
IPv6 compression and expansion
IPv6 subnetting using prefixes
IPv6 address types
Dual Stack routing
IPv6 tunneling
NAT64
DNS64
IPv6 routing protocols
IPv6 security considerations
IPv6 knowledge is essential for modern network engineering, cloud computing, and cybersecurity because future networks will rely heavily on IPv6 communication.


Routing Protocols and Advanced Routing Concepts Documentation
Overview
Routing is the process of selecting the best path for data packets to travel between different networks. Routers use routing tables to make forwarding decisions.

Routing can be configured manually using static routing or automatically using dynamic routing protocols.

Understanding routing is essential for network engineering and cybersecurity because routing controls how information moves across networks.

1. Static Routing
Definition
Static routing is a routing method where network administrators manually configure routes on routers.

The administrator tells the router:

Destination network
Next-hop address
Exit interface
Example:

ip route 192.168.2.0 255.255.255.0 10.0.0.2
This tells the router:

“To reach network 192.168.2.0/24, send traffic to 10.0.0.2.”

Advantages of Static Routing
Simple to configure
No routing protocol overhead
More secure because routes are manually controlled
Good for small networks
Disadvantages of Static Routing
Difficult to manage in large networks
Requires manual updates
Does not automatically adapt to network failures
2. Dynamic Routing
Definition
Dynamic routing uses routing protocols to automatically learn and exchange network information between routers.

Routers communicate with each other and update their routing tables automatically.

Examples:

RIP
EIGRP
OSPF
BGP
Advantages of Dynamic Routing
Automatically learns new networks
Adapts to failures
Suitable for large networks
Reduces manual configuration
Disadvantages
Requires more resources
More complex configuration
Can introduce security risks if not properly protected
3. Routing Protocol Categories
Dynamic routing protocols are divided into:

Interior Gateway Protocols (IGP)
Used inside one organization or autonomous system.

Examples:

RIP
EIGRP
OSPF
Exterior Gateway Protocols (EGP)
Used between different autonomous systems.

Example:

BGP
4. RIP (Routing Information Protocol)
Definition
RIP is a distance-vector routing protocol that uses hop count as its metric.

The router chooses the route with the lowest number of hops.

Maximum hop count:

15 hops
16 hops means unreachable.

5. RIPv1
Definition
RIPv1 is the first version of RIP.

Characteristics:

Classful routing protocol
Does not send subnet mask information
Does not support VLSM
Uses broadcast updates
Example:

255.255.255.255 broadcast
Limitations of RIPv1
Cannot support modern subnetting
No authentication
Inefficient for large networks
6. RIPv2
Definition
RIPv2 improved RIPv1 by adding support for modern networking features.

Characteristics:

Classless routing protocol
Sends subnet mask information
Supports VLSM
Supports authentication
Uses multicast updates
Multicast address:

224.0.0.9
RIPv1 vs RIPv2
Feature

RIPv1

RIPv2

Routing Type

Classful

Classless

Subnet Mask

Not included

Included

VLSM Support

No

Yes

Updates

Broadcast

Multicast

Authentication

No

Yes

7. EIGRP (Enhanced Interior Gateway Routing Protocol)
Definition
EIGRP is an advanced distance-vector routing protocol developed by Cisco.

It uses the Diffusing Update Algorithm (DUAL) to calculate the best path.

EIGRP Features
Fast convergence
Supports VLSM
Uses bandwidth and delay as metrics
Supports unequal-cost load balancing
Sends partial updates instead of full routing tables
EIGRP Metric
EIGRP calculates routes using:

Bandwidth
Delay
Reliability
Load
(Default calculation uses bandwidth and delay.)

EIGRP Operation
EIGRP routers maintain:

Neighbor Table
Stores directly connected EIGRP routers.

Topology Table
Stores learned routes.

Routing Table
Stores the best routes selected for forwarding.

8. OSPF (Open Shortest Path First)
Definition
OSPF is a link-state routing protocol that builds a complete map of the network.

It uses the Shortest Path First (SPF) algorithm.

OSPF Features
Open standard protocol
Supports VLSM
Fast convergence
Uses cost as a metric
Designed for large networks
OSPF Operation
OSPF routers create:

Neighbor Relationships
Routers discover each other using hello packets.

Link-State Database (LSDB)
Contains information about the network topology.

SPF Calculation
Uses the database to calculate the shortest path.

OSPF Areas
OSPF uses areas to improve scalability.

Important area:

Area 0 (Backbone Area)
All other areas connect to Area 0.

9. BGP (Border Gateway Protocol)
Definition
BGP is the routing protocol used on the Internet.

It exchanges routing information between autonomous systems (AS).

An Autonomous System is a collection of networks controlled by one organization.

Example:

Internet Service Providers
Large enterprises
Types of BGP
1. Internal BGP (iBGP)
Used between routers inside the same Autonomous System.

Example:

Router A AS 65001
       |
Router B AS 65001
Both routers belong to the same organization.

2. External BGP (eBGP)
Used between routers in different Autonomous Systems.

Example:

AS 65001
    |
    |
AS 65002
Used by:

ISPs
Internet exchange points
BGP Characteristics
Path-vector protocol
Uses AS numbers
Highly scalable
Controls Internet routing decisions
BGP considers attributes such as:

AS Path
Next Hop
Local Preference
MED
10. Administrative Distance (AD)
Definition
Administrative Distance determines how trustworthy a routing source is.

When multiple routes to the same destination exist, the router chooses the route with the lowest administrative distance.

Common Administrative Distances
Route Source

Administrative Distance

Connected

0

Static Route

1

EIGRP

90

OSPF

110

RIP

120

External BGP

20

Internal BGP

200

Example:

If a router learns a network through:

Static route AD = 1
OSPF AD = 110
The router chooses the static route because 1 is lower.

11. FHRP (First Hop Redundancy Protocol)
Definition
FHRP provides gateway redundancy by allowing multiple routers to act as a single virtual default gateway.

If one router fails, another router takes over.

Why FHRP is Needed
Without FHRP:

PC
 |
Single Router
 |
Network
If the router fails, users lose connectivity.

With FHRP:

        Router 1
          |
PC ---> Virtual Gateway
          |
        Router 2
Another router provides backup.

Types of FHRP
HSRP (Hot Standby Router Protocol)
Developed by Cisco.

Features:

Active router forwards traffic
Standby router waits for failure
VRRP (Virtual Router Redundancy Protocol)
Open standard alternative to HSRP.

GLBP (Gateway Load Balancing Protocol)
Cisco protocol that provides:

Gateway redundancy
Load balancing
12. Subinterfaces
Definition
A subinterface is a virtual interface created on a physical router interface.

It allows one physical interface to support multiple logical networks.

Router-on-a-Stick
A common use of subinterfaces is connecting multiple VLANs using one physical router interface.

Example:

Physical interface:

GigabitEthernet0/0
Subinterfaces:

GigabitEthernet0/0.10
GigabitEthernet0/0.20
Each subinterface represents a different VLAN.

Subinterface Configuration Example
interface gigabitEthernet 0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
Summary
Routing is the foundation of network communication.

Key concepts learned:

Static routing provides manual route configuration.
Dynamic routing allows routers to automatically exchange routes.
RIP uses hop count and has RIPv1 and RIPv2 versions.
EIGRP provides fast convergence using the DUAL algorithm.
OSPF builds a complete network map using link-state information.
BGP controls communication between autonomous systems on the Internet.
Administrative Distance determines route trustworthiness.
FHRP provides gateway redundancy.
Subinterfaces allow multiple logical networks on one physical interface.
These concepts are essential for network administration, cloud networking, and cybersecurity because attackers and defenders both depend on understanding how traffic moves through networks.

NAT: Translates IP addresses between networks.

NAT Overload (PAT): Allows multiple devices to share one public IP address using port numbers.

VLAN: Logically divides a switched network into separate broadcast domains.

VLAN Trunking: Carries traffic from multiple VLANs over one physical link.

Native VLAN: The VLAN whose traffic travels untagged on an 802.1Q trunk by default.

Link Aggregation: Combines multiple physical links into one logical link.

STP (Spanning Tree Protocol): Prevents Layer 2 switching loops by blocking redundant paths.

Rapid STP (RSTP): Provides faster recovery from network topology changes than STP.

Band Steering: Encourages Wi-Fi devices to connect to a preferred frequency band.

IBSS: A Wi-Fi ad hoc network where devices communicate without a central access point.

SSID: The name of a Wi-Fi network.

BSSID: Identifies a specific Wi-Fi Basic Service Set, typically by its radio’s MAC address.

ESSID: The network name shared by access points in an Extended Service Set.

Antenna: Transmits and receives electromagnetic waves for wireless communication.

Wireless Mesh: A network where wireless nodes relay data between one another.

MDF: The main telecommunications distribution point in a building.

IDF: A secondary distribution point that connects local cabling to the main network.
