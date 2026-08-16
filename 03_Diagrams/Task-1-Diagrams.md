# Task 1 Diagrams

These diagrams are intentionally simple and original. They are meant to explain the security logic rather than decorate the repository.

## CIA Triad

```mermaid
flowchart LR
    C[Confidentiality]
    I[Integrity]
    A[Availability]
    C --- I
    I --- A
    A --- C
```

## Risk Chain

```mermaid
flowchart LR
    T[Threat] --> V[Vulnerability]
    V --> E[Exploit or Abuse]
    E --> R[Risk / Incident]
    R --> B[Business Impact]
```

## Equifax Attack Chain

```mermaid
flowchart TD
    A[Internet-facing application] --> B[Unpatched Apache Struts]
    B --> C[CVE-2017-5638]
    C --> D[Initial access]
    D --> E[Credentials and internal access]
    E --> F[Sensitive databases]
    F --> G[Data exposure]
```
