# Use SIEM Tools to Protect Organizations

## Overview
Security Information and Event Management (SIEM) tools provide critical insights into potential threats, risks, and vulnerabilities through dashboards that collect, monitor, and analyze log data. Two widely used SIEM solutions are **Splunk** and **Chronicle**.

---

## Splunk
Splunk offers two main SIEM options:
- **Splunk® Enterprise**
- **Splunk® Cloud**

Both allow security professionals to manage internal infrastructure by reviewing dashboards that gather log data from multiple sources.

### Key Splunk Dashboards
- **Security Posture Dashboard**  
  Displays notable security events and trends from the last 24 hours. Helps SOC teams monitor and investigate potential threats in real-time, such as suspicious network activity from a specific IP.

- **Executive Summary Dashboard**  
  Tracks the overall health of an organization’s security posture over time. Used to provide high-level summaries and trends to stakeholders.

- **Incident Review Dashboard**  
  Highlights high-risk items requiring immediate review. Offers a visual timeline of events leading up to an incident.

- **Risk Analysis Dashboard**  
  Assesses risk for specific assets (users, devices, IPs). Detects changes in activity, such as unusual login times or high network traffic, to prioritize risk mitigation.

---

## Chronicle
Chronicle is a **cloud-native SIEM** by Google, used to retain, analyze, and search log data by asset, domain, user, or IP.

### Key Chronicle Dashboards
- **Enterprise Insights Dashboard**  
  Highlights recent alerts and indicators of compromise (IOCs) with confidence scores and severity ratings. Used to detect unusual logins or data access attempts.

- **Data Ingestion and Health Dashboard**  
  Monitors log processing, sources, and success rates. Ensures logs are received and processed correctly.

- **IOC Matches Dashboard**  
  Displays top threats and vulnerabilities over time, such as suspicious domains, IPs, and devices, to identify trends and prioritize threats.

- **Main Dashboard**  
  Provides a high-level summary of ingestion, alerting, and event activity over time, including timelines of incidents like spikes in failed logins.

- **Rule Detections Dashboard**  
  Shows incidents with the highest occurrences and severities. Lists alerts triggered by specific detection rules (e.g., malicious email attachments).

- **User Sign-In Overview Dashboard**  
  Tracks user access behavior, highlighting unusual activity such as logins from multiple locations simultaneously.

---

## Key Takeaways
- SIEM dashboards enable security professionals to organize, prioritize, and address security issues efficiently.
- They help identify and mitigate high-priority threats, risks, and vulnerabilities.
- Familiarity with SIEM tools like Splunk and Chronicle is essential for reducing organizational risk.
