# Overview of SIEM Technology  

**Course 6 – Module X**  
_File: c6_mX_siem_overview.md_  

---

## What is SIEM?  
A **Security Information and Event Management (SIEM)** tool is an application that collects and analyzes log data to monitor critical activities in an organization.  
- Helps analysts perform **log analysis** to identify events of interest.  
- Provides visibility into activity between systems and devices on a network.  

---

## Advantages of SIEM  
- **Access to event data** → Collects logs from many sources (firewalls, servers, routers) in real-time.  
- **Monitoring, detecting, and alerting** → Continuously monitors data, applies detection rules, and triggers alerts.  
- **Log storage** → Retains historical data for investigations, audits, or compliance needs.  

---

## The SIEM Process  

### 1. Collect and Aggregate Data  
- Collects logs from multiple sources (firewalls, servers, routers, etc.).  
- Aggregates logs into one centralized location.  
- **Parsing** → Maps log fields into structured values for easier interpretation.  
  - Example:  
    - Raw log:  
      ```
      April 3 11:01:21 server sshd[1088]: Failed password for user nuhara from 218.124.14.105 port 5023
      ```  
    - Parsed log:  
      ```
      host = server  
      process = sshd  
      source_user = nuhara  
      source_ip = 218.124.14.105  
      source_port = 5023  
      ```  

### 2. Normalize Data  
- Data from different sources must be standardized.  
- Normalization converts raw data into a consistent, structured format that is easily searchable.  

### 3. Analyze Data  
- SIEM applies detection logic (rules and conditions) to the data.  
- If activity matches rules, alerts are generated.  
- **Correlation**: Compares multiple log events to find patterns that may indicate threats.  

---

## Common SIEM Tools  
- **AlienVault® OSSIM™**  
- **Chronicle**  
- **Elastic**  
- **Exabeam**  
- **IBM QRadar®**  
- **LogRhythm**  
- **Splunk**  

---

## Key Takeaways  
- SIEM tools centralize log data for visibility and faster investigations.  
- Process includes **collecting, normalizing, and analyzing** event data.  
- SIEM tools support threat detection, incident response, and compliance.  
- Analysts use SIEMs to detect anomalies, investigate events, and protect critical assets.  
