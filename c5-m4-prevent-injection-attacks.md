# Prevent Injection Attacks

## Overview

Structured Query Language (SQL) is widely used to create, interact with,
and request information from databases. Due to its popularity, **SQL
injection** is a common attack vector and is consistently listed in the
OWASP® Top 10. Attackers use SQL injection to modify, delete, or steal
data by exploiting vulnerable input fields in applications.

## SQL Queries

-   A database is an organized collection of data (e.g., employee
    records, customer payment details).\
-   SQL organizes data into **tables** and retrieves it using
    **queries**.\
-   Input fields like login forms, search bars, or comment boxes can be
    exploited for injections if not properly secured.\
-   SQL injection allows attackers to manipulate databases, steal data,
    or gain control of applications.

## SQL Injection Categories

### In-band SQL Injection

-   Most common type.\
-   Uses the same channel for attack and data retrieval.\
-   **Example:** A malicious query in a retailer's search box retrieves
    and displays sensitive information (e.g., user passwords).

### Out-of-band SQL Injection

-   Uses a different channel for attack and retrieval.\
-   **Example:** An attacker uses a query to create a connection between
    a vulnerable website and their own database.\
-   Rare, as it requires specific features to be enabled on the target
    server.

### Inferential SQL Injection

-   Results are not directly visible.\
-   Attackers infer details based on system behavior (e.g., error
    messages from login forms).\
-   Helps map database structure for further attacks.

## Injection Prevention

SQL queries often assume user input will be valid (e.g.,
`jdoe@domain.com`). Attackers exploit this assumption.

### Prevention Techniques

-   **Prepared statements:** Execute SQL statements safely before
    sending to a database.\
-   **Input sanitization:** Strip malicious code from user input.\
-   **Input validation:** Enforce strict input formats.

Combining these methods greatly reduces injection risks. Security
professionals often collaborate with developers to implement these
defenses.

**Resource:** [OWASP SQL Injection Prevention Cheat
Sheet](https://owasp.org/www-community/attacks/SQL_Injection)

## Key Takeaways

-   SQL is central to most web applications, making SQL injection
    attacks common and dangerous.\
-   SQL injection results from improper handling of user input.\
-   Effective prevention requires a mix of secure coding practices, user
    input handling, and developer collaboration.
