---
alias: T1218
---

## T1218

Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries. Binaries used in this technique are often Microsoft-signed files, indicating that they have been either downloaded from Microsoft or are already native in the operating system.(Citation: LOLBAS Project) Binaries signed with trusted digital certificates can typically execute on Windows systems protected by digital signature validation. Several Microsoft signed binaries that are default on Windows installations can be used to proxy execution of other files or commands.

Similarly, on Linux systems adversaries may abuse trusted binaries such as <code>split</code> to proxy execution of malicious commands.(Citation: split man page)(Citation: GTFO split)


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
| [[Execution Prevention\|M1038]] | Execution Prevention | Consider using application control to prevent execution of binaries that are susceptible to abuse and not required for a given system or network. |
| [[Execution Prevention\|M1038]] | Execution Prevention | Certain signed binaries that can be used to execute other programs may not be necessary within a given environment. Use application whitelisting configured to block execution of these binaries if they are not required for a given system or network to prevent potential misuse by adversaries. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Restrict execution of particularly vulnerable binaries to privileged accounts or groups that need to use it to lessen the opportunities for malicious usage. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | If these binaries are required for use, then restrict execution of them to privileged accounts or groups that need to use them to lessen the opportunities for malicious use. |
| [[Exploit Protection\|M1050]] | Exploit Protection | Microsoft's Enhanced Mitigation Experience Toolkit (EMET) Attack Surface Reduction (ASR) feature can be used to block methods of using using trusted binaries to bypass application control. |
| [[Disable or Remove Feature or Program\|M1042]] | Disable or Remove Feature or Program | Many native binaries may not be necessary within a given environment. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Rundll32\|T1218.011]] | Rundll32 |
| [[Mavinject\|T1218.013]] | Mavinject |
| [[InstallUtil\|T1218.004]] | InstallUtil |
| [[Msiexec\|T1218.007]] | Msiexec |
| [[CMSTP\|T1218.003]] | CMSTP |
| [[Control Panel\|T1218.002]] | Control Panel |
| [[Odbcconf\|T1218.008]] | Odbcconf |
| [[Verclsid\|T1218.012]] | Verclsid |
| [[Mshta\|T1218.005]] | Mshta |
| [[Compiled HTML File\|T1218.001]] | Compiled HTML File |
| [[Regsvr32\|T1218.010]] | Regsvr32 |
| [[Regsvcs／Regasm\|T1218.009]] | Regsvcs／Regasm |
| [[MMC\|T1218.014]] | MMC |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1218
- GTFO split: https://gtfobins.github.io/gtfobins/split/
- LOLBAS Project: https://github.com/LOLBAS-Project/LOLBAS#criteria
- split man page: https://man7.org/linux/man-pages/man1/split.1.html
