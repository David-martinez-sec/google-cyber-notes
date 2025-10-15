**Incident report analysis**

**Instructions**

As you continue through this course, you may use this template to record your findings after completing an activity or to take notes on what you've learned about a specific tool or concept. You can also use this chart as a way to practice applying the NIST framework to different situations you encounter.

| Summary | The organization experienced a DDoS attack caused by an ICMP flood through an unconfigured firewall, resulting in a two-hour outage. |  |  |
| :---- | :---- | ----- | ----- |
| Identify | To strengthen the organization’s ability to anticipate threats, all network assets must be cataloged and regularly reviewed to ensure visibility into critical systems and services. Risk assessments should be conducted to uncover vulnerabilities such as firewall misconfigurations, and governance policies must clearly define responsibilities for maintaining secure network operations. Establishing this baseline allows the company to better understand its current risk exposure and prioritize resources accordingly. |  |  |
| Protect | Security protections will focus on access management and the implementation of technical controls. Administrative privileges to firewalls and network devices should be limited to authorized staff, and firewall rules must be configured to rate-limit ICMP traffic and prevent source IP spoofing. Network segmentation can provide additional isolation for critical services, reducing the blast radius of potential attacks. Alongside technical controls, staff should receive training to ensure proper configuration management and awareness of risks associated with insecure practices. |  |  |
| Detect | Detection capabilities must be improved to ensure abnormal traffic patterns are identified before they can disrupt operations. Continuous monitoring through network security tools will provide visibility into traffic flows, while IDS and IPS devices can generate alerts based on predefined thresholds. Logging from firewalls and detection systems should be centralized and actively analyzed to identify spikes in ICMP traffic or other anomalies indicative of a DDoS attempt. |  |  |
| Respond | The response process must be formalized in an incident response plan that includes a DDoS-specific playbook. Security analysts should be prepared to analyze IDS/IPS logs and monitoring data to identify traffic sources and distinguish malicious activity from legitimate requests. Mitigation actions, such as dynamically filtering ICMP traffic while preserving normal operations, need to be coordinated in real time. Clear communication channels should also be established to ensure leadership and potentially impacted customers are informed quickly and accurately during an incident. |  |  |
| Recover | The recovery process will focus on restoring network services and improving resiliency for future events. Non-critical services should be brought back online systematically once mitigation steps have been applied, and post-incident reviews must be conducted to refine firewall rules, IDS/IPS signatures, and monitoring thresholds. Transparent communication with stakeholders regarding the incident’s root cause and the remediation measures implemented will help rebuild trust while reinforcing accountability. |  |  |

---

| Reflections/Notes: By aligning with the NIST Cybersecurity Framework, the organization can significantly improve its ability to withstand and recover from DDoS attacks. This structured approach strengthens prevention through secure configurations, enhances detection with monitoring and IDS/IPS integration, ensures coordinated response through predefined playbooks, and reinforces resilience by integrating lessons learned into ongoing security operations. |
| :---- |

