# Overview of Interception Tactics

Interception attacks occur when malicious actors capture data packets as they travel across a network. Two common methods are **packet sniffing** and **IP spoofing**. This reading introduces specific interception attacks and ways to mitigate them.

---

## Packet Sniffing

Packet sniffing is the practice of capturing and inspecting data packets across a network.  

- **Normal operation:**  
  A device’s Network Interface Card (NIC) reads transmissions. If the packet contains its MAC address, it accepts and processes it.  

- **Promiscuous mode:**  
  A NIC can be set to accept **all traffic**, even packets not addressed to its device.  

- **Attack example:**  
  Malicious actors may use tools like **Wireshark** to capture private data. They can store the data or use it to impersonate users by spoofing their IP or MAC addresses.  

---

## IP Spoofing

After sniffing packets, attackers can impersonate authorized devices by spoofing their **IP** and **MAC addresses**.  

- **Defense:** Firewalls can block unauthorized or suspicious IP packets to reduce spoofing risks.

---

## Types of Attacks

### 1. On-Path Attack
- **Description:** Attacker intercepts communication between two trusted devices (a.k.a. Man-in-the-Middle).  
- **Impact:** Theft of sensitive information (e.g., usernames, passwords) or DNS lookups.  
- **Example:** Hacker spoofs DNS responses to redirect traffic to malicious sites.  
- **Mitigation:** Encrypt data in transit using **TLS**.

---

### 2. Smurf Attack
- **Description:** Attacker spoofs an IP address and floods it with packets via the network broadcast address.  
- **Mechanism:** Often uses **ICMP ping floods**, overwhelming all devices on the network.  
- **Impact:** Creates a **Denial of Service (DoS)**, halting operations.  
- **Mitigation:** Use **next-generation firewalls (NGFWs)** that detect unusual traffic and oversized broadcasts.  

---

### 3. DoS Attack
- **Description:** Prevents a system from responding to legitimate traffic by overwhelming it with requests.  
- **Key difference from IP spoofing:**  
  - DoS attacks may use valid IP addresses.  
  - IP spoofing specifically forges IP headers with fake addresses.  
- **Impact:** Server crashes or becomes unresponsive.  
- **Mitigation:** Apply **defense-in-depth**, including encryption, anomaly detection, and firewall rules.  

---

## Key Takeaways

- **Packet sniffing** lets attackers capture and analyze data packets.  
- **IP spoofing** allows impersonation of authorized devices.  
- Common attacks include:  
  - **On-path attacks (MITM)**  
  - **Smurf attacks**  
  - **DoS attacks**  
- **Mitigation strategies:**  
  - Use encryption (TLS)  
  - Deploy NGFWs to monitor anomalies  
  - Apply defense-in-depth with multiple protective layers  

---
