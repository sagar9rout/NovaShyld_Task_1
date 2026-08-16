# 06 – Common Attack Vectors & Social Engineering

Task 1 asks us to identify common entry points used by attackers. The point is not to memorize a list. The point is to recognize the pattern.

## 1. Phishing

An attacker tricks a person into clicking a link, opening a file, giving away credentials or performing an action.

Defensive ideas:

- Email filtering
- MFA
- User awareness
- URL and attachment analysis
- Reporting procedures

## 2. Weak or reused credentials

If a password is guessed, leaked or reused, an attacker may gain access without exploiting a software bug.

Defensive ideas:

- MFA
- Password managers
- Strong authentication
- Breached-password detection
- Least privilege

## 3. Unpatched software

Known vulnerabilities can become an entry point when organizations do not patch exposed systems.

The Equifax case is a strong example.

## 4. Misconfiguration

Examples include:

- Publicly exposed administration interfaces
- Excessive cloud permissions
- Default credentials
- Unnecessary services
- Overly permissive firewall rules

## 5. Web application vulnerabilities

Examples include:

- Injection
- Cross-site scripting
- Broken access control
- Authentication weaknesses
- Security misconfiguration

We will practice these only against the intentionally vulnerable lab targets in later tasks.

## 6. Social engineering

Social engineering targets human decision-making rather than only technical weaknesses.

A useful defensive question is:

> “What would make a normal employee trust this request?”

That leads to better awareness training than simply telling people “don't click phishing links”.

## The common pattern

```text
Attacker
   ↓
Finds a human or technical weakness
   ↓
Builds trust / sends malicious input / abuses exposure
   ↓
Obtains access
   ↓
Attempts to increase access or reach valuable data
   ↓
Collects information or causes impact
```

## Defender mindset

For every attack vector, ask:

1. Can we prevent it?
2. If prevention fails, can we detect it?
3. If detection fails, can we contain it?
4. If containment fails, can we recover?
