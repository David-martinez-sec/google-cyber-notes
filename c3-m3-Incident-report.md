# Security Incident Report: DNS Service Interruption

---

## Part 1: Summary of the Problem

- **Incident:** Users reported being unable to access **www.yummyrecipesforme.com**.  
- **Error:** “Destination port unreachable.”  
- **Network Analysis Findings:**  
  - The browser attempted to resolve the domain via **UDP traffic to port 53** (DNS).  
  - **ICMP error responses** were returned, stating: **“udp port 53 unreachable.”**  
  - This indicates that the DNS server was not responding to resolution requests.  

**Most likely issue:** The DNS server was **down or unresponsive** on port 53, preventing domain name resolution.  

---

## Part 2: Analysis

- **Time of incident:** 1:24 PM (based on tcpdump timestamps).  
- **How the issue was identified:** Multiple customers reported website inaccessibility and received the “destination port unreachable” error.  
- **IT team actions:**  
  1. Verified the issue by attempting to access the site internally (reproduced the error).  
  2. Captured traffic with **tcpdump** to investigate the network flow.  
  3. Determined that all DNS queries to port 53 failed with ICMP errors.  

- **Key findings:**  
  - **Affected port:** UDP port 53 (DNS).  
  - **Service:** DNS resolution required for translating domain names to IP addresses.  
  - **Result:** Without DNS resolution, the browser could not retrieve the IP address of the web server, preventing access.  

- **Likely cause:**  
  The disruption points to an issue with the DNS server or service. Possible causes include:  
  - A **DoS/DDoS attack** targeting port 53 to overwhelm the server with requests.  
  - A **service outage or crash** on the DNS server, preventing it from listening on port 53.  
  - A **configuration error or mismanagement** of the DNS service.  

Further investigation would be required to confirm whether this was an external attack or an internal system failure.  
