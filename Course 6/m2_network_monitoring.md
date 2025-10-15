# Maintain Awareness with Network Monitoring  

**Course 6 – Module 2**  
_File: c6_m2_network_monitoring.md_  

---

## Why Network Monitoring Matters  
- Network communication = **network traffic + network data**  
- Network monitoring helps organizations detect suspicious activity.  
- Key to maintaining **situational awareness** and preventing intrusions.  

---

## Know Your Network  
- Networks generate information: source/destination IP, ports, amount of data, time, etc.  
- Establishing a **baseline** of normal activity is essential.  
  - Example: Normal work traffic = 9 a.m. to 5 p.m.  
  - Deviations (e.g., large data transfers at 2 a.m.) → may indicate threats.  

---

## What to Monitor  
### Flow Analysis  
- **Flow** = movement of network communications (packets, protocols, ports).  
- Ports are often tied to protocols (e.g., HTTPS → Port 443).  
- Malicious actors may misuse uncommon ports (e.g., HTTPS on port 8088).  
- Watch for **command and control (C2)** traffic.  

### Packet Payload Information  
- Packets = source/destination IP + payload (actual data).  
- Payloads may be encrypted; decryption may be required.  
- Monitor for **data exfiltration** (sensitive data leaving network).  

### Temporal Patterns  
- Packets also contain timing data.  
- Example: Bulk traffic expected during business hours; unusual traffic outside baseline should be flagged.  

---

## Protecting Your Network  
- **SOC (Security Operations Center):** Focuses on network/system security, incident detection, and response.  
- **NOC (Network Operations Center):** Focuses on performance, availability, and uptime.  

Security analysts use **indicators of compromise (IoC)** to detect threats by watching for unusual traffic patterns.  

---

## Tools for Network Monitoring  
- **Intrusion Detection Systems (IDS):** Detect and alert on deviations (often monitoring packet payloads).  
- **Network Protocol Analyzers (Packet Sniffers):** Capture and analyze traffic manually.  
  - Examples: **tcpdump, Wireshark**  
  - Allow recording of packet captures (pcaps) for detailed investigation.  

---

## Key Takeaways  
- You can’t protect what you don’t know → network monitoring is foundational.  
- Baselines establish "normal" activity → deviations may signal threats.  
- IDS and packet sniffers are critical tools for identifying suspicious activity.  
- SOCs focus on **security monitoring**; NOCs focus on **network performance**.  
