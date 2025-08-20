# Security Incident Report

---

## Part 1: Summary of the Problem

- **Incident:** [Briefly describe what happened — e.g., users unable to access a website]  
- **Error observed:** [Exact error message]  
- **Network Analysis Findings:**  
  - [Protocol used, e.g., UDP/TCP, ICMP, etc.]  
  - [Port affected, e.g., port 53 for DNS]  
  - [High-level summary of what tcpdump or analyzer showed]  

**Most likely issue:** [e.g., DNS server down, misconfigured firewall, DDoS attack, etc.]  

---

## Part 2: Analysis

- **Time of incident:** [Timestamp or range]  
- **How the issue was identified:** [Customer reports, monitoring alerts, internal verification]  
- **Actions taken by IT/security team:**  
  1. [Step 1: e.g., Reproduced the issue]  
  2. [Step 2: e.g., Captured logs with tcpdump/Wireshark]  
  3. [Step 3: e.g., Identified affected service or port]  

- **Key findings:**  
  - **Affected port/service:** [e.g., UDP 53 (DNS)]  
  - **Impact:** [What services/users were affected]  
  - **Root technical issue:** [Summarize the failure or vulnerability]  

- **Likely cause(s):**  
  - [Option 1: e.g., DoS/DDoS attack on a service]  
  - [Option 2: e.g., Internal server outage/misconfiguration]  
  - [Option 3: e.g., Firewall or routing error]  

---

## Part 3: (Optional) Recommendations / Next Steps

- [e.g., Implement monitoring/alerts on critical ports]  
- [e.g., Add redundancy/failover for DNS servers]  
- [e.g., Review firewall rules and access logs for anomalies]  
- [e.g., Conduct post-incident review with IT team]  

