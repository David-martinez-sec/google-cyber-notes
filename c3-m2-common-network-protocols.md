# Module 1 – Common Network Protocols

## Overview
- **Network protocol** = set of rules that define how data is structured, transmitted, and received.  
- Acts as a **common language** between devices worldwide.  
- Security analysts must understand both function and vulnerabilities.  
- Example: **DNS hijacking** can redirect users to malicious sites.  

---

## Categories of Protocols
1. **Communication Protocols**  
2. **Management Protocols**  
3. **Security Protocols**  

---

## Communication Protocols
- Govern **data exchange and timing** between devices.  
- Provide methods to recover lost data.  

### TCP (Transmission Control Protocol)  
- Connection-oriented, reliable.  
- Uses **three-way handshake** (SYN → SYN/ACK → ACK).  
- Operates at **Transport layer** (TCP/IP).  

### UDP (User Datagram Protocol)  
- Connectionless, faster but less reliable.  
- Often used for **DNS requests** and real-time apps.  
- Operates at **Transport layer** (TCP/IP).  

### HTTP (Hypertext Transfer Protocol)  
- Enables communication between clients and web servers.  
- Uses **port 80**.  
- Insecure → replaced by **HTTPS**.  
- Operates at **Application layer**.  

### DNS (Domain Name System)  
- Translates domain names → IP addresses.  
- Normally uses **UDP port 53**, switches to TCP for large responses.  
- Operates at **Application layer**.  

---

## Management Protocols
Used for **monitoring and managing** network activity.  

### SNMP (Simple Network Management Protocol)  
- Monitors and manages network devices.  
- Can reset device passwords, change configs, or check bandwidth usage.  
- Operates at **Application layer**.  

### ICMP (Internet Control Message Protocol)  
- Used for error reporting and connectivity checks.  
- Common tool: **ping** (checks connectivity/latency).  
- Operates at **Internet layer**.  

---

## Security Protocols
Ensure **data is transmitted securely** using encryption.  

### HTTPS (Hypertext Transfer Protocol Secure)  
- Secure version of HTTP, uses **SSL/TLS encryption**.  
- Protects content, not source/destination IPs.  
- Uses **port 443**.  
- Operates at **Application layer**.  

### SFTP (Secure File Transfer Protocol)  
- Transfers files securely using **SSH** (TCP port 22).  
- Encrypts with **AES and other algorithms**.  
- Common for cloud storage uploads/downloads.  
- Operates at **Application layer**.  

---

## Key Takeaways
- Protocols define **how communication occurs** between devices.  
- Analysts must know protocols + their vulnerabilities to detect misuse.  
- Key protocols to know:  
  - **TCP, UDP, HTTP, DNS, SNMP, ICMP, HTTPS, SFTP**.  
- Security protocols encrypt data but still expose metadata (source/destination).  
