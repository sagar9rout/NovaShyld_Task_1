# 01 – Introduction to Cybersecurity

## Why I am learning this

When people hear “cybersecurity”, it is easy to imagine only hacking tools and Kali Linux. That is a small part of the picture.

For me, a better way to think about cybersecurity is: **how do we keep digital systems and the information inside them trustworthy when something eventually goes wrong?**

A company has applications, servers, employees, cloud accounts, databases, APIs, laptops and identities. Every one of those can become an entry point. Security is therefore a continuous process rather than a single product.

NIST describes cybersecurity in terms that include preventing damage, protecting systems and restoring them when necessary. Information security is also strongly connected to confidentiality, integrity and availability. [1][2]

## The attacker vs defender mindset

An attacker normally asks questions such as:

- What can I reach from outside?
- What software is exposed?
- Is anything outdated?
- Can I get around authentication?
- What information becomes available after the first compromise?
- Can I stay unnoticed?

A defender asks the same questions from the opposite direction:

- What is exposed?
- Which weaknesses are known?
- Which accounts have too much access?
- What should generate an alert?
- How do we limit the blast radius?
- How quickly can we recover?

That is the mindset I want to develop during this internship.

## Core security vocabulary

| Term | Simple meaning |
|---|---|
| Asset | Something valuable that needs protection |
| Threat | A possible cause of harm |
| Vulnerability | A weakness that could be exploited |
| Exploit | A method or action that takes advantage of a weakness |
| Risk | The potential impact and likelihood associated with a threat exploiting a weakness |
| Control | A safeguard used to reduce security risk |
| Attack surface | The reachable points where an attacker could potentially interact with a system |

NIST defines a vulnerability as a weakness in a system, security procedure, internal control or implementation that could be exploited or triggered by a threat source. [3]

## A simple chain

```text
Asset
  ↓
Weakness / Vulnerability
  ↓
Threat Actor or Threat Event
  ↓
Exploit / Abuse
  ↓
Security Incident
  ↓
Business Impact
```

The important lesson is that a vulnerability by itself is not the same thing as a breach. Context matters: exposure, exploitability, controls, attacker capability and the value of the affected asset all influence the actual risk.

## Why this matters for the rest of the internship

Task 1 gives the vocabulary we will reuse in the later tasks:

- Task 2: build a safe lab
- Task 3: discover exposed services
- Task 4: test web applications
- Task 5: combine the skills into a VAPT assessment

### Key takeaway

Cybersecurity is not “knowing hacking commands”. It is understanding systems well enough to identify what can go wrong, prove it safely, reduce the risk, and explain the result clearly.

## References

[1] NIST Cybersecurity Glossary – Cybersecurity  
https://csrc.nist.gov/glossary/term/cybersecurity

[2] NIST Cybersecurity Glossary – Information Security  
https://csrc.nist.gov/glossary/term/information_security

[3] NIST Cybersecurity Glossary – Vulnerability  
https://csrc.nist.gov/glossary/term/vulnerability
