# Course 7 - Module 3 Notes: Regular Expressions in Cybersecurity

## Activity Overview
This module expanded on my Python skills by focusing on **regular expressions (regex)** and their applications.  
I practiced constructing regex patterns, using Python’s `re` module, and applying `re.findall()` to extract useful information from strings.  
The course examples were helpful, but I also thought about how these skills directly tie into real-world cybersecurity work like log analysis, threat hunting, and incident response.

## What I Did
- Reviewed the **basics of regex** and how to use them with Python.  
- Learned about regex symbols for matching characters and quantifying occurrences.  
- Practiced extracting data from strings using `re.findall()`.  
- Applied regex to simulate cybersecurity-related tasks such as parsing login attempts and analyzing device IDs.  

## Key Concepts
### Basics of Regex in Python
- Regex patterns are stored as strings and used with Python’s `re` module.  
- Common workflow:  
  ```python
  import re
  pattern = "\d+"
  text = "user123"
  matches = re.findall(pattern, text)
  print(matches)
  ```
  Output: `['123']`  

### Common Regex Symbols
- **Character types**  
  - `\w` → word characters (alphanumeric + underscore)  
  - `\d` → digits [0-9]  
  - `\s` → whitespace  
  - `.` → matches any character  
  - `\.` → literal period  

- **Quantifiers**  
  - `+` → one or more occurrences  
  - `*` → zero or more occurrences  
  - `{n}` → exactly n repetitions  
  - `{m,n}` → between m and n repetitions  

### Constructing Patterns
Example: Extracting usernames and login attempts from employee logs.  
```python
import re
pattern = "\w+:\s\d+"
employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
print(re.findall(pattern, employee_logins_string))
```
Output: `['bmoreno: 12', 'tshah: 7', 'sgilmore: 5']`  

This exercise showed how to build regex from smaller chunks: username (`\w+`), colon (`:`), space (`\s`), digits (`\d+`).

## Cybersecurity Applications of Regex
Regex is essential for analysts because so much of security work involves extracting meaning from raw text, logs, or packet captures. Examples include:  
- **Log analysis:** Searching for suspicious IPs, usernames, or errors inside system logs.  
- **Threat hunting:** Detecting indicators of compromise (IOCs) like email addresses, hashes, or domains.  
- **Forensics:** Extracting file paths, registry keys, or encoded payloads from large text dumps.  
- **Network monitoring:** Identifying IPv4/IPv6 patterns, URLs, or malformed requests in traffic captures.  
- **Malware analysis:** Pulling out function names, strings, or obfuscation patterns from binaries.  

Examples of useful regex patterns for cybersecurity tasks:  
- IPv4 addresses: `(?:\d{1,3}\.){3}\d{1,3}`  
- Email addresses: `[\w.-]+@[\w.-]+`  
- MD5/SHA1/SHA256 hashes:  
  - MD5: `[a-fA-F0-9]{32}`  
  - SHA1: `[a-fA-F0-9]{40}`  
  - SHA256: `[a-fA-F0-9]{64}`  
- URLs: `https?://[\w./-]+`  

## Personal Takeaways
Regex can feel abstract at first, but in cybersecurity it’s an incredibly practical tool. Instead of scrolling manually through thousands of log entries, I can design a regex pattern to pull exactly what I need in seconds. The practice with quantifiers and character types gave me confidence to construct patterns for specific IOCs like IPs or hashes. I’ve also realized how important it is to **test and refine** regex patterns — too broad can give false positives, too narrow can miss important data.

---
*File generated for GitHub as a first-person lab note.*
