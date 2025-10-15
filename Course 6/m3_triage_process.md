# The Triage Process  

**Course 6 – Module 3**  
_File: c6_m3_triage_process.md_  

---

## What is Triage?  
- **Triage** = Prioritizing incidents by urgency and importance.  
- Helps allocate resources effectively so critical issues are addressed first.  
- Ensures security teams respond quickly to limit damage.  

---

## The Triage Process (3 Steps)  

### 1. Receive and Assess  
- Alerts usually come from systems like **IDS**.  
- Analyst reviews the alert to verify validity.  
- Key questions:  
  - Is this a false positive?  
  - Has this alert occurred before? How was it resolved?  
  - Is the alert linked to a known vulnerability?  
  - What is the severity?  

### 2. Assign Priority  
Factors to determine priority:  
- **Functional Impact** → Effect on system services (e.g., ransomware disrupting availability).  
- **Information Impact** → Effect on confidentiality, integrity, availability of data (e.g., data exfiltration).  
- **Recoverability** → Can the org recover? Is the cost/time worth it?  

⚠️ Note: Alerts often include a severity rating (low/medium/high).  

### 3. Collect and Analyze  
- Perform deeper analysis of incident.  
- Gather evidence from logs, research, and tools.  
- Document investigative process.  
- Escalate to Tier 2 analyst or manager if needed.  

---

## Benefits of Triage  
- **Resource Management** → Focus on high-priority threats, avoid wasting time on false positives or low impact issues.  
- **Standardized Approach** → Ensures alerts are consistently assessed and validated (playbooks, documentation).  
- **Faster Response** → Critical incidents addressed sooner, reducing overall impact.  

---

## Key Takeaways  
- Triage = structured prioritization of alerts/incidents.  
- Helps reduce impact by ensuring timely and efficient responses.  
- Security analysts must triage daily to meet incident response goals.  
