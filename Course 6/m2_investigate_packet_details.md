# Investigate Packet Details  

**Course 6 – Module 2**  
_File: c6_m2_investigate_packet_details.md_  

---

## IP Packets Overview  
Packets are the foundation of data exchange over networks. The **Internet Protocol (IP)** provides routing and addressing to ensure packets reach their destination.  

Two main versions:  
- **IPv4** → Most common, uses 32-bit addresses.  
- **IPv6** → Growing adoption, uses 128-bit addresses.  

---

## IPv4 Header (13 Fields)  
1. **Version** → IP version (IPv4).  
2. **Internet Header Length (IHL)** → Header size.  
3. **Type of Service (ToS)** → Packet priority.  
4. **Total Length** → Entire packet size (header + data).  
5. **Identification** → Identifies fragments of the same packet.  
6. **Flags** → Fragmentation information.  
7. **Fragment Offset** → Order of fragments.  
8. **Time to Live (TTL)** → Limits packet lifespan.  
9. **Protocol** → Next layer protocol (e.g., TCP, UDP).  
10. **Header Checksum** → Error-checking the header.  
11. **Source Address** → Sender’s IP.  
12. **Destination Address** → Receiver’s IP.  
13. **Options** → Extra features like security.  

---

## IPv6 Header (8 Fields)  
1. **Version** → IP version (IPv6).  
2. **Traffic Class** → Priority/class of service.  
3. **Flow Label** → Identifies packet flows.  
4. **Payload Length** → Size of payload.  
5. **Next Header** → Next protocol (e.g., TCP).  
6. **Hop Limit** → Equivalent of TTL.  
7. **Source Address** → Sender’s IP.  
8. **Destination Address** → Receiver’s IP.  

---

## Wireshark Overview  
- **Wireshark** = Open-source packet analyzer with a GUI.  
- Visualizes packets in a human-readable format.  
- Useful for investigating **headers, payloads, and anomalies**.  

### Display Filters  
- Help isolate specific packets from large captures.  
- Filters can be based on **protocols, IPs, MAC addresses, ports, etc.**  

#### Comparison Operators  
- Equal: `==` or `eq`  
- Not equal: `!=` or `ne`  
- Greater than: `>` or `gt`  
- Less than: `<` or `lt`  
- Greater or equal: `>=` or `ge`  
- Less or equal: `<=` or `le`  

Pro tip: Combine with `and`, `or`, parentheses for complex filters.  

#### Contains Operator  
- Example: `http contains "moved"` → Finds HTTP streams with the string “moved.”  

#### Matches Operator  
- Uses regex patterns to filter.  

#### Filter Toolbar  
- Example: `dns` → Shows only DNS packets.  
- Protocol filters: `dns`, `http`, `ftp`, `ssh`, `arp`, `telnet`, `icmp`.  

---

## Filtering Examples  
- **IP Address** → `ip.addr == 172.21.224.2`  
- **Source IP** → `ip.src == 10.10.10.10`  
- **Destination IP** → `ip.dst == 4.4.4.4`  
- **MAC Address** → `eth.addr == 00:70:f4:23:18:c4`  
- **UDP Port** → `udp.port == 53`  
- **TCP Port** → `tcp.port == 25`  

---

## Follow Streams  
- A **stream** = sequence of packets in a conversation.  
- Wireshark can reassemble and display streams (e.g., HTTP conversations).  
- Useful to inspect full request/response messages.  

---

## Key Takeaways  
- IPv4 headers = 13 fields, IPv6 headers = 8 fields.  
- Wireshark filters let you narrow down huge captures.  
- Display filters support operators, regex, and Boolean logic.  
- Following streams helps analysts reconstruct conversations for investigation.  
