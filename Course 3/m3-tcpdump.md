# Reading tcpdump Logs

A **network protocol analyzer** (also called a packet sniffer) captures and analyzes network traffic. Analysts use these tools to **monitor networks** and **identify suspicious activity**.  

Common tools include:  
- SolarWinds NetFlow Traffic Analyzer  
- ManageEngine OpManager  
- Azure Network Watcher  
- Wireshark  
- **tcpdump** (focus of this reading)

---

## tcpdump Overview

- **Command-line analyzer** for Unix/Linux/macOS  
- Lightweight (low CPU/memory usage)  
- Uses **libpcap** library  
- Provides **brief packet analysis** directly in the terminal  
- Displays:  
  - Source IP and port  
  - Destination IP and port  
  - Timestamp  

By default, tcpdump:  
- Resolves host addresses to hostnames  
- Replaces port numbers with common service names  

---

## Interpreting tcpdump Output

Each packet captured contains key information:  
- **Timestamp** – Hours:Minutes:Seconds.Fractions  
- **Source IP & Port** – Where the packet originated  
- **Destination IP & Port** – Where the packet is headed  

Example output might look like:  

