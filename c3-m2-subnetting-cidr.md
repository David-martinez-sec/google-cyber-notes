# Module 1 – Subnetting and CIDR

## Overview
- **Subnetting** = dividing a network into smaller, logical groups (subnets).  
- Used for efficiency, security, and segmentation (e.g., security zones).  
- Builds on concepts like the **uncontrolled, controlled, DMZ, and restricted zones**.  

---

## Subnetting
- A **subnet** is like a "network inside a network."  
- Based on **IP address + subnet mask**.  
- Benefits:  
  - Devices within the same subnet communicate directly via the switch.  
  - Improves **speed and efficiency** of communications.  
  - Supports **security zoning**.  

Example:  
One router connecting to two separate subnets = two isolated networks within the same larger network.  

---

## CIDR (Classless Inter-Domain Routing)
- Introduced to replace **classful addressing** (Class A–E system of the 1980s).  
- Solved IPv4 exhaustion by making addressing more flexible.  
- **CIDR format:** `IP_address/prefix_length`.  
  - Example:  
    - IPv4: `198.51.100.0`  
    - CIDR: `198.51.100.0/24` → includes `198.51.100.0` to `198.51.100.255`.  

### Benefits of CIDR
- Reduces **routing table entries** (more efficient routing).  
- Expands number of available IPv4 addresses.  
- Allows finer-grained segmentation of networks.  

---

## Security Benefits of Subnetting
- Creates **isolated subnets** without requesting new public IP ranges.  
- Conserves bandwidth and improves performance.  
- Enables **security controls** like firewalls and routing policies between subnets.  
- Helps enforce **security zones** (DMZ, restricted zones, etc.).  

---

## Key Takeaways
- **Subnetting** = breaking a private network into smaller subnetworks.  
- **CIDR** allows more flexible IP allocation than old class-based system.  
- Both improve efficiency, scalability, and network security.  
- Subnetting is a foundational strategy for **network performance and isolation**.  
