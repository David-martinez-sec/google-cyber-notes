# Principle of Least Privilege

## Overview
The principle of least privilege (PoLP) is a security concept in which users, devices, or applications are only granted the minimum access and authorization required to complete a task or function. It supports the **confidentiality, integrity, and availability (CIA) triad** and is one of the most important security controls for reducing risk.

---

## Limiting Access Reduces Risk
Implementing least privilege reduces the likelihood of costly incidents like data breaches by:
- Limiting access to sensitive information  
- Reducing accidental modification, tampering, or data loss  
- Supporting system monitoring and administration  

By linking specific resources to specific users and limiting what they can do, least privilege reduces the attack surface.  

*Note:* Least privilege is related to **separation of duties**, where tasks are divided among different users to avoid giving one person total control over critical functions.

---

## Determining Access and Authorization
Two guiding questions for implementing least privilege:
1. **Who is the user?** (can be a person, device, or software)  
2. **How much access do they need to a resource?**

### User Account Types
- **Guest accounts**: External users (customers, clients, contractors, partners)  
- **User accounts**: Staff accounts based on job duties  
- **Service accounts**: Applications or software interacting with other services  
- **Privileged accounts**: Elevated permissions or administrative access  

**Best practice:** Establish a baseline access level per account type and adjust as needed. Example: a support agent should only access your data while actively assisting you.  

**Pro tip:** Secure passwords are critical — even properly assigned accounts can be compromised if passwords are weak.

---

## Auditing Account Privileges
Auditing ensures that accounts and privileges remain aligned with security policies. Three common approaches:

### Usage Audits
- Review what resources each account accesses and how they are used  
- Verify compliance with security policies  
- Identify permissions that can be revoked  

### Privilege Audits
- Detect **privilege creep** (gradual accumulation of excess access)  
- Ensure user roles match the resources they can access  

### Account Change Audits
- Monitor logs of account changes (e.g., password resets)  
- Identify suspicious activity  
- Ensure all changes are made by authorized users  
- Many directory services can alert admins automatically  

---

## Key Takeaways
- Least privilege reduces risk of unauthorized access to sensitive resources.  
- Correctly configuring and maintaining user accounts is essential.  
- Routine audits (usage, privilege, account change) help prevent privilege creep and detect suspicious activity.  
- This practice directly supports the CIA triad.  

---

## Personal Takeaways
*Your reflections here — e.g., how PoLP applies to your projects, GitHub repos, or how you’ve seen privilege creep in past roles.*
