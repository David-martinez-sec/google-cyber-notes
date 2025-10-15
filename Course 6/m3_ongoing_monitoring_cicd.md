# Ongoing Monitoring of CI/CD: Automatically Finding Threats  

**Course 6 – Module 3**  
_File: c6_m3_ongoing_monitoring_cicd.md_  

---

## Why CI/CD Monitoring Matters  
- CI/CD pipelines speed up software delivery but introduce new vulnerabilities.  
- Attackers may:  
  - Insert malicious code.  
  - Steal secrets.  
  - Disrupt deployments.  
- Ongoing monitoring with **automation** finds unusual activity and potential **Indicators of Compromise (IoCs)** early.  

---

## Common IoCs in CI/CD Pipelines  

### Unauthorized Code Changes  
- Commits from unauthorized users.  
- Changes at unusual times or locations.  
- Suspicious changes (large deletions, confusing code).  

### Suspicious Deployment Patterns  
- Deployments to **unapproved systems**.  
- Unexpected or excessive deployment frequency.  
- Deployments triggered by unusual accounts.  

### Compromised Dependencies  
- Known CVEs detected in dependencies.  
- Unexpected new dependencies.  
- Dependencies downloaded from untrusted sources.  

### Unusual Pipeline Execution  
- Steps failing unexpectedly.  
- Pipelines running longer than normal.  
- Step order changed without approval.  

### Secrets Exposure Attempts  
- Logs showing unauthorized secret access attempts.  
- Hardcoded secrets discovered in commits.  

---

## Proactive Monitoring Benefits  
- **Respond Quickly** → Detect IoCs early to stop attacks.  
- **Limit Damage** → Reduce attacker dwell time in pipeline.  
- **Improve Threat Knowledge** → Learn attacker TTPs for better defenses.  

---

## Automation Methods  

### 1. Comprehensive Logging & Auditing  
- **Pipeline Execution Logs** → Establish baselines of normal runs, detect anomalies.  
- **Code Commit Logs** → Track unusual changes or authors.  
- **Access Logs** → Identify odd login attempts or suspicious access.  
- **Deployment Logs** → Detect deployments outside normal times or locations.  

### 2. SIEM Integration  
- SIEMs analyze logs at scale.  
- **Automatic anomaly detection** using ML/analytics.  
- **Rule-based alerts** for known IoCs, e.g.:  
  - Malicious file hashes in builds.  
  - CI/CD contacting known C2 servers.  
  - Unauthorized access to secrets.  

### 3. Real-time Alerting & Notifications  
- Alerts for:  
  - Repeated build failures.  
  - Suspicious or unusual code changes.  
  - Secret exposure attempts.  
  - Unusual outbound traffic from CI/CD servers.  

### 4. Performance Monitoring  
- Detect Indicators of Attack (IoAs) via performance issues.  
- Sudden slowdowns or resource spikes may reveal deeper IoCs.  

### 5. Continuous Vulnerability Scanning  
- Scan CI/CD infrastructure, tools, plugins, and containers.  
- Identify CVEs and patch weaknesses promptly.  

---

## Key Takeaways  
- **Automation + Monitoring** = stronger CI/CD security.  
- Detect IoCs early → respond quickly and reduce damage.  
- Logs, SIEM, alerts, performance checks, and vuln scans all contribute.  
- Builds resilience in software pipelines and protects both organization and customers.  
