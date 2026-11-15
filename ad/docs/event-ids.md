# Active Directory Security Event IDs

A compact reference for common Windows Security events used in Active Directory monitoring.

| Event ID | Meaning | Typical SOC use |
|---:|---|---|
| 4624 | Successful logon | Track successful authentication |
| 4625 | Failed logon | Brute force / password spray investigation |
| 4648 | Logon using explicit credentials | Alternate credential use |
| 4672 | Special privileges assigned | Privileged logon context |
| 4720 | User account created | Unexpected account creation |
| 4722 | User account enabled | Account lifecycle monitoring |
| 4724 | Password reset attempted | Sensitive account administration |
| 4725 | User account disabled | Account lifecycle monitoring |
| 4728 | Member added to global security group | Privilege escalation |
| 4732 | Member added to local security group | Privilege escalation |
| 4740 | User account locked out | Password attack / broken service |
| 4756 | Member added to universal security group | Privilege escalation |
| 4768 | Kerberos TGT requested | Kerberos authentication monitoring |
| 4769 | Kerberos service ticket requested | Kerberoasting / service access analysis |
| 4771 | Kerberos pre-authentication failed | Authentication failure analysis |
| 4776 | NTLM credential validation | NTLM usage monitoring |
| 5136 | Directory Service object modified | Sensitive AD / GPO attribute changes |

## Notes

- Event presence depends on Windows audit policy and log collection configuration.
- A single event is rarely enough to determine malicious activity.
- Correlate events with account role, source host, time, target object, and surrounding activity.
