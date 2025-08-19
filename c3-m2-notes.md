# Module 1 – Additional Notes

## Firewalls
- Inspect packets before they enter a network.  
- Can be **hardware** or **software**.  
  - Software firewalls = less expensive but consume processing power.  

### Types of Firewalls
- **Stateless Firewall**  
  - Uses predefined rules, does not track active sessions.  
  - Faster, but less secure.  

- **Stateful Firewall**  
  - Tracks active connections and analyzes traffic patterns.  
  - More secure than stateless.  

- **NGFW (Next-Generation Firewall)**  
  - Offers advanced features:  
    - Deep Packet Inspection (DPI)  
    - Intrusion Prevention Systems (IPS)  
    - Cloud-based threat intelligence (real-time updates).  
  - Provides the strongest level of protection.  

---

## VPN (Virtual Private Network)
- Changes public IP address and hides virtual location.  
- Encrypts data traveling across the internet → prevents unauthorized access.  
- **Encapsulation**: wraps sensitive data into packets so it can be routed securely.  
- Creates an **encrypted tunnel** between device ↔ VPN server.  
- Requires a **cryptographic key** to access.  

### VPN Protocols
- **WireGuard**: newer, lightweight, faster.  
- **IPsec**: older, widely adopted, highly reliable.  

---

## Security Zones
- Used to **segment a network** and control access.  
- Zones:  
  - **Uncontrolled Zone** → internet (public).  
  - **Controlled Zone** → subnets like DMZ (public-facing services).  
  - **Restricted Zone** → sensitive data and internal systems.  

### Subnetting & CIDR
- **Subnetting**: divides a network into logical groups.  
- **CIDR (Classless Inter-Domain Routing):** assigns subnet masks to IP addresses.  
  - Example: `192.1.1.1/23` → `/23` indicates the subne
