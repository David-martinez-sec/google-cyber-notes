# Module 1 – Components of Network Layer Communication

## Overview
This reading explores operations at **Layer 3 (Network Layer)** of the OSI model, focusing on:  
- How addressing and delivery of packets works.  
- The structure of **IPv4 packets**.  
- Key differences between **IPv4 and IPv6**.  

---

## Operations at the Network Layer
- The **network layer** manages addressing and delivery of packets from host to destination.  
- Packets are forwarded router-to-router until reaching the destination IP address.  
- The **destination IP address** is stored in the packet header and used for routing.  
- Routing tables store information for future routing decisions.  

### Data Packets
- A data packet = IP packet (TCP) or datagram (UDP).  
- **Header** includes:  
  - Destination IP address.  
  - Source IP address.  
  - Packet size.  
  - Protocol used (TCP/UDP).  

---

## IPv4 Packet Format
An **IPv4 packet** has two parts:  
1. **Header** (20–60 bytes): contains routing information.  
2. **Data** (variable, up to 65,535 bytes): contains the actual message.  

### IPv4 Packet Header (13 Fields)
1. **Version (VER)**: Identifies protocol version (e.g., IPv4).  
2. **Header Length (HLEN/IHL)**: Where header ends and data begins.  
3. **Type of Service (ToS)**: Prioritization of packets (QoS).  
4. **Total Length**: Length of entire packet (max 65,535 bytes).  
5. **Identification**: Unique ID for fragmented packets.  
6. **Flags**: Indicates fragmentation details.  
7. **Fragmentation Offset**: Position of fragment in original packet.  
8. **Time to Live (TTL)**: Prevents endless forwarding; decrements per hop.  
9. **Protocol**: Identifies protocol for data portion (TCP, UDP, etc.).  
10. **Header Checksum**: Detects header corruption.  
11. **Source IP Address**: Address of sender.  
12. **Destination IP Address**: Address of receiver.  
13. **Options**: Extra features like security options.  

---

## IPv4 vs. IPv6

### IPv4
- Address format: **four decimal numbers** (0–255) separated by periods.  
- Size: **4 bytes**, ~4.3 billion possible addresses.  
- Example: `198.51.100.0`.  
- Limitations: Address exhaustion, private address collisions.  

### IPv6
- Address format: **eight groups** of four hex digits separated by colons.  
- Size: **16 bytes**, ~340 undecillion possible addresses.  
- Example: `2002:0db8:0000:0000:0000:ff21:0023:1234` (can be shortened to `2002:0db8::ff21:0023:1234`).  
- Simpler header: Removes fields like IHL, Identification, and Flags. Adds **Flow Label** (for special handling).  
- Advantages: Efficient routing, eliminates address collisions, supports vastly more devices.  

---

## Security Implications
- **Packet analysis** can reveal:  
  - Source and destination of traffic.  
  - Protocol in use (TCP, UDP, etc.).  
  - Potential anomalies or malicious activity.  
- IPv6 improves routing efficiency and reduces risks from address conflicts.  

---

## Key Takeaways
- The **network layer** ensures delivery of packets using IP addressing and routing.  
- IPv4 packets consist of a **header** and **data**, with up to 13 fields in the header.  
- IPv6 addresses exhaustion issues, simplifies headers, and supports exponentially more devices.  
- Analyzing packet fields provides critical **security insights** into network activity.  
