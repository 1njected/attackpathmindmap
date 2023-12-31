---
alias: T1564
---

## T1564

Adversaries may attempt to hide artifacts associated with their behaviors to evade detection. Operating systems may have features to hide various artifacts, such as important system files and administrative task execution, to avoid disrupting user work environments and prevent users from changing files or features on the system. Adversaries may abuse these features to hide artifacts such as files, directories, user accounts, or other system activity to evade detection.(Citation: Sofacy Komplex Trojan)(Citation: Cybereason OSX Pirrit)(Citation: MalwareBytes ADS July 2015)

Adversaries may also attempt to hide artifacts associated with malicious behavior by creating computing regions that are isolated from common security instrumentation, such as through the use of virtualization technology.(Citation: Sophos Ragnar May 2020)


### Tactic
- [[Defense Evasion]] (TA0005)

### Platforms
- Linux
- macOS
- Windows
- Office 365

### Permissions Required

### Mitigations

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Email Hiding Rules\|T1564.008]] | Email Hiding Rules |
| [[Hidden Users\|T1564.002]] | Hidden Users |
| [[Resource Forking\|T1564.009]] | Resource Forking |
| [[Run Virtual Instance\|T1564.006]] | Run Virtual Instance |
| [[VBA Stomping\|T1564.007]] | VBA Stomping |
| [[Hidden Window\|T1564.003]] | Hidden Window |
| [[Hidden File System\|T1564.005]] | Hidden File System |
| [[Hidden Files and Directories\|T1564.001]] | Hidden Files and Directories |
| [[NTFS File Attributes\|T1564.004]] | NTFS File Attributes |
| [[Process Argument Spoofing\|T1564.010]] | Process Argument Spoofing |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1564
- Sofacy Komplex Trojan: https://researchcenter.paloaltonetworks.com/2016/09/unit42-sofacys-komplex-os-x-trojan/
- Cybereason OSX Pirrit: https://cdn2.hubspot.net/hubfs/3354902/Content%20PDFs/Cybereason-Lab-Analysis-OSX-Pirrit-4-6-16.pdf
- MalwareBytes ADS July 2015: https://blog.malwarebytes.com/101/2015/07/introduction-to-alternate-data-streams/
- Sophos Ragnar May 2020: https://news.sophos.com/en-us/2020/05/21/ragnar-locker-ransomware-deploys-virtual-machine-to-dodge-security/
