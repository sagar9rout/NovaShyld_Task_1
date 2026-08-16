# 05 – MITRE ATT&CK Basics

MITRE ATT&CK is a knowledge base of adversary tactics and techniques based on real-world observations. [1]

The easiest way for me to remember it is:

> **Tactics explain why. Techniques explain how.**

## Tactics

Examples from the Enterprise ATT&CK matrix include:

- Reconnaissance
- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Credential Access
- Discovery
- Lateral Movement
- Collection
- Command and Control
- Exfiltration
- Impact

MITRE describes tactics as the adversary's tactical goal. [2]

## Why this matters

Suppose a security alert says:

> “A public web application received a suspicious request.”

That is an event.

ATT&CK helps us put events into an adversary-behavior model.

For example:

**T1190 – Exploit Public-Facing Application**

This technique covers attempts to exploit weaknesses in Internet-facing hosts or systems to obtain initial access. [3]

## Applying ATT&CK to the Equifax case

The strongest mapping we can make from the sources we reviewed is:

| Observed behavior | ATT&CK mapping | Confidence |
|---|---|---|
| Exploitation of an Internet-facing vulnerable application | T1190 – Exploit Public-Facing Application | High |
| Remote command execution through CVE-2017-5638 | Execution occurred as a consequence of exploitation, but we should not invent a more specific technique without evidence | Moderate |
| Access and theft of sensitive information | Collection/exfiltration concepts are relevant, but exact ATT&CK technique mapping requires more evidence about how the data was collected and transferred | Moderate |

The important professional habit is **not to force a technique mapping just because it sounds plausible**.

If the evidence is weak, say so.

## Defender perspective

ATT&CK is also useful for detection.

For T1190, MITRE discusses monitoring suspicious requests to public endpoints and correlating them with unusual server behavior. [4]

That connects offensive knowledge with defensive work:

```text
Attack technique
      ↓
Observable behavior
      ↓
Log source
      ↓
Detection rule
      ↓
Alert
      ↓
Investigation
```

## Reference

[1] MITRE ATT&CK  
https://attack.mitre.org/

[2] MITRE Enterprise Tactics  
https://attack.mitre.org/tactics/

[3] MITRE T1190 – Exploit Public-Facing Application  
https://attack.mitre.org/techniques/T1190/

[4] MITRE Detection Strategy – Exploit Public-Facing Application  
https://attack.mitre.org/detectionstrategies/DET0080/
