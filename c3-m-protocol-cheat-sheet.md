# Module 1 – Network Protocols Reference Sheet

## Overview
This sheet combines all protocols from the readings into one quick reference.  
Each protocol is listed with:  
- **Category** (Communication, Management, Security)  
- **Port(s)**  
- **TCP/IP Model Layer**  

---

## Communication Protocols
| Protocol | Purpose | Port(s) | TCP/IP Layer |
|----------|---------|---------|--------------|
| **TCP** (Transmission Control Protocol) | Reliable, connection-oriented delivery. Uses three-way handshake. | Dynamic (depends on service) | Transport |
| **UDP** (User Datagram Protocol) | Fast, connectionless delivery. Best for real-time/low-latency apps. | Dynamic (depends on service) | Transport |
| **HTTP** (Hypertext Transfer Protocol) | Web browsing (insecure). | TCP 80 | Application |
| **HTTPS** (HTTP Secure) | Secure web browsing with SSL/TLS. | TCP 443 | Application |
| **DNS** (Domain Name System) | Translates domain names → IP addresses. | UDP 53 (default), TCP 53 (large queries) | Application |

---

## Management Protocols
| Protocol | Purpose | Port(s) | TCP/IP Layer |
|----------|---------|---------|--------------|
| **SNMP** (Simple Network Management Protocol) | Monitors and manages network devices. | UDP 161 (requests), UDP 162 (traps) | Application |
| **ICMP** (Internet Control Message Protocol) | Error reporting, connectivity tests (e.g., ping). | No port (uses IP directly) | Internet |
| **DHCP** (Dynamic Host Configuration Protocol) | Assigns IP addresses and config info to devices. | UDP 67 (server), UDP 68 (client) | Application |
| **ARP** (Address Resolution Protocol) | Maps IP → MAC addresses within a LAN. | None (layer 2 protocol) | Network Access |

---

## Security Protocols
| Protocol | Purpose | Port(s) | TCP/IP Layer |
|----------|---------|---------|--------------|
| **HTTPS** | Secure web browsing with SSL/TLS. | TCP 443 | Application |
| **SFTP** (Secure File Transfer Protocol) | Secure file transfer using SSH. | TCP 22 | Application |
| **SSH** (Secure Shell) | Secure remote login & encrypted communication. | TCP 22 | Application |
| **Telnet** | Remote access (insecure, cleartext). | TCP 23 | Application |

---

## Email Protocols
| Protocol | Purpose | Port(s) | TCP/IP Layer |
|----------|---------|---------|--------------|
| **SMTP** (Simple Mail Transfer Protocol) | Sends/relays email. | TCP/UDP 25 (unencrypted), TCP/UDP 587 (TLS) | Application |
| **POP3** (Post Office Protocol v3) | Downloads email from server, may not sync across devices. | TCP/UDP 110 (unencrypted), TCP/UDP 995 (SSL/TLS) | Application |
| **IMAP** (Internet Message Access Protocol) | Retrieves/syncs email across devices, keeps on server. | TCP 143 (unencrypted), TCP 993 (TLS) | Application |

---

## Key Takeaways
- Protocols are grouped into **Communication, Management, Security, and Email** categories.  
- **Port numbers** are critical for firewall rules, monitoring, and intrusion detection.  
- Some protocols (Telnet, unencrypted HTTP/POP3/SMTP) are **insecure** and often exploited.  
- Knowing both the **function** and the **TCP/IP layer** helps analysts quickly locate where issues occur and how to secure them.  
