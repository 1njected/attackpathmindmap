---
alias: T1491
---

## T1491

Adversaries may modify visual content available internally or externally to an enterprise network, thus affecting the integrity of the original content. Reasons for [Defacement](https://attack.mitre.org/techniques/T1491) include delivering messaging, intimidation, or claiming (possibly false) credit for an intrusion. Disturbing or offensive images may be used as a part of [Defacement](https://attack.mitre.org/techniques/T1491) in order to cause user discomfort, or to pressure compliance with accompanying messages. 



### Tactic
- [[Impact]] (TA0040)

### Platforms
- Windows
- IaaS
- Linux
- macOS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Data Backup\|M1053]] | Data Backup | Consider implementing IT disaster recovery plans that contain procedures for taking regular data backups that can be used to restore organizational data.(Citation: Ready.gov IT DRP) Ensure backups are stored off system and is protected from common methods adversaries may use to gain access and destroy the backups to prevent recovery.<br /> |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[External Defacement\|T1491.002]] | External Defacement |
| [[Internal Defacement\|T1491.001]] | Internal Defacement |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1491
