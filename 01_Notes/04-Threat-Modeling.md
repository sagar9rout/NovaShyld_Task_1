# 04 – Threat Modeling

Threat modeling is basically asking:

> “If I were trying to break this system, where would I start, and what could I reach?”

The professional version is more structured.

## A simple workflow

```text
1. Identify assets
        ↓
2. Identify trust boundaries
        ↓
3. Identify entry points
        ↓
4. Identify threats
        ↓
5. Identify vulnerabilities
        ↓
6. Estimate impact and likelihood
        ↓
7. Choose controls
        ↓
8. Reassess
```

## What should we model?

Imagine a simple online application:

```text
User
  |
  | HTTPS
  v
Web Application
  |
  | Database connection
  v
Database
```

We would ask:

- What data does the user send?
- What can an unauthenticated user reach?
- What happens if the web application is compromised?
- Can the application account read everything in the database?
- Can the database be reached directly from the Internet?
- What logs would show suspicious behavior?

## STRIDE as a learning framework

A common threat-modeling framework is STRIDE:

- **Spoofing** – pretending to be someone else
- **Tampering** – changing data or behavior
- **Repudiation** – denying an action without reliable evidence
- **Information Disclosure** – exposing information to unauthorized parties
- **Denial of Service** – making a service unavailable
- **Elevation of Privilege** – obtaining more permissions than intended

STRIDE is useful because it gives a beginner a checklist instead of relying only on intuition.

## Threat modeling is not the same as vulnerability scanning

A scanner asks:

> “What known weaknesses can I find?”

Threat modeling asks:

> “How could this system be abused, and what would the consequences be?”

Both are useful, but they answer different questions.

## Equifax lesson

The Equifax case shows why threat modeling has to include more than the public-facing application.

The initial vulnerable application was only the beginning. According to the FTC, attackers were able to reach other databases and found administrative credentials stored in plain text. The FTC also alleged that network segmentation and intrusion-detection protections were insufficient. [1]

A stronger threat model would have considered the blast radius of a compromised public-facing application.

## Defensive questions

For every system we build later, I want to ask:

1. What is the most valuable asset?
2. What is Internet-facing?
3. What happens if that component is compromised?
4. What identity does the compromised component use?
5. What can that identity access?
6. Where are the trust boundaries?
7. What logs would reveal the attack?
8. What control limits the blast radius?

That is the beginning of thinking like a security engineer.

## Reference

[1] FTC – Equifax settlement and security failures  
https://www.ftc.gov/news-events/news/press-releases/2019/07/equifax-pay-575-million-part-settlement-ftc-cfpb-states-related-2017-data-breach
