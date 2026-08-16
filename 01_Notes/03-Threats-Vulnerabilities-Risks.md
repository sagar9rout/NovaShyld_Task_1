# 03 – Threats, Vulnerabilities, Exploits and Risk

These four words appear together so often that it is easy to mix them up.

## Threat

A threat is a possible cause of harm.

Examples:

- A malicious attacker
- Ransomware
- A malicious insider
- A phishing campaign
- A natural event that affects infrastructure

NIST describes a cyber threat as a circumstance or event with the potential to adversely affect operations, assets or people through an information system. [1]

## Vulnerability

A vulnerability is a weakness that can be exploited or triggered.

Examples:

- Unpatched software
- Weak authentication
- Excessive permissions
- Insecure configuration
- Vulnerable code

NIST's definition is useful here: a vulnerability is a weakness in a system, security procedure, internal control or implementation that could be exploited or triggered by a threat source. [2]

## Exploit

An exploit is the technique, action or code used to take advantage of a vulnerability.

In the Equifax case, CVE-2017-5638 described a vulnerability in Apache Struts that could allow remote attackers to execute arbitrary commands through crafted HTTP headers. [3]

## Risk

Risk is not simply “there is a vulnerability”.

A useful way to think about it is:

```text
Risk ≈ Likelihood × Impact
```

This is a simplified mental model rather than a universal scoring formula.

A low-impact weakness on an isolated test machine is very different from a remotely exploitable weakness on a public server containing millions of sensitive records.

NIST describes information-system-related risk in terms of potential impact and likelihood. [4]

## Putting the pieces together

```text
Threat
  ↓
Looks for an exposed weakness
  ↓
Vulnerability
  ↓
Uses an exploit or abuse path
  ↓
Security event / incident
  ↓
Potential confidentiality, integrity or availability impact
```

## Equifax example

```text
Threat actor
     ↓
Internet-facing ACIS application
     ↓
Unpatched Apache Struts vulnerability
     ↓
CVE-2017-5638 exploitation
     ↓
Access to the network
     ↓
Unsecured credentials + weak internal controls
     ↓
Access to additional databases
     ↓
Large-scale data exposure
```

The important lesson is that the breach was not caused by one magic hacking command. It was a chain of technical and process failures.

## References

[1] NIST – Cyber Threat  
https://csrc.nist.gov/glossary/term/cyber_threat

[2] NIST – Vulnerability  
https://csrc.nist.gov/glossary/term/vulnerability

[3] NIST NVD – CVE-2017-5638  
https://nvd.nist.gov/vuln/detail/CVE-2017-5638

[4] NIST – Information System-Related Security Risk  
https://csrc.nist.gov/glossary/term/information_system_related_security_risks
