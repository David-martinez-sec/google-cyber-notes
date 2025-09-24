# Overview of tcpdump  

**Course 6 – Module 2**  
_File: c6_m2_overview_of_tcpdump.md_  

---

## What is tcpdump?  
- **tcpdump** = Command-line network protocol analyzer.  
- Captures network traffic and saves to **pcap** files.  
- Useful for troubleshooting and detecting malicious activity.  
- Pre-installed on many Linux distributions; available for Unix/macOS.  
- ⚠️ Capturing requires **root/sudo privileges**.  

---

## Capturing Packets with tcpdump  
**Syntax:**  
```bash
sudo tcpdump [-i interface] [option(s)] [expression(s)]
```  

- `-i` → Interface (e.g., `-i any` for all interfaces).  
- Options → Flags that alter command execution.  
- Expressions → Filters to isolate specific traffic.  
- Use `-D` → Lists available interfaces.  

---

## Options (Flags)  

- **-w** → Write packets to file  
  ```bash
  sudo tcpdump -i any -w capture.pcap
  ```  

- **-r** → Read packets from file  
  ```bash
  sudo tcpdump -r capture.pcap
  ```  

- **-v / -vv / -vvv** → Verbosity levels (more detail in output).  
  ```bash
  sudo tcpdump -r capture.pcap -v
  ```  

- **-c** → Capture count limit  
  ```bash
  sudo tcpdump -i any -c 3
  ```  

- **-n / -nn** → Disable hostname/port resolution (best practice).  
  ```bash
  sudo tcpdump -r capture.pcap -v -n
  ```  

⚡ Pro tip: Options can be combined (`-vn`). If an option takes a parameter (e.g., `-c 3`), it can’t be combined.  

---

## Expressions  
Filter packets by **protocols, IPs, ports**.  

- IPv6 only:  
  ```bash
  sudo tcpdump ip6
  ```  

- IP + Port 80:  
  ```bash
  sudo tcpdump -r capture.pcap -n 'ip and port 80'
  ```  

- Grouping with parentheses:  
  ```bash
  sudo tcpdump 'ip and (port 80 or port 443)'
  ```  

Supports Boolean logic (`and`, `or`, `not`).  

---

## Interpreting Output  
Example:  
```bash
sudo tcpdump -i any -v -c 1
```  

Output includes:  
- **Timestamp** → When packet captured.  
- **Source IP & Port** → Packet origin.  
- **Destination IP & Port** → Packet destination.  
- **TCP flags, sequence numbers, options** (with `-v`).  

---

## Key Takeaways  
- tcpdump is a powerful CLI packet sniffer.  
- Requires elevated privileges (`root` or `sudo`).  
- Options control capture, verbosity, output.  
- Expressions isolate traffic for investigation.  
- Analysts must know how to capture, filter, and interpret packets effectively.  
