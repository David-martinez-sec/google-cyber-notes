# Learn More About Packet Captures  

**Course 6 – Module X**  
_File: c6_mX_packet_captures.md_  

---

## Why Packet Captures Matter  
Security analysts monitor and analyze **network traffic flows**.  
- Packets are the basic units of information exchange.  
- Packet captures (pcaps) allow analysts to inspect traffic for unusual activity.  
- Analyzing packets gives valuable context to network events and investigations.  

---

## Packets  
- **Definition:** Small units of data sent across a network.  
- Example: Uploading an image → broken into many packets → reassembled at destination.  
- In cybersecurity, packets help identify anomalies and attacks.  

### Components of a Packet  
1. **Header** → Routing/metadata (source/destination IPs, length, protocol, IDs).  
   - Can include Ethernet, IP, TCP headers, etc.  
2. **Payload** → The actual data (e.g., image, HTTP request).  
3. **Footer/Trailer** → Used by some protocols (e.g., Ethernet CRC for error-checking).  
   - Note: Most protocols (like IP) do not use footers.  

---

## Network Protocol Analyzers (Packet Sniffers)  
Tools that capture and analyze data traffic in a network.  
- Examples: **tcpdump, Wireshark, TShark**.  
- Uses:  
  - Investigate suspicious activity (security).  
  - Collect network stats (bandwidth, speed).  
  - Troubleshoot network performance.  
- Can also be abused by attackers to capture sensitive data (logins, passwords).  

### How They Work  
- Packets flow through the **Network Interface Card (NIC)**.  
- By default, NICs only see traffic addressed to them.  
- **Promiscuous mode / Monitor mode:** Lets NIC capture *all* visible traffic.  
- Captured in **raw binary** → converted to human-readable format by analyzers.  

⚠️ Note: Promiscuous mode can expose sensitive data. Use responsibly.  

---

## Packet Captures (P-caps)  
- **Definition:** Files containing intercepted packets.  
- Used with protocol analyzers to filter, view, and analyze traffic.  
- Common use: Filtering packets from a specific IP during an investigation.  
- Legal note: Capturing traffic without permission is often illegal.  

### File Formats & Libraries  
- **Libpcap** → Unix/Linux/Mac (used by tcpdump).  
- **WinPcap** → Older Windows format, now less used.  
- **Npcap** → Windows library from Nmap project.  
- **PCAPng** → “Next generation” format, supports both packets and metadata.  

---

## Key Takeaways  
- Packets are the foundation of network communication.  
- Analyzers like Wireshark and tcpdump provide visibility into network activity.  
- Packet captures (pcaps) let analysts investigate, filter, and study traffic.  
- Understanding packet structure and capture formats is essential for defending networks.  

---

### Pro Tip  
Try capturing and analyzing packets on your **home network** to practice using tools like tcpdump and Wireshark.  
