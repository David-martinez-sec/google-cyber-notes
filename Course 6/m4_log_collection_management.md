# Best Practices for Log Collection and Management  

**Course 6 – Module 4**  
_File: c6_m4_log_collection_management.md_  

---

## Logs  
- Logs = records of events that occur in systems, applications, and devices.  
- Originally used for troubleshooting errors, now critical for **incident investigation**.  
- Logs answer the **5 W’s**: Who, What, When, Where, Why.  
- Accessed through **logging receivers** (e.g., SIEMs) that centralize data.  

---

## Types of Logs  
- **Network logs** → From firewalls, routers, switches.  
- **System logs** → From operating systems (Windows, Linux, macOS, Chrome OS™).  
- **Application logs** → Events inside software (e.g., smartphone app).  
- **Security logs** → From security tools (AV, IDS/IPS).  
- **Authentication logs** → Successful/failed login attempts.  

---

## Log Details  
Typical entries include:  
- Date & time  
- Location  
- Action performed  
- Author (user/process)  

**Example:**  
```  
Login Event [05:45:15] User1 Authenticated successfully  
```  

Verbose logging adds more detail:  
```  
Login Event [2022/11/16 05:45:15.892673] auth_performer.cc:470 User1 Authenticated successfully from device1 (192.168.1.2)  
```  

---

## Log Management  
The process of **collecting, storing, analyzing, and disposing of log data**.  

### What to Log  
- Prioritize log sources with most useful security info.  
- Avoid unnecessary verbosity.  
- Handle **PII** carefully (e.g., phone numbers, names, email addresses).  

### The Issue with Overlogging  
- Tempting to log everything → bad practice.  
- **Disadvantages:**  
  - High storage & maintenance costs.  
  - Increased system load → performance impact.  
  - Difficult searches → slows down investigations.  

### Log Retention  
- Some industries have strict requirements:  
  - **Public sector:** FISMA.  
  - **Healthcare:** HIPAA.  
  - **Financial services:** PCI DSS, GLBA, SOX.  
- Policies should define retention periods.  

### Log Protection  
- Malicious actors may alter/delete logs to hide activity.  
- **Best practice:** store logs in **centralized log servers** instead of local machines.  
  - Adds a barrier between attackers and log data.  

---

## Key Takeaways  
- Logs are essential for **incident investigations**.  
- Effective log management improves **searchability and efficiency**.  
- Balance between enough detail vs overlogging.  
- Secure storage and compliance with retention requirements are crucial for integrity and legal adherence.  
