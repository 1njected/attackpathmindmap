---
alias: T1518
---

## T1518

Adversaries may attempt to get a listing of software and software versions that are installed on a system or in a cloud environment. Adversaries may use the information from [Software Discovery](https://attack.mitre.org/techniques/T1518) during automated discovery to shape follow-on behaviors, including whether or not the adversary fully infects the target and/or attempts specific actions.

Adversaries may attempt to enumerate software for a variety of reasons, such as figuring out what security measures are present or if the compromised system has a version of software that is vulnerable to [Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068).


### Tactic
- [[Discovery]] (TA0007)

### Platforms
- Windows
- Azure AD
- Office 365
- SaaS
- IaaS
- Linux
- macOS
- Google Workspace

### Permissions Required
- User
- Administrator

### Mitigations

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Security Software Discovery\|T1518.001]] | Security Software Discovery |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1518
