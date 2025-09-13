# The Rise of SSO and MFA

## Overview
Authentication is a core security control that protects access to sensitive data. Traditionally, usernames and passwords have been the standard method, but they are often insufficient. **Single sign-on (SSO)** and **multi-factor authentication (MFA)** strengthen authentication by streamlining access and requiring multiple factors to verify identity.

---

## Single Sign-On (SSO)

### Benefits of SSO
- Reduces password fatigue by minimizing the number of credentials users must remember.  
- Lowers costs by simplifying management of connected services.  
- Improves security by reducing the number of attack surfaces.  

### How SSO Works
- Uses **trusted third parties** to validate users via encrypted **access tokens**.  
- Common protocols:  
  - **LDAP (Lightweight Directory Access Protocol):** Mostly for on-premises.  
  - **SAML (Security Assertion Markup Language):** Mostly for cloud/off-premises.  
- LDAP and SAML are often used together.  

### Limitation of SSO
- Password reuse or compromise can expose multiple services.  
- SSO needs to be combined with additional safeguards.  

---

## Multi-Factor Authentication (MFA)

### How MFA Works
Requires users to present **two or more factors** to confirm identity. These include:  
1. **Something you know** → Username, password, or PIN.  
2. **Something you have** → Token or one-time passcode (OTP).  
3. **Something you are** → Biometric factors such as fingerprint or facial recognition.  

### Benefits of MFA
- Harder for attackers to impersonate users.  
- Effective for securing cloud-based access.  
- Strengthens security when combined with SSO.  

---

## Key Takeaways
- Passwords alone are a weak authentication method.  
- **SSO** simplifies the login process and reduces attack points.  
- **MFA** requires additional factors, making impersonation and brute force much more difficult.  
- Using **SSO + MFA together** improves security without harming the user experience.  

---

## Personal Takeaways
*Your reflections here — e.g., how MFA has impacted services you use, or why combining MFA with SSO is valuable in cloud security.*
