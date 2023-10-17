---
alias: T1546
---

## T1546

Adversaries may establish persistence and/or elevate privileges using system mechanisms that trigger execution based on specific events. Various operating systems have means to monitor and subscribe to events such as logons or other user activity such as running specific applications/binaries. Cloud environments may also support various functions and services that monitor and can be invoked in response to specific cloud events.(Citation: Backdooring an AWS account)(Citation: Varonis Power Automate Data Exfiltration)(Citation: Microsoft DART Case Report 001)

Adversaries may abuse these mechanisms as a means of maintaining persistent access to a victim via repeatedly executing malicious code. After gaining access to a victim system, adversaries may create/modify event triggers to point to malicious content that will be executed whenever the event trigger is invoked.(Citation: FireEye WMI 2015)(Citation: Malware Persistence on OS X)(Citation: amnesia malware)

Since the execution can be proxied by an account with higher permissions, such as SYSTEM or service accounts, an adversary may be able to abuse these triggered execution mechanisms to escalate their privileges. 


### Tactic
- [[Privilege Escalation]] (TA0004)
- [[Persistence]] (TA0003)

### Platforms
- Linux
- macOS
- Windows
- SaaS
- IaaS
- Office 365

### Permissions Required

### Mitigations

### Sub-techniques

| ID | Name |
| --- | --- |
| [[PowerShell Profile\|T1546.013]] | PowerShell Profile |
| [[LC_LOAD_DYLIB Addition\|T1546.006]] | LC_LOAD_DYLIB Addition |
| [[Application Shimming\|T1546.011]] | Application Shimming |
| [[Trap\|T1546.005]] | Trap |
| [[Image File Execution Options Injection\|T1546.012]] | Image File Execution Options Injection |
| [[Accessibility Features\|T1546.008]] | Accessibility Features |
| [[AppCert DLLs\|T1546.009]] | AppCert DLLs |
| [[Windows Management Instrumentation Event Subscription\|T1546.003]] | Windows Management Instrumentation Event Subscription |
| [[Change Default File Association\|T1546.001]] | Change Default File Association |
| [[Emond\|T1546.014]] | Emond |
| [[Unix Shell Configuration Modification\|T1546.004]] | Unix Shell Configuration Modification |
| [[Component Object Model Hijacking\|T1546.015]] | Component Object Model Hijacking |
| [[AppInit DLLs\|T1546.010]] | AppInit DLLs |
| [[Screensaver\|T1546.002]] | Screensaver |
| [[Installer Packages\|T1546.016]] | Installer Packages |
| [[Netsh Helper DLL\|T1546.007]] | Netsh Helper DLL |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1546
- FireEye WMI 2015: https://www.fireeye.com/content/dam/fireeye-www/global/en/current-threats/pdfs/wp-windows-management-instrumentation.pdf
- Microsoft DART Case Report 001: https://www.microsoft.com/security/blog/2020/03/09/real-life-cybercrime-stories-dart-microsoft-detection-and-response-team
- amnesia malware: https://researchcenter.paloaltonetworks.com/2017/04/unit42-new-iotlinux-malware-targets-dvrs-forms-botnet/
- Backdooring an AWS account: https://medium.com/daniel-grzelak/backdooring-an-aws-account-da007d36f8f9
- Varonis Power Automate Data Exfiltration: https://www.varonis.com/blog/power-automate-data-exfiltration
- Malware Persistence on OS X: https://www.virusbulletin.com/uploads/pdf/conference/vb2014/VB2014-Wardle.pdf
