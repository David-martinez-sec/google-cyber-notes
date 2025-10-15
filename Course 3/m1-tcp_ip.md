# Module 1 – TCP/IP Model

## Overview
This reading builds on the **TCP/IP model**, compares it with the **OSI model**, and explores the common protocols that operate at each layer.  
Both models are conceptual frameworks used by network and security professionals to visualize how data moves across networks and where security threats may occur.

---

## TCP/IP Model
- A framework for visualizing **how data is organized and transmitted**.  
- Helps engineers and analysts troubleshoot and identify which layers are impacted by incidents.  
- Has **four layers**:  
  1. Network Access Layer  
  2. Internet Layer  
  3. Transport Layer  
  4. Application Layer  

---

## Network Access Layer
- Also called the **data link layer**.  
- Deals with **creation of packets** and **transmission across the physical network**.  
- Hardware components: hubs, modems, cables, wiring.  
- **Protocol**: Address Resolution Protocol (**ARP**)  
  - Maps IP addresses ↔ MAC addresses.  
  - Enables local network communication.

---

## Internet Layer
- Also called the **network layer**.  
- Ensures **delivery of packets** to the destination host, even across different networks.  
- Attaches **IP addresses** to data packets (source and destination).  
- Determines delivery protocol.  

### Common Protocols
- **Internet Protocol (IP)**: Sends packets to the correct destination. Works with TCP/UDP for service delivery.  
- **Internet Control Message Protocol (ICMP)**: Provides error reporting and status updates.  
  - Detects and troubleshoots errors (e.g., dropped packets, redirect notices).  

---

## Transport Layer
- Responsible for **end-to-end delivery** between two systems.  
- Includes **flow control** and **error handling**.  

### Protocols
- **Transmission Control Protocol (TCP)**  
  - Connection-oriented.  
  - Establishes connection between devices.  
  - Reliable delivery → retransmits lost/corrupted data.  
  - Includes port number in the TCP header.  

- **User Datagram Protocol (UDP)**  
  - Connectionless.  
  - No connection setup → faster but less reliable.  
  - No retransmission tracking.  
  - Common for **real-time applications** (video/audio streaming, gaming).  

---

## Application Layer
- Equivalent to the **application, presentation, and session layers** in OSI.  
- Defines **network requests and responses**.  
- Determines how packets interact with receiving devices.  

### Common Protocols
- **HTTP** – Web browsing.  
- **SMTP** – Email transfer.  
- **SSH** – Secure remote login.  
- **FTP** – File transfers.  
- **DNS** – Resolves domain names to IP addresses.  

Application protocols rely on **transport and lower layers** for data delivery.

---

## TCP/IP vs. OSI Model
- **OSI Model**: 7 layers (Physical, Data Link, Network, Transport, Session, Presentation, Application).  
- **TCP/IP Model**: 4 layers (Network Access, Internet, Transport, Application).  
- Both models:  
  - Define standards for networking.  
  - Help professionals identify sources of issues.  
- **TCP/IP model is a simplified version** of the OSI model.  

---

## Key Takeaways
- **TCP/IP** and **OSI** are conceptual models for understanding network communication.  
- TCP/IP has **4 layers**, OSI has **7 layers**.  
- Each TCP/IP layer has key protocols:  
  - **Network Access**: ARP  
  - **Internet**: IP, ICMP  
  - **Transport**: TCP, UDP  
  - **Application**: HTTP, SMTP, SSH, FTP, DNS
