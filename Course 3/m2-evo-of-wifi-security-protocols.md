# Module 1 – The Evolution of Wireless Security Protocols

## Overview
- Wireless networking emerged in the late 1990s/2000s as devices began sending/receiving data via radio frequencies.  
- Wi-Fi refers to IEEE **802.11 standards**, managed by the Wi-Fi Alliance.  
- Wireless security protocols evolved from **WEP → WPA → WPA2 → WPA3** to address vulnerabilities.  

---

## Wired Equivalent Privacy (WEP)
- Introduced: **1999**.  
- Goal: Provide wireless security equal to wired connections.  
- Weakness: Encryption can be easily cracked.  
- Status: **Outdated and insecure**, but may still appear in legacy devices.  
- Security risk: High-risk if still in use.  

---

## Wi-Fi Protected Access (WPA)
- Introduced: **2003** as a replacement for WEP.  
- Transitional → backward-compatible with older hardware.  
- Uses **TKIP (Temporal Key Integrity Protocol)** for stronger encryption.  
- Adds **message integrity check** to prevent packet tampering/replay.  
- Vulnerability: Susceptible to **KRACK attacks** (key reinstallation).  
- Status: Replaced by WPA2 due to flaws.  

---

## WPA2
- Introduced: **2004**, became the **standard for Wi-Fi security**.  
- Uses **AES (Advanced Encryption Standard)**.  
- Implements **CCMP (Counter Mode Cipher Block Chain Message Authentication Code Protocol)** for integrity + authentication.  
- Still vulnerable to **KRACK attacks**.  

### WPA2 Modes
- **Personal (Pre-shared Key / PSK):**  
  - Simple setup → one passphrase shared across all devices.  
  - Best for **home networks**, not scalable for organizations.  

- **Enterprise (802.1X):**  
  - Centralized authentication server (RADIUS).  
  - Individualized user access → admins can revoke/modify permissions.  
  - Users never see encryption keys → stronger against key recovery attacks.  

---

## WPA3
- Introduced: **2018**, addressing WPA2’s vulnerabilities.  
- Key Improvements:  
  - Protects against **KRACK attacks** using **SAE (Simultaneous Authentication of Equals)**.  
  - Prevents offline password cracking → attackers cannot download traffic to brute-force later.  
  - Stronger encryption:  
    - WPA3-Personal: **128-bit encryption**.  
    - WPA3-Enterprise: optional **192-bit encryption**.  
- Adoption: Growing as more devices support WPA3.  

---

## Key Takeaways
- **WEP → WPA → WPA2 → WPA3** shows the ongoing evolution of Wi-Fi security.  
- WEP and WPA are insecure and should not be used.  
- WPA2 remains widely used, but WPA3 is the **most secure** and future standard.  
- Security analysts must ensure devices use the latest wireless security protocol to mitigate vulnerabilities.  
