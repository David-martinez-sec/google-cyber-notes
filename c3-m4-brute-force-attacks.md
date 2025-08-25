# Brute Force Attacks and OS Hardening

## Overview
Usernames and passwords are among the most common and important security controls in place today. They protect sensitive information on devices, applications, and networks. However, login credentials can be stolen or guessed by malicious actors, making them a vulnerable line of defense. One common method used by attackers is the **brute force attack**.

---

## Brute Force Attacks
A brute force attack is a **trial-and-error process** of guessing login credentials or other private information. Types include:

- **Simple brute force attack**: Attackers attempt random combinations of usernames and passwords until successful.  
- **Dictionary attack**: Attackers use lists of common passwords or stolen credentials from previous breaches. Originally, attackers used dictionary words, but now lists include more complex combinations.  

Since manual brute force is time-consuming, attackers typically use automated tools.

---

## Assessing Vulnerabilities
Organizations can assess vulnerabilities before an attack occurs using **virtual machines (VMs)** and **sandbox environments**.

### Virtual Machines (VMs)
- A VM is a **software-based computer** running in an isolated environment.  
- VMs allow analysts to run suspicious code without affecting the host machine.  
- Benefits:  
  - Safe environment for malware testing.  
  - Ability to revert to a clean state.  
  - Streamlined testing with multiple VM images.  
- Risks:  
  - Rare but possible: malware can escape virtualization and impact the host.

### Sandbox Environments
- A sandbox is a **separate environment** for executing code safely.  
- Used for testing patches, detecting bugs, or simulating attacks.  
- Can be physical machines or virtual/cloud-based systems.  
- Limitation: some malware detects sandbox/VM environments and hides its malicious behavior.

---

## Prevention Measures
To defend against brute force attacks, organizations implement layered authentication and OS hardening techniques:

- **Salting and Hashing**  
  - **Hashing**: Converts passwords into irreversible fixed values.  
  - **Salting**: Adds random characters to passwords before hashing, making precomputed attacks (e.g., rainbow tables) ineffective.

- **Multi-Factor Authentication (MFA) / Two-Factor Authentication (2FA)**  
  - Requires two or more forms of verification, such as:  
    - Passwords  
    - Biometrics (fingerprint, face ID)  
    - One-time passcodes (OTP) via SMS/email  

- **CAPTCHA / reCAPTCHA**  
  - Automated challenges to verify human users.  
  - Prevents bots from automating brute force attempts.  

- **Password Policies**  
  - Organizational rules to enforce password security:  
    - Minimum length and complexity.  
    - Regular updates and expiration periods.  
    - Restrictions on reuse.  
    - Account lockout after failed login attempts.  

---

## Key Takeaways
- **Brute force attacks** exploit weak or guessable passwords through trial-and-error or dictionary methods.  
- **VMs and sandboxes** provide safe environments for testing malware and assessing vulnerabilities.  
- **Prevention strategies** include salting and hashing, MFA/2FA, CAPTCHA, and strong password policies.  
- **OS hardening tasks** help reduce the attack surface and make brute force attempts less effective.  
