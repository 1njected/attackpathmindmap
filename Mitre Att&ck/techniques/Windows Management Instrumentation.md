---
alias: T1047
---

## T1047

Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads. WMI is an administration feature that provides a uniform environment to access Windows system components. The WMI service enables both local and remote access, though the latter is facilitated by [Remote Services](https://attack.mitre.org/techniques/T1021) such as [Distributed Component Object Model](https://attack.mitre.org/techniques/T1021/003) (DCOM) and [Windows Remote Management](https://attack.mitre.org/techniques/T1021/006) (WinRM).(Citation: MSDN WMI) Remote WMI over DCOM operates using port 135, whereas WMI over WinRM operates over port 5985 when using HTTP and 5986 for HTTPS.(Citation: MSDN WMI)(Citation: FireEye WMI 2015)

An adversary can use WMI to interact with local and remote systems and use it as a means to execute various behaviors, such as gathering information for Discovery as well as remote Execution of files as part of Lateral Movement. (Citation: FireEye WMI SANS 2015) (Citation: FireEye WMI 2015)


### Tactic
- [[Execution]] (TA0002)

### Platforms
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Execution Prevention\|M1038]] | Execution Prevention | Use application control configured to block execution of <code>wmic.exe</code> if it is not required for a given system or network to prevent potential misuse by adversaries. For example, in Windows 10 and Windows Server 2016 and above, Windows Defender Application Control (WDAC) policy rules may be applied to block the <code>wmic.exe</code> application and to prevent abuse.(Citation: Microsoft WDAC) |
| [[Behavior Prevention on Endpoint\|M1040]] | Behavior Prevention on Endpoint | On Windows 10, enable Attack Surface Reduction (ASR) rules to block processes created by WMI commands from running. Note: many legitimate tools and applications utilize WMI for command execution. (Citation: win10_asr) |
| [[User Account Management\|M1018]] | User Account Management | By default, only administrators are allowed to connect remotely using WMI. Restrict other users who are allowed to connect, or disallow all users to connect remotely to WMI. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Prevent credential overlap across systems of administrator and privileged accounts. (Citation: FireEye WMI 2015) |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1047
- FireEye WMI 2015: https://www.fireeye.com/content/dam/fireeye-www/global/en/current-threats/pdfs/wp-windows-management-instrumentation.pdf
- FireEye WMI SANS 2015: https://www.fireeye.com/content/dam/fireeye-www/services/pdfs/sans-dfir-2015.pdf
- MSDN WMI: https://msdn.microsoft.com/en-us/library/aa394582.aspx
