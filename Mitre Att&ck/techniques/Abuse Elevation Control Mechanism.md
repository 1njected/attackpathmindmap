---
alias: T1548
---

## T1548

Adversaries may circumvent mechanisms designed to control elevate privileges to gain higher-level permissions. Most modern systems contain native elevation control mechanisms that are intended to limit privileges that a user can perform on a machine. Authorization has to be granted to specific users in order to perform tasks that can be considered of higher risk. An adversary can perform several methods to take advantage of built-in control mechanisms in order to escalate privileges on a system.


### Tactic
- [[Privilege Escalation]] (TA0004)
- [[Defense Evasion]] (TA0005)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required
- Administrator
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Account Control\|M1052]] | User Account Control | Although UAC bypass techniques exist, it is still prudent to use the highest enforcement level for UAC when possible and mitigate bypass opportunities that exist with techniques such as [DLL Search Order Hijacking](https://attack.mitre.org/techniques/T1574/001). |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Applications with known vulnerabilities or known shell escapes should not have the setuid or setgid bits set to reduce potential damage if an application is compromised. Additionally, the number of programs with setuid or setgid bits set should be minimized across a system. Ensuring that the sudo tty_tickets setting is enabled will prevent this leakage across tty sessions. |
| [[Execution Prevention\|M1038]] | Execution Prevention | System settings can prevent applications from running that haven't been downloaded from legitimate repositories which may help mitigate some of these issues. Not allowing unsigned applications from being run may also mitigate some risk. |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Remove users from the local administrator group on systems.<br /><br />By requiring a password, even if an adversary can get terminal access, they must know the password to run anything in the sudoers file. Setting the timestamp_timeout to 0 will require the user to input their password every time sudo is executed. |
| [[Audit\|M1047]] | Audit | Check for common UAC bypass weaknesses on Windows systems to be aware of the risk posture and address issues where appropriate.(Citation: Github UACMe) |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Bypass User Account Control\|T1548.002]] | Bypass User Account Control |
| [[Sudo and Sudo Caching\|T1548.003]] | Sudo and Sudo Caching |
| [[Setuid and Setgid\|T1548.001]] | Setuid and Setgid |
| [[Elevated Execution with Prompt\|T1548.004]] | Elevated Execution with Prompt |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1548
