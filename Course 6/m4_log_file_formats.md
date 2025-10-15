# Overview of Log File Formats  

**Course 6 – Module 4**  
_File: c6_m4_log_file_formats.md_  

---

## Purpose  
- Logs record events in systems and networks.  
- Security analysts use **log analysis** to identify events of interest.  
- Different formats exist → knowing how to interpret them is critical for investigations.  

---

## JSON (JavaScript Object Notation)  
- Lightweight, human-readable format often used in web/cloud.  
- Syntax derived from JavaScript.  

**Components:**  
- **Key-value pairs** → `"Alert": "Malware"`  
- **Commas** separate entries  
- **Double quotes** enclose text values  
- **Curly brackets `{}`** enclose objects  
- **Square brackets `[]`** enclose arrays  

**Example:**  
```json
"User": { 
    "id": "1234", 
    "name": "user",
    "role": "engineer"
}
```  

---

## Syslog  
- Standard for logging and transmitting data.  
- Three uses: **protocol, service, log format**.  
- Uses **port 514** (plaintext) and **6514** (encrypted).  
- Native format in Unix® systems.  

**Components:**  
- **Header** (timestamp, hostname, app, msg ID)  
- **Structured-data** (key-value pairs in brackets)  
- **Message** (details of the event)  
- **PRI** (priority level, lower = more urgent)  

**Example:**  
```
<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!
```  

---

## XML (eXtensible Markup Language)  
- Native to Windows systems.  
- Stores/transmits data with **tags**, **elements**, and **attributes**.  

**Example:**  
```xml
<Event>	
    <EventID>4688</EventID>
    <Version>5</Version>
</Event>
```  

**Attributes Example:**  
```xml
<EventData>
    <Data Name='SubjectUserSid'>S-2-3-11-160321</Data>
    <Data Name='SubjectUserName'>JSMITH</Data>
</EventData>
```  

---

## CSV (Comma Separated Values)  
- Uses commas to separate values.  
- Field position = meaning (headers may not be present).  

**Example:**  
```
2009-11-24T21:27:09.534255,ALERT,192.168.2.7,1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
```  

---

## CEF (Common Event Format)  
- Structured log format using **key-value pairs**.  
- Syntax:  
```
CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension
```  
- Often transported via Syslog.  

**Example:**  
```
Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
```  

**Breakdown:**  
- Timestamp: `Sep 29 08:26:10`  
- Hostname: `host`  
- Version: `CEF:1`  
- Device: `Security threatmanager v1.0`  
- Signature ID: `100`  
- Name: `worm successfully stopped`  
- Severity: `10`  
- Extension: `src=10.0.0.2 dst=2.1.2.2 spt=1232`  

---

## Key Takeaways  
- Logs come in many formats (JSON, Syslog, XML, CSV, CEF).  
- Analysts must know how to read and interpret each to extract meaningful details.  
- Familiarity with formats supports faster and more accurate investigations.  
