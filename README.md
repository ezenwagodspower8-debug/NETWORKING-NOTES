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

## 💻 The 10 Core Network Command Prompt Utilities
The definitive suite of native command-line interface tools used for network diagnostics, security auditing, and verification. (Use the `/?` help switch after any command to view its hidden variety configurations and flags).

1. `ipconfig` — Audits local network interface cards, subnets, and active default gateways.
2. `ping` — Tests device connectivity (tested via loopback 127.0.0.1, the default gateway, and external 8.8.8.8).
3. `tracert` — Traces every hop router path to isolate where traffic drops occur across the WAN.
4. `nslookup` — Interrogates DNS servers to audit name-to-IP resolution mechanics.
5. `netstat` — Audits all active network connections, routing tables, and listening daemon ports on the system.
6. `arp` — Reveals the local network table mapping IP addresses to physical MAC hardware addresses.
7. `route` — Displays and manipulates your computer's internal network traffic routing tables.
8. `hostname` — Instantly prints out the unique network identification name of your computer.
9. `pathping` — A hybrid tool that combines ping and tracert to pinpoint exact packet loss locations.
10. `nbtstat` — Troubleshoots NetBIOS over TCP/IP name resolutions on legacy infrastructure networks
11. `nbtstat` — Troubleshoots NetBIOS over TCP/IP name resolutions on legacy infrastructure networks.

