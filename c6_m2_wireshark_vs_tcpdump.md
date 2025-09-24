# Wireshark vs tcpdump  

**Course 6 – Module 2**  
_File: c6_m2_wireshark_vs_tcpdump.md_  

---

## Similarities  
1. **Purpose** → Both are packet sniffers / network protocol analyzers.  
2. **Packet Capture Format** → Both use `.pcap` files (interchangeable).  
3. **Filtering** → Both support BPF (Berkeley Packet Filter) syntax.  
4. **Cross-Platform** → Run on Linux, macOS, Windows (via Libpcap/Npcap).  
5. **Privileges** → Require root/admin rights for live captures.  
6. **Analysis** → Both display detailed packet info (IPs, ports, flags, protocols).  

---

## Differences  

| Feature             | Wireshark (GUI)                   | tcpdump (CLI)                   |
|---------------------|-----------------------------------|----------------------------------|
| **Interface**       | Graphical (user-friendly, visual) | Command-line (text-based)        |
| **Ease of Use**     | Beginner-friendly, visual filters | Steeper learning curve           |
| **Filtering**       | Advanced display filters, regex   | Basic capture filters (BPF)      |
| **Analysis**        | Deep forensic analysis, follow streams | Lightweight, raw summaries |
| **Performance**     | Heavier, not ideal for servers    | Lightweight, efficient           |
| **Best Use Case**   | Detailed forensic packet analysis | Quick captures, remote servers   |

---

## Hardware & Software Requirements  
- **No special hardware required** → Standard NICs work.  
- NIC must support **promiscuous mode** (see all packets) and **monitor mode** for Wi-Fi.  
- **Libraries**:  
  - tcpdump uses **Libpcap** (Linux/macOS).  
  - Wireshark/tcpdump on Windows use **Npcap/WinPcap**.  

---

## Open Source Licensing  
- **tcpdump** → Open source (BSD-style license), maintained at tcpdump.org.  
- **Wireshark** → Open source (GNU GPL v2), global community-supported.  
- ✅ Both are **free to use** and widely adopted in cybersecurity.  

---

## Key Takeaways  
- Wireshark = **Microscope** 🧪 (deep, visual forensic analysis).  
- tcpdump = **Scalpel** 🔪 (fast, lightweight, CLI-based captures).  
- They complement each other: capture with tcpdump, analyze deeply with Wireshark.  
