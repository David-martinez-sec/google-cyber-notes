# Explore Signatures with Suricata  

**Course 6 – Module 4**  
_File: c6_m4_suricata_signatures_activity.md_  

---

## Activity Overview  
In this exercise, I explored how **Suricata** generates alerts and logs, and I practiced creating and testing custom rules.  
I worked with:  
- A **sample.pcap** file containing captured traffic.  
- A **custom.rules** file where I added rules.  
- The **fast.log** and **eve.json** output logs.  

---

## Scenario  
As a security analyst, I was tasked with monitoring traffic on my organization’s network. To do this, I needed to:  
1. Explore and understand existing rules in Suricata.  
2. Run Suricata against a packet capture with custom rules to trigger alerts.  
3. Analyze Suricata’s outputs in both `fast.log` and `eve.json`.  

---

## Task 1. Examine a Custom Rule  
I started by reviewing the contents of the `custom.rules` file:  

```bash
cat custom.rules
```  

The file contained this rule:  

```  
alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)  
```  

### Rule Breakdown  
- **Action:** `alert` → generate alerts when matched.  
- **Header:** `http $HOME_NET any -> $EXTERNAL_NET any` → applies to outbound HTTP traffic.  
- **Options:**  
  - `msg` = Alert text (“GET on wire”).  
  - `flow` = Established session to server.  
  - `content` = Looks for “GET” in HTTP method.  
  - `sid` = Unique rule ID (12345).  
  - `rev` = Revision (3).  

This rule alerts whenever Suricata detects HTTP traffic leaving the home network with “GET” in the request.  

---

## Task 2. Trigger the Custom Rule  
I ran Suricata against the supplied packet capture with my rules:  

```bash
sudo suricata -r sample.pcap -S custom.rules -k none
```  

- `-r sample.pcap` → replay the traffic.  
- `-S custom.rules` → apply my rules file.  
- `-k none` → skip checksum checks (not needed for test traffic).  

After running this, Suricata generated alerts in `/var/log/suricata/fast.log`.  

I confirmed:  

```bash
cat /var/log/suricata/fast.log
```  

Output showed alerts like:  
```
11/23/2022-12:38:34.624866  [**] [1:12345:3] GET on wire [**] {TCP} 172.21.224.2:49652 -> 142.250.1.139:80
```  

Each entry displayed the alert message, classification, priority, and traffic details.  

---

## Task 3. Examine eve.json Output  
I then inspected the richer JSON logs Suricata generated:  

```bash
jq . /var/log/suricata/eve.json | less
```  

This file contained far more context than `fast.log`, including:  
- **Severity property** → first alert had severity `3`.  
- **Destination IP** → last event showed `142.250.1.102`.  
- **Signature text** → first event used `"GET on wire"`.  

I also tested extracting specific fields:  

```bash
jq -c "[.timestamp,.flow_id,.alert.signature,.proto,.dest_ip]" /var/log/suricata/eve.json
```  

This made it easy to track:  
- Timestamps  
- Flow IDs  
- Alert signatures  
- Protocols  
- Destination IPs  

Finally, I filtered logs by flow ID:  

```bash
jq "select(.flow_id==14500150016149)" /var/log/suricata/eve.json
```  

This allowed me to correlate all events for a single network flow.  

---

## Conclusion  
By completing this activity, I gained hands-on experience in:  
- Writing and analyzing **Suricata rules**.  
- Running Suricata against captured traffic.  
- Understanding the difference between `fast.log` (quick alerts) and `eve.json` (detailed JSON logs).  

This exercise gave me practical skills to:  
1. Create and customize IDS rules.  
2. Monitor packet captures.  
3. Interpret Suricata’s logs for deeper investigation.  

These skills directly support my growth as a security analyst by improving my ability to detect, analyze, and respond to suspicious traffic.  
