---
alias: T1098
---

## T1098

Adversaries may manipulate accounts to maintain access to victim systems. Account manipulation may consist of any action that preserves adversary access to a compromised account, such as modifying credentials or permission groups. These actions could also include account activity designed to subvert security policies, such as performing iterative password updates to bypass password duration policies and preserve the life of compromised credentials. 

In order to create or manipulate accounts, the adversary must already have sufficient permissions on systems or the domain. However, account manipulation may also lead to privilege escalation where modifications grant access to additional roles, permissions, or higher-privileged [Valid Accounts](https://attack.mitre.org/techniques/T1078).


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
- SaaS
- Network

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Protect domain controllers by ensuring proper security configuration for critical servers to limit access by potentially unnecessary protocols and services, such as SMB file sharing. |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Protect domain controllers by ensuring proper security configuration for critical servers to limit access by potentially unnecessary protocols and services, such as SMB file sharing. |
| [[Network Segmentation\|M1030]] | Network Segmentation | Configure access controls and firewalls to limit access to critical systems and domain controllers. Most cloud environments support separate virtual private cloud (VPC) instances that enable further segmentation of cloud systems. |
| [[User Account Management\|M1018]] | User Account Management | Ensure that low-privileged user accounts do not have permissions to modify accounts or account-related policies. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Do not allow domain administrator accounts to be used for day-to-day operations that may expose them to potential adversaries on unprivileged systems. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use multi-factor authentication for user and privileged accounts. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Additional Cloud Roles\|T1098.003]] | Additional Cloud Roles |
| [[SSH Authorized Keys\|T1098.004]] | SSH Authorized Keys |
| [[Device Registration\|T1098.005]] | Device Registration |
| [[Additional Cloud Credentials\|T1098.001]] | Additional Cloud Credentials |
| [[Additional Email Delegate Permissions\|T1098.002]] | Additional Email Delegate Permissions |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1098
- Microsoft Security Event 4670: https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventID=4670
- Microsoft User Modified Event: https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/event-4738
- InsiderThreat ChangeNTLM July 2017: https://blog.stealthbits.com/manipulating-user-passwords-with-mimikatz-SetNTLM-ChangeNTLM
- GitHub Mimikatz Issue 92 June 2017: https://github.com/gentilkiwi/mimikatz/issues/92
