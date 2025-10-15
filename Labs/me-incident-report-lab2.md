# Cybersecurity Incident Report

## Section 1: Identification of the Attack

**Incident Summary:**  
The company’s sales webpage became inaccessible, returning connection timeout errors for employees and customers.  

**Log Findings:**  
- An abnormally high number of **TCP SYN requests** were observed in packet captures.  
- The requests originated from a suspicious, unfamiliar IP address.  
- The server was unable to establish stable connections with legitimate users.  

**Attack Classification:**  
This event is consistent with a **Denial of Service (DoS) attack** using the **SYN flood** method, which exploits the TCP three-way handshake process.  

---

## Section 2: Analysis of the Attack

**Normal TCP Three-Way Handshake:**  
1. A client sends a **SYN** packet to request a connection with the server.  
2. The server replies with a **SYN-ACK** to acknowledge the request.  
3. The client responds with an **ACK**, completing the handshake and establishing the connection.  

**Attack Behavior:**  
- In a SYN flood, the attacker sends a **large volume of SYN packets** without completing the handshake.  
- The server allocates resources for each half-open connection, waiting for the final ACK.  
- With too many half-open connections, the server becomes overwhelmed and **cannot process legitimate requests**.  

**Impact on the Web Server:**  
- The web server was overloaded with SYN requests and became unresponsive.  
- Employees and customers were unable to access the sales webpage.  
- Business operations were disrupted until the server was taken offline to recover.  

---

## Section 3: Immediate Mitigation Steps

1. **Server taken offline** temporarily to allow recovery.  
2. **Firewall rule implemented** to block the attacking IP address.  
3. Monitoring systems updated to watch for repeated SYN flooding attempts.  

---

## Section 4: Next Steps & Recommendations

- **Short Term:**  
  - Continue monitoring for abnormal SYN traffic.  
  - Enable rate limiting or SYN cookies on the web server.  
  - Implement intrusion detection/prevention system (IDS/IPS) alerts for flood patterns.  

- **Long Term:**  
  - Consider deploying a **Web Application Firewall (WAF)** or a **DDoS mitigation service**.  
  - Regularly review and update firewall rules.  
  - Train staff on recognizing early indicators of DoS/DDoS activity.  

---

**Conclusion:**  
The incident was identified as a **SYN flood attack**, a type of DoS attack. The attacker exploited the TCP handshake process to overwhelm the server, preventing legitimate connections. While immediate mitigation reduced the impact, additional safeguards are recommended to protect against future attempts.  
