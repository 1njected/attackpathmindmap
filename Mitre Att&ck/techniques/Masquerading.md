---
alias: T1036
---

## T1036

Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools. Masquerading occurs when the name or location of an object, legitimate or malicious, is manipulated or abused for the sake of evading defenses and observation. This may include manipulating file metadata, tricking users into misidentifying the file type, and giving legitimate task or service names.

Renaming abusable system utilities to evade security monitoring is also a form of [Masquerading](https://attack.mitre.org/techniques/T1036).(Citation: LOLBAS Main Site)


### Tactic
- [[Defense Evasion]] (TA0005)

### Platforms
- Linux
- macOS
- Windows
- Containers

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Execution Prevention\|M1038]] | Execution Prevention | Use tools that restrict program execution via application control by attributes other than file name for common operating system utilities that are needed. |
| [[Mitre Att&ck/techniques/Code Signing|M1045]] | Code Signing | Require signed binaries. |
| [[Behavior Prevention on Endpoint\|M1040]] | Behavior Prevention on Endpoint | Implement security controls on the endpoint, such as a Host Intrusion Prevention System (HIPS), to identify and prevent execution of potentially malicious files (such as those with mismatching file signatures). |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Use file system access controls to protect folders such as C:\\Windows\\System32. |
| [[Antivirus／Antimalware\|M1049]] | Antivirus／Antimalware | Anti-virus can be used to automatically quarantine suspicious files. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Double File Extension\|T1036.007]] | Double File Extension |
| [[Match Legitimate Name or Location\|T1036.005]] | Match Legitimate Name or Location |
| [[Masquerade File Type\|T1036.008]] | Masquerade File Type |
| [[Right-to-Left Override\|T1036.002]] | Right-to-Left Override |
| [[Masquerade Task or Service\|T1036.004]] | Masquerade Task or Service |
| [[Invalid Code Signature\|T1036.001]] | Invalid Code Signature |
| [[Rename System Utilities\|T1036.003]] | Rename System Utilities |
| [[Space after Filename\|T1036.006]] | Space after Filename |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1036
- Twitter ItsReallyNick Masquerading Update: https://twitter.com/ItsReallyNick/status/1055321652777619457
- Elastic Masquerade Ball: http://pages.endgame.com/rs/627-YBU-612/images/EndgameJournal_The%20Masquerade%20Ball_Pages_R2.pdf
- LOLBAS Main Site: https://lolbas-project.github.io/
