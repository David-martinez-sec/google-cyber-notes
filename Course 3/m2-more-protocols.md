# Module 1 – Additional Network Protocols

## Overview
This reading introduces additional protocols that security analysts frequently encounter, along with their port numbers and TCP/IP model placement. Understanding these is critical for analyzing traffic, configuring firewalls, and recognizing vulnerabilities.

---

## Network Address Translation (NAT)
- Translates **private IP addresses** ↔ **public IP addresses**.  
- Required for devices in a LAN to communicate with the internet.  
- Typically performed by a **router or firewall**.  
- Operates at the **Internet layer (L2)** and **Transport layer (L3)** of the TCP/IP model.  

### Private IP ranges (RFC1918):
- `10.0.0.0 – 10.255.255.255`  
- `172.16.0.0 – 172.31.255.255`  
- `192.168.0.0 – 192.168.255.255`  

### Public IP ranges:
- Assigned by ISP/IANA.  
- Unique across the global internet.  
- Cost associated with leasing.  

---

## Dynamic Host Configuration Protocol (DHCP)
- **Management protocol** at the **Application layer**.  
- Dynamically assigns IP addresses, DNS servers, and default gateways.  
- Ports:  
  - **UDP 67** (server)  
  - **UDP 68** (client)  

---

## Address Resolution Protocol (ARP)
- Resolves **IP addresses → MAC addresses**.  
- Operates at the **Network Access layer (L2)**.  
- Each device maintains an **ARP cache**.  
- No assigned port number.  

---

## Telnet
- Application layer protocol for **remote system connections**.  
- Sends data in **cleartext** → insecure.  
- Ports: **TCP 23**.  
- Largely replaced by **SSH**.  

---

## Secure Shell (SSH)
- Provides **secure authentication and encrypted communication**.  
- Application layer protocol.  
- Port: **TCP 22**.  
- Replaces Telnet for secure remote access.  

---

## Email Protocols

### Post Office Protocol (POP3)
- Retrieves and downloads emails from a mail server.  
- Emails may not sync across devices.  
- Ports:  
  - **TCP/UDP 110** (unencrypted)  
  - **TCP/UDP 995** (encrypted, SSL/TLS).  

### Internet Message Access Protocol (IMAP)
- Retrieves emails but keeps them on the server.  
- Allows syncing across multiple devices.  
- Ports:  
  - **TCP 143** (unencrypted)  
  - **TCP 993** (encrypted, TLS).  

### Simple Mail Transfer Protocol (SMTP)
- Sends and routes emails between servers.  
- Works with **Message Transfer Agents (MTAs)** and DNS.  
- Ports:  
  - **TCP/UDP 25** (unencrypted, common for spam).  
  - **TCP/UDP 587** (encrypted, TLS).  

---

## Protocols and Port Numbers (Quick Reference)

| Protocol | Port(s) |
|----------|---------|
| DHCP     | UDP 67 (server), UDP 68 (client) |
| ARP      | None |
| Telnet   | TCP 23 |
| SSH      | TCP 22 |
| POP3     | TCP/UDP 110 (unencrypted), TCP/UDP 995 (SSL/TLS) |
| IMAP     | TCP 143 (unencrypted), TCP 993 (TLS) |
| SMTP     | TCP/UDP 25 (unencrypted), TCP/UDP 587 (TLS) |

---

## Key Takeaways
- Security analysts must understand **protocol placement in TCP/IP** and their **port numbers**.  
- Critical protocols: **NAT, DHCP, ARP, Telnet, SSH, POP3, IMAP, SMTP**.  
- Ports are essential for configuring firewalls and detecting malicious activity.  
- Some protocols (e.g., Telnet, unencrypted POP3/SMTP) are insecure and often exploited.  
