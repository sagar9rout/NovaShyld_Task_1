# 02 – CIA Triad

The CIA Triad is one of the easiest cybersecurity concepts to learn and one of the easiest to misunderstand.

It is not about the Central Intelligence Agency. In security, CIA means:

- **Confidentiality**
- **Integrity**
- **Availability**

NIST identifies confidentiality, integrity and availability as core security objectives. [1]

## Confidentiality

Confidentiality means information should only be available to authorized people, processes or systems.

Think about a bank account statement. It is fine for the account owner and authorized staff to see it. It is not fine for a random person on the Internet to download it.

Common controls:

- Access control
- Authentication
- Encryption
- Data classification
- Least privilege

## Integrity

Integrity means information and systems should remain accurate and protected from unauthorized modification.

For example, if a payroll database says an employee's salary is ₹50,000 and an attacker changes it to ₹5,000 without authorization, integrity has been damaged.

Common controls:

- File integrity monitoring
- Database permissions
- Hashes and digital signatures
- Change management
- Strong authorization

## Availability

Availability means authorized users can access systems and information when they need them.

A website can have excellent confidentiality and integrity and still be a security problem if nobody can use it.

Common controls:

- Backups
- Redundancy
- Monitoring
- Capacity planning
- DDoS protection
- Disaster recovery

## Why the three have to be balanced

Security decisions involve trade-offs.

For example, adding extremely restrictive access controls may improve confidentiality but hurt availability if legitimate users cannot get the data they need.

A mature security program therefore asks:

> What level of confidentiality, integrity and availability does this particular asset actually require?

## CIA in the Equifax breach

### Confidentiality — clearly compromised

The FTC states that the 2017 breach exposed personal information of approximately 147 million people, including names, dates of birth and Social Security numbers, along with payment-card information for some consumers. [2]

### Integrity — at risk, but not the main documented impact

The official sources used for this case focus primarily on unauthorized access and theft of information. They do not establish broad modification of consumer records as the main consequence.

Therefore, the responsible conclusion is:

**Integrity was a security property that needed protection, but the documented primary impact was confidentiality loss.**

### Availability — not the primary objective

The documented incident centered on unauthorized access and data theft rather than intentionally taking the service offline. Equifax later took the affected platform offline during its response. [2][3]

## My takeaway

The CIA Triad is useful because it stops us from describing every incident simply as “the system was hacked”.

Instead, we ask:

**What exactly was lost?**

- Was information exposed?
- Was information changed?
- Was the service disrupted?

That gives us a much more useful security assessment.

## References

[1] NIST – Confidentiality, Integrity, Availability  
https://csrc.nist.gov/glossary/term/confidentiality_integrity_availability

[2] FTC – Equifax settlement and breach details  
https://www.ftc.gov/news-events/news/press-releases/2019/07/equifax-pay-575-million-part-settlement-ftc-cfpb-states-related-2017-data-breach

[3] FTC – Equifax Data Breach Settlement  
https://www.ftc.gov/enforcement/refunds/equifax-data-breach-settlement
