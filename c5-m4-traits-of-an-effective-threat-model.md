# Traits of an Effective Threat Model

## Overview

Threat modeling is the process of identifying assets, their
vulnerabilities, and how each is exposed to threats. It combines
activities such as vulnerability management, threat analysis, and
incident response. Security teams use it to ensure adequate protection
and proactively reduce risks.

Traditionally, threat modeling is associated with **application
development**, but its principles apply broadly to systems and business
processes.

## Why Application Security Matters

-   Applications are central to modern organizations (web-based and
    mobile).\
-   Applications process huge amounts of data, making security
    critical.\
-   Example: **Log4Shell vulnerability (CVE-2021-44228)** in Java
    logging libraries allowed remote code execution. If unpatched,
    millions of devices could be compromised.

## Defending the Application Layer

Threat modeling ensures applications meet security requirements.
Typically performed by **DevSecOps teams**.

### Threat Modeling Cycle

1.  Define the scope\
2.  Identify threats\
3.  Characterize the environment\
4.  Analyze threats\
5.  Mitigate risks\
6.  Evaluate findings

> Best practice: Perform threat modeling before, during, and after
> application development.\
> Integrate it into every stage of the **Software Development Lifecycle
> (SDLC)**.

## Common Threat Modeling Frameworks

### STRIDE

-   Developed by Microsoft.\
-   Identifies vulnerabilities in six attack vectors:
    -   **S**poofing\
    -   **T**ampering\
    -   **R**epudiation\
    -   **I**nformation disclosure\
    -   **D**enial of service\
    -   **E**levation of privilege

### PASTA (Process of Attack Simulation and Threat Analysis)

-   Risk-centric, evidence-based framework developed by OWASP leaders
    and VerSprite.\
-   Seven-stage process using artifacts like vulnerability reports.\
-   Focus: Discovering evidence of viable threats and modeling them.

### Trike

-   Open source methodology and tool.\
-   Focuses on security permissions, application use cases, and
    privilege models.\
-   Provides a **security-centric approach** to modeling.

### VAST (Visual, Agile, and Simple Threat Modeling)

-   Part of **ThreatModeler® platform**.\
-   Designed for automation and scalability.\
-   Used to streamline and simplify assessments.

## Participating in Threat Modeling

Threat modeling is collaborative and not limited to experts.
Applications are complex, requiring multiple perspectives.

### Key Questions

-   What are we working on?\
-   What kinds of things can go wrong?\
-   What are we doing about it?\
-   Have we addressed everything?\
-   Did we do a good job?

> Anyone can contribute to threat modeling by applying an **attacker
> mindset** and asking the right questions.

## Key Takeaways

-   Application security is critical for protecting data privacy and
    integrity.\
-   Threat modeling ensures security controls are in place.\
-   Building expertise requires practice, but even junior analysts can
    contribute effectively.\
-   The goal is to think like an attacker and evaluate how data is
    handled at every stage.
