---
alias: T1136
---

## T1136

Adversaries may create an account to maintain access to victim systems. With a sufficient level of access, creating such accounts may be used to establish secondary credentialed access that do not require persistent remote access tools to be deployed on the system.

Accounts may be created on the local system or within a domain or cloud tenant. In cloud environments, adversaries may create accounts that only have access to specific services, which can reduce the chance of detection.


### Tactic
- [[Persistence]] (TA0003)

### Platforms
- Windows
- Azure AD
- Office 365
- IaaS
- Linux
- macOS
- Google Workspace
- Network

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Protect domain controllers by ensuring proper security configuration for critical servers. |
| [[Network Segmentation\|M1030]] | Network Segmentation | Configure access controls and firewalls to limit access to domain controllers and systems used to create and manage accounts. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Do not allow domain administrator accounts to be used for day-to-day operations that may expose them to potential adversaries on unprivileged systems. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use multi-factor authentication for user and privileged accounts. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Local Account\|T1136.001]] | Local Account |
| [[Domain Account\|T1136.002]] | Domain Account |
| [[Cloud Account\|T1136.003]] | Cloud Account |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1136
- Microsoft User Creation Event: https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/event-4720
