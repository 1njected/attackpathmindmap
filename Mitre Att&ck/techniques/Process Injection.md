---
alias: T1055
---

## T1055

Adversaries may inject code into processes in order to evade process-based defenses as well as possibly elevate privileges. Process injection is a method of executing arbitrary code in the address space of a separate live process. Running code in the context of another process may allow access to the process's memory, system/network resources, and possibly elevated privileges. Execution via process injection may also evade detection from security products since the execution is masked under a legitimate process. 

There are many different ways to inject code into a process, many of which abuse legitimate functionalities. These implementations exist for every major OS but are typically platform specific. 

More sophisticated samples may perform multiple process injections to segment modules and further evade detection, utilizing named pipes or other inter-process communication (IPC) mechanisms as a communication channel. 


### Tactic
- [[Defense Evasion]] (TA0005)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Behavior Prevention on Endpoint\|M1040]] | Behavior Prevention on Endpoint | Some endpoint security solutions can be configured to block some types of process injection based on common sequences of behavior that occur during the injection process. For example, on Windows 10, Attack Surface Reduction (ASR) rules may prevent Office applications from code injection. (Citation: win10_asr) |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Utilize Yama (ex: /proc/sys/kernel/yama/ptrace_scope) to mitigate ptrace based process injection by restricting the use of ptrace to privileged users only. Other mitigation controls involve the deployment of security kernel modules that provide advanced access control and process restrictions such as SELinux, grsecurity, and AppArmor. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | ###Linux<br /><br />Utilize Yama to mitigate ptrace based process injection by restricting the use of ptrace to privileged users only. Other mitigation controls involve the deployment of security kernel modules that provide advanced access control and process restrictions such as SELinux, grsecurity, and AppArmor. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Extra Window Memory Injection\|T1055.011]] | Extra Window Memory Injection |
| [[Thread Execution Hijacking\|T1055.003]] | Thread Execution Hijacking |
| [[Process Doppelgänging\|T1055.013]] | Process Doppelgänging |
| [[Asynchronous Procedure Call\|T1055.004]] | Asynchronous Procedure Call |
| [[Portable Executable Injection\|T1055.002]] | Portable Executable Injection |
| [[VDSO Hijacking\|T1055.014]] | VDSO Hijacking |
| [[Process Hollowing\|T1055.012]] | Process Hollowing |
| [[Proc Memory\|T1055.009]] | Proc Memory |
| [[Thread Local Storage\|T1055.005]] | Thread Local Storage |
| [[Ptrace System Calls\|T1055.008]] | Ptrace System Calls |
| [[ListPlanting\|T1055.015]] | ListPlanting |
| [[Dynamic-link Library Injection\|T1055.001]] | Dynamic-link Library Injection |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1055
- GNU Acct: https://www.gnu.org/software/acct/
- Elastic Process Injection July 2017: https://www.endgame.com/blog/technical-blog/ten-process-injection-techniques-technical-survey-common-and-trending-process
- RHEL auditd: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/security_guide/chap-system_auditing
- Microsoft Sysmon v6 May 2017: https://docs.microsoft.com/sysinternals/downloads/sysmon
- Chokepoint preload rootkits: http://www.chokepoint.net/2014/02/detecting-userland-preload-rootkits.html
