---
alias: T1037
---

## T1037

Adversaries may use scripts automatically executed at boot or logon initialization to establish persistence. Initialization scripts can be used to perform administrative functions, which may often execute other programs or send information to an internal logging server. These scripts can vary based on operating system and whether applied locally or remotely.  

Adversaries may use these scripts to maintain persistence on a single system. Depending on the access configuration of the logon scripts, either local credentials or an administrator account may be necessary. 

An adversary may also be able to escalate their privileges since some boot or logon initialization scripts run with higher privileges.


### Tactic
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)

### Platforms
- macOS
- Windows
- Linux

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Restrict write access to logon scripts to specific administrators. |
| [[Restrict Registry Permissions\|M1024]] | Restrict Registry Permissions | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for logon scripts that may lead to persistence. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Login Hook\|T1037.002]] | Login Hook |
| [[Startup Items\|T1037.005]] | Startup Items |
| [[Network Logon Script\|T1037.003]] | Network Logon Script |
| [[RC Scripts\|T1037.004]] | RC Scripts |
| [[Logon Script (Windows)\|T1037.001]] | Logon Script (Windows) |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1037
