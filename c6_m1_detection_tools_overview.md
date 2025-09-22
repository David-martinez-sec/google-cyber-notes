# Overview of Detection Tools  

**Course 6 – Module X**  
_File: c6_mX_detection_tools_overview.md_  

---

## Why You Need Detection Tools  
Detection tools work like home security systems: they **monitor** and **alert** on intrusions.  
- They continuously monitor networks and systems for suspicious activity.  
- Once unusual activity is detected, they trigger alerts for investigation.  
- Some tools can also **prevent** or **stop** intrusions automatically.  

---

## Comparison of Detection Tools  

| Capability                | IDS | IPS | EDR |
|----------------------------|:---:|:---:|:---:|
| Detects malicious activity | ✓  | ✓  | ✓  |
| Prevents intrusions        | N/A| ✓  | ✓  |
| Logs activity              | ✓  | ✓  | ✓  |
| Generates alerts           | ✓  | ✓  | ✓  |
| Behavioral analysis        | N/A| N/A| ✓  |  

---

## Intrusion Detection System (IDS)  
- Monitors system/network activity and alerts on possible intrusions  
- Provides continuous monitoring but does **not stop** malicious activity  
- Example: Detects suspicious logins but won’t block them  
- Tools: **Zeek, Suricata, Snort®, Sagan**  

### Detection Categories  
- **True Positive** → Correctly detects an attack  
- **True Negative** → No malicious activity; no alert  
- **False Positive** → Alert triggered but no real threat  
- **False Negative** → Missed detection of an actual threat (most dangerous)  

---

## Intrusion Prevention System (IPS)  
- Similar to IDS, but also **takes action** to block/stop intrusions  
- Example: Sends alert + modifies router ACL to block traffic  
- Many IDS tools also have IPS modes (e.g., **Suricata, Snort, Sagan**)  

---

## Endpoint Detection and Response (EDR)  
- Installed on **endpoints** (computers, phones, tablets, servers)  
- Monitors, records, and analyzes endpoint activity  
- Performs **behavioral analysis** with ML/AI to detect patterns  
- Can **automate responses** (e.g., block malicious process)  
- Tools: **Open EDR®, Bitdefender™ EDR, FortiEDR™**  

---

## Key Takeaways  
- Detection tools (IDS, IPS, EDR) are critical for monitoring and protecting systems.  
- **IDS** → Detects and alerts only.  
- **IPS** → Detects, alerts, and **prevents intrusions**.  
- **EDR** → Endpoint-focused, adds **behavioral analysis** and **automated response**.  
- These tools give security professionals awareness and the ability to stop attacks quickly.  
