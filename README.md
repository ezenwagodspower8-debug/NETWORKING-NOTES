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

## 💻 Command Prompt for Network Troubleshooting & Auditing
Hands-on validation, diagnostic execution, and security auditing using native command-line interface tools:
* `ipconfig` - Audits local network interface cards, subnets, and active default gateways.
* `ping 127.0.0.1` - Tests local loopback to verify your computer's internal TCP/IP stack configuration.
* `ping [Default Gateway]` - Tests physical connectivity to the local network edge (your router).
* `ping 8.8.8.8` - Tests external packet transmission viability via Google's public DNS servers.
* `tracert 8.8.8.8` - Traces every hop router path to isolate where traffic drops occur across the WAN.
* `nslookup` - Interrogates DNS servers to audit name-to-IP resolution mechanics.
* `netstat` - Audits all active network connections, routing tables, and listening daemon ports on the system.
