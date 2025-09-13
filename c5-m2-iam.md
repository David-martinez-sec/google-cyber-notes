# Identity and Access Management (IAM)

## Overview
Security is about more than technologies and processes — it’s about creating an environment that supports defense strategies. Two key principles help limit access to resources:  
- **Least privilege:** Grant only the minimum access needed.  
- **Separation of duties:** Divide responsibilities so no user has too much control.  

IAM is a framework that combines these principles with authentication and authorization to ensure the right people, devices, or systems access the right resources.

---

## IAM and AAA
- **AAA (Authentication, Authorization, Accounting):** Traditional model for verifying and monitoring user access.  
- **IAM (Identity and Access Management):** A broader, modern framework that helps organizations manage digital identities.  
- Both ensure the right user gets access to the right resources, at the right time, for the right reasons.  

---

## Authentication
- Authentication proves a user is who they claim to be.  
- Methods:  
  - **Something you know** (password, PIN)  
  - **Something you have** (token, OTP)  
  - **Something you are** (fingerprint, facial scan)  
- Tools: **Single Sign-On (SSO)**, **Multi-Factor Authentication (MFA)**.  

---

## User Provisioning
- **Provisioning:** Creating and maintaining a user’s digital identity with proper access rights.  
- **Deprovisioning:** Removing user access when no longer required.  
- Example: Creating an instructor account at a college, then deprovisioning when they leave.  

---

## Authorization Models

### Mandatory Access Control (MAC)
- Strictest model; access granted by a central authority.  
- Common in law enforcement, military, government.  
- Also known as **non-discretionary control**.  

### Discretionary Access Control (DAC)
- Access determined by the data owner.  
- Example: Sharing permissions on a Google Drive folder.  

### Role-Based Access Control (RBAC)
- Access granted based on a user’s role within the organization.  
- Example: Marketing staff access analytics but not network administration.  

---

## Access Control Technologies
- Authentication and authorization often appear seamless due to integrated tools.  
- Typical IAM or AAA systems include:  
  - User directory  
  - Management tools  
  - Authorization system  
  - Auditing system  
- Options: Custom-built vs licensed third-party solutions.  
- Importance: Correct configuration is essential for creating secure environments.  

---

## Key Takeaways
- IAM and AAA frameworks enforce least privilege and separation of duties.  
- Analysts often handle **provisioning and deprovisioning** users.  
- Three access models: **MAC, DAC, RBAC**.  
- IAM ensures users access the right resources, at the right time, for the right reasons.  

---

## Personal Takeaways
*Your reflections here — e.g., which access control model you’ve seen in practice, or why provisioning/deprovisioning is critical in preventing insider threats.*
