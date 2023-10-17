---
alias: T1092
---

## T1092

Adversaries can perform command and control between compromised hosts on potentially disconnected networks using removable media to transfer commands from system to system. Both systems would need to be compromised, with the likelihood that an Internet-connected system was compromised first and the second through lateral movement by [Replication Through Removable Media](https://attack.mitre.org/techniques/T1091). Commands and files would be relayed from the disconnected system to the Internet-connected system to which the adversary has direct access.


### Tactic
- [[Command and Control]] (TA0011)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Disallow or restrict removable media at an organizational policy level if they are not required for business operations.(Citation: TechNet Removable Media Control) |
| [[Disable or Remove Feature or Program\|M1042]] | Disable or Remove Feature or Program | Disable Autoruns if it is unnecessary.(Citation: Microsoft Disable Autorun) |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1092
