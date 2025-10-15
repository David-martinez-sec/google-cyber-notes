# Indicators of Compromise  

**Course 6 – Module 3**  
_File: c6_m3_indicators_of_compromise.md_  

---

## Indicators of Compromise (IoCs)  
- **Definition:** Observable evidence suggesting a potential security incident.  
- Examples:  
  - File names tied to malware.  
  - IP addresses linked to malicious activity.  
- IoCs = evidence of something that **already happened**.  

## Indicators of Attack (IoAs)  
- **Definition:** Behavioral evidence of an **active attack** in progress.  
- Examples:  
  - Suspicious process making a network connection (IoA).  
  - Filename of that process + contacted IP (IoCs).  
- IoAs = focus on **why and how** of ongoing attacks.  
- IoCs = focus on **who and what** after an incident.  

⚠️ Note: IoCs don’t always confirm an incident; they could be caused by human error or system malfunctions.  

---

## Pyramid of Pain  
Created by **David J. Bianco** to illustrate IoC usefulness vs. attacker difficulty.  
- Goal: Help defenders prioritize which IoCs to block for maximum impact.  

### Levels of the Pyramid  
1. **Hash Values** → Unique identifiers of malicious files.  
   - Easy for attackers to evade (change file hash).  

2. **IP Addresses** → Malicious IPs.  
   - Also easy to evade (attackers switch IPs).  

3. **Domain Names** → Malicious domains.  
   - Harder to replace than IPs but still manageable.  

4. **Network Artifacts** → Evidence in protocols (e.g., User-Agent strings).  
   - More difficult for attackers to alter consistently.  

5. **Host Artifacts** → Evidence on endpoints (e.g., malware-created files).  
   - Requires attackers to modify malware behavior.  

6. **Tools** → Software attackers rely on (e.g., password crackers).  
   - Blocking forces attackers to change tooling.  

7. **Tactics, Techniques, and Procedures (TTPs)** → Attacker behavior patterns.  
   - Hardest to change. Blocking at this level causes **maximum pain**.  

---

## Key Takeaways  
- **IoCs** = After-the-fact evidence; **IoAs** = real-time attack behaviors.  
- The **Pyramid of Pain** helps prioritize IoC blocking.  
- The higher up the pyramid you block, the more difficult you make it for attackers to continue.  
- Effective defense = combining IoCs, IoAs, and TTP awareness.  
