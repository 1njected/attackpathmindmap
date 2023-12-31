---
alias: T1562.010
---

## T1562.010

Adversaries may downgrade or use a version of system features that may be outdated, vulnerable, and/or does not support updated security controls such as logging. For example, [PowerShell](https://attack.mitre.org/techniques/T1059/001) versions 5+ includes Script Block Logging (SBL) which can record executed script content. However, adversaries may attempt to execute a previous version of PowerShell that does not support SBL with the intent to [Impair Defenses](https://attack.mitre.org/techniques/T1562) while running malicious scripts that may have otherwise been detected.(Citation: CrowdStrike BGH Ransomware 2021)(Citation: Mandiant BYOL 2018)(Citation: att_def_ps_logging)

Adversaries may downgrade and use less-secure versions of various features of a system, such as [Command and Scripting Interpreter](https://attack.mitre.org/techniques/T1059)s or even network protocols that can be abused to enable [Adversary-in-the-Middle](https://attack.mitre.org/techniques/T1557).(Citation: Praetorian TLS Downgrade Attack 2014)


### Tactic
- [[Defense Evasion]] (TA0005)

### Platforms
- Windows
- Linux
- macOS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Disable or Remove Feature or Program\|M1042]] | Disable or Remove Feature or Program | Consider removing previous versions of tools that are unnecessary to the environment when possible. |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1562/010
- CrowdStrike BGH Ransomware 2021: https://www.crowdstrike.com/blog/how-falcon-complete-stopped-a-big-game-hunting-ransomware-attack/
- att_def_ps_logging: https://nsfocusglobal.com/attack-and-defense-around-powershell-event-logging/
- inv_ps_attacks: https://powershellmagazine.com/2014/07/16/investigating-powershell-attacks/
- Mandiant BYOL 2018: https://www.mandiant.com/resources/bring-your-own-land-novel-red-teaming-technique
- Praetorian TLS Downgrade Attack 2014: https://www.praetorian.com/blog/man-in-the-middle-tls-ssl-protocol-downgrade-attack/
