# Cybersecurity Incident Detection Methods  

**Course 6 – Module 3**  
_File: c6_m3_incident_detection_methods.md_  

---

## Detection and Analysis Phase  
- Detection = **prompt discovery** of security events.  
- Analysis = **investigation and validation** of alerts.  
- Tools like **IDS** and **SIEM** help detect and analyze suspicious activity.  
- Challenges: Detection tools only work as well as their **configuration**. Poor tuning = missed threats.  

---

## Threat Hunting  
- **Definition:** Proactive search for threats missed by automated tools.  
- Combines technology + human expertise.  
- Detects **fileless malware** and advanced evasion techniques.  
- **Threat hunters**:  
  - Research emerging attacks.  
  - Use **threat intelligence, IoCs, IoAs, and machine learning**.  
  - Find hidden intrusions and reduce damage.  

---

## Threat Intelligence  
- **Definition:** Evidence-based information about threats, attackers, and vulnerabilities.  
- **Sources:**  
  - Industry reports → attacker tactics, techniques, and procedures (TTPs).  
  - Government advisories → similar to reports, with guidance.  
  - Threat data feeds → IPs, domains, file hashes (often used against APTs).  
- **Platforms:** Threat Intelligence Platforms (TIPs) aggregate and analyze threat intel.  
- ⚠️ Threat feeds = context only → should not drive detection blindly.  

---

## Cyber Deception  
- **Definition:** Using deception to detect attackers and improve defenses.  
- **Honeypots:** Decoy systems/resources designed to lure intruders.  
  - Example: Fake file “Client Credit Card Information – 2022.”  
  - When accessed → security team alerted.  

---

## Key Takeaways  
- Detection requires **multiple methods**, not just tools.  
- **Threat hunting** = human-driven, proactive detection.  
- **Threat intelligence** = context from external sources.  
- **Cyber deception** = tricking attackers with honeypots/decoys.  
- A layered detection strategy strengthens organizational defense.  
