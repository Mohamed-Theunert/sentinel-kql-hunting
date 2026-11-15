# Active Directory Detection Engineering

Practical KQL detections and hunting queries for monitoring on-premises Active Directory with Microsoft Sentinel and Microsoft Defender XDR.

## Goals

- Detect high-value Active Directory security events
- Reduce noise by focusing on meaningful attack patterns
- Map detections to MITRE ATT&CK
- Document expected false positives and investigation steps
- Keep queries generic and safe for public reuse

## Structure

```text
ad/
├── detections/
│   ├── account-management/
│   ├── privileged-groups/
│   ├── domain-controllers/
│   └── directory-changes/
├── docs/
│   └── event-ids.md
└── watchlists/
    └── privileged-groups.example.csv
```

## Detection template

Each detection should document:

- Name
- Description
- Severity
- Data source
- Windows Event IDs
- MITRE ATT&CK mapping
- KQL query
- Expected false positives
- Investigation guidance
- Tuning notes

## Initial detections

| Detection | Severity | Events |
|---|---|---|
| Privileged group membership added | High | 4728, 4732, 4756 |
| New user account created | Medium | 4720 |
| RDP logon to a domain controller | High | 4624 / LogonType 10 |
| Sensitive AD object attribute modified | High | 5136 |

## Important

The queries in this repository are examples and must be validated against the schema, audit policy, naming conventions, and baseline of the target environment before being enabled as production analytics rules.

Do not publish real internal domain names, server names, usernames, IP addresses, group names, or other sensitive organizational information.
