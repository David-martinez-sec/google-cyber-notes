# Module 1 – Network Components, Devices, and Diagrams

## Overview
This reading introduces network devices, their functions, and how they connect within a network. It also covers how **network diagrams** help security analysts understand and secure architectures.

---

## Network Devices
- **Network devices** connect over wired/wireless connections and send data packets.  
- Data packets include source and destination information.  
- Examples: routers, switches, computers, phones.  

---

## Everyday Devices
- **Computers, laptops, tablets, phones**  
  - Each has a unique **MAC address** and **IP address**.  
  - Have a network interface that sends/receives packets.  
  - Connect via wired or wireless connections.

---

## Firewalls
- A **firewall** monitors and restricts traffic (incoming/outgoing).  
- Acts as a **first line of defense**.  
- Configured with rules by the organization.  
- Typically sits between internal trusted networks and untrusted external networks (like the internet).  
- One line of defense → not sufficient alone.

---

## Servers
- **Servers** provide information and services for client devices.  
- **Clients** request services → servers process the requests.  
- This is the **client-server model**.  
- Examples:  
  - DNS servers (domain name lookups)  
  - File servers (store/retrieve files)  
  - Mail servers (manage company email)  

---

## Hubs and Switches
- **Hub**:  
  - Common connection point.  
  - Repeats all traffic to all ports.  
  - Vulnerable to eavesdropping → rarely used today.  
  - Common only in small setups (like home offices).  

- **Switch**:  
  - Forwards packets directly to intended device.  
  - Uses **MAC address table** to match addresses to switch ports.  
  - Operates at the **data link layer** of TCP/IP.  
  - Improves performance and security → preferred over hubs.  

---

## Routers
- **Routers** connect different networks.  
- Direct traffic based on **IP addresses** in the packet header.  
- Operate at the **network layer** of TCP/IP.  
- Forward packets hop-by-hop until destination network is reached.  
- Can include firewall features to block malicious traffic.  

---

## Modems and Wireless Access Points
- **Modems**:  
  - Connect home/office to ISP.  
  - Convert ISP signals (phone, cable, fiber) into digital format.  
  - Usually connect to a router for local distribution.  
  - Enterprises often use other high-volume technologies.  

- **Wireless Access Point (WAP)**:  
  - Creates a wireless network via **radio waves**.  
  - Devices connect using **Wi-Fi protocols**.  
  - Works with routers and switches to forward data.  

---

## Network Diagrams
- **Network diagrams** = maps of devices and their connections.  
- Use icons and lines to visualize architecture.  
- Allow analysts to:  
  - Understand network structure.  
  - Plan security controls.  
  - Identify weaknesses and potential improvements.  

---

## Key Takeaways
- **Client-server model** → clients request services, servers provide them.  
- Common network devices: routers, workstations, servers, hubs, switches, modems, and WAPs.  
- **Firewalls** = first line of defense.  
- **Switches** are preferred over hubs for both performance and security.  
- **Network diagrams** help analysts visualize and secure network architectures.
