---
alias: T1078.003
---

## T1078.003

Adversaries may obtain and abuse credentials of a local account as a means of gaining Initial Access, Persistence, Privilege Escalation, or Defense Evasion. Local accounts are those configured by an organization for use by users, remote support, services, or for administration on a single system or service.

Local Accounts may also be abused to elevate privileges and harvest credentials through [OS Credential Dumping](https://attack.mitre.org/techniques/T1003). Password reuse may allow the abuse of local accounts across a set of machines on a network for the purposes of Privilege Escalation and Lateral Movement. 


### Tactic
- [[Defense Evasion]] (TA0005)
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)
- [[Initial Access]] (TA0001)

### Platforms
- Linux
- macOS
- Windows
- Containers

### Permissions Required
- Administrator
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Password Policies\|M1027]] | Password Policies | Ensure that local administrator accounts have complex, unique passwords across all systems on the network. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Audit local accounts permission levels routinely to look for situations that could allow an adversary to gain wide access by obtaining credentials of a privileged account. (Citation: TechNet Credential Theft) (Citation: TechNet Least Privilege) These audits should check if new local accounts are created that have not be authorized. Implementing LAPS may help prevent reuse of local administrator credentials across a domain.(Citation: Microsoft Remote Use of Local) |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1078/003
