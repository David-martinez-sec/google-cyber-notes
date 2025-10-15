# The Evolution of Hash Functions

## Overview
Hash functions are algorithms that convert information into fixed-size values, or digests, which cannot be decrypted. They are widely used for authentication, non-repudiation, and data integrity. Over time, hash functions have evolved to address vulnerabilities such as collisions and rainbow table attacks.

---

## Origins of Hashing
- Early hash functions were designed to speed up data searches by creating fixed-size values for variable-length inputs.  
- **MD5 (Message Digest 5):** Developed in the early 1990s, produces 128-bit hash values. Any change in input generates a completely different output.  
- Weakness: Limited digest length makes MD5 vulnerable to collisions.  

---

## Hash Collisions
- **Collision:** When two different inputs produce the same hash value.  
- Problem: Allows attackers to impersonate authentic data.  
- MD5’s 32-character values made it especially prone to collision attacks.  

---

## Next-Generation Hashing
- To reduce collision risk, longer digests were developed in the **Secure Hash Algorithm (SHA)** family.  
- Approved by **NIST**.  
- SHA family includes:  
  - **SHA-1** → 160-bit digest (weakened, not recommended)  
  - **SHA-224, SHA-256, SHA-384, SHA-512** → considered collision-resistant.  

---

## Secure Password Storage
- Passwords should never be stored in plaintext.  
- Hashing secures passwords by converting them to fixed-size digests that can’t be reversed.  
- If an attacker gains access to a password database, hashes prevent immediate use of stolen data.  

---

## Rainbow Tables
- Pre-computed files of plaintext values mapped to their hash values.  
- Attackers use rainbow tables to compare stolen hashes against weak password values.  
- Makes short, unsalted hashes especially vulnerable.  

---

## Salting Hashes
- **Salt:** A random string of characters added before hashing.  
- Produces unique hash values even for identical inputs.  
- Example: Multiple users with the password “password” would all have different hashed values if salted.  
- Strong, unique salts make rainbow table attacks ineffective.  

---

## Key Takeaways
- Hash functions validate data integrity and protect against breaches.  
- **MD5** is weak due to collisions and short digest length.  
- **SHA algorithms** provide stronger, longer digests.  
- **Rainbow tables** exploit weak hashing; **salting** strengthens password protection.  
- Understanding hashing evolution helps security professionals recommend safer practices.  

---

## Personal Takeaways
*Your reflections here — e.g., how salting improves password security in systems you’ve used, or why moving away from MD5 matters for modern organizations.*
