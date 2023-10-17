---
alias: T1072
---

## T1072

Adversaries may gain access to and use third-party software suites installed within an enterprise network, such as administration, monitoring, and deployment systems, to move laterally through the network. Third-party applications and software deployment systems may be in use in the network environment for administration purposes (e.g., SCCM, HBSS, Altiris, etc.).

Access to a third-party network-wide or enterprise-wide software system may enable an adversary to have remote code execution on all systems that are connected to such a system. The access may be used to laterally move to other systems, gather information, or cause a specific effect, such as wiping the hard drives on all endpoints.

The permissions required for this action vary by system configuration; local credentials may be sufficient with direct access to the third-party system, or specific domain credentials may be required. However, the system may require an administrative account to log in or to perform it's intended purpose.


### Tactic
- [[Execution]] (TA0002)
- [[Lateral Movement]] (TA0008)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required
- User
- Administrator
- SYSTEM

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Remote Data Storage\|M1029]] | Remote Data Storage | If the application deployment system can be configured to deploy only signed binaries, then ensure that the trusted signing certificates are not co-located with the application deployment system and are instead located on a system that cannot be accessed remotely or to which remote access is tightly controlled. |
| [[User Training\|M1017]] | User Training | Have a strict approval policy for use of deployment systems. |
| [[Network Segmentation\|M1030]] | Network Segmentation | Ensure proper system isolation for critical network systems through use of firewalls. |
| [[Password Policies\|M1027]] | Password Policies | Verify that account credentials that may be used to access deployment systems are unique and not used throughout the enterprise network. |
| [[User Account Management\|M1018]] | User Account Management | Ensure that any accounts used by third-party providers to access these systems are traceable to the third-party and are not used throughout the network or used by other third-party providers in the same environment. Ensure there are regular reviews of accounts provisioned to these systems to verify continued business need, and ensure there is governance to trace de-provisioning of access that is no longer required. Ensure proper system and access isolation for critical network systems through use of account privilege separation. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Grant access to application deployment systems only to a limited number of authorized administrators. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Ensure proper system and access isolation for critical network systems through use of multi-factor authentication. |
| [[Active Directory Configuration\|M1015]] | Active Directory Configuration | Ensure proper system and access isolation for critical network systems through use of group policy. |
| [[Update Software\|M1051]] | Update Software | Patch deployment systems regularly to prevent potential remote access through [Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068). |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1072
