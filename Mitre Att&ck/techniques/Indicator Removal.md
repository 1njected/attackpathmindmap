---
alias: T1070
---

## T1070

Adversaries may delete or modify artifacts generated within systems to remove evidence of their presence or hinder defenses. Various artifacts may be created by an adversary or something that can be attributed to an adversary’s actions. Typically these artifacts are used as defensive indicators related to monitored events, such as strings from downloaded files, logs that are generated from user actions, and other data analyzed by defenders. Location, format, and type of artifact (such as command or login history) are often specific to each platform.

Removal of these indicators may interfere with event collection, reporting, or other processes used to detect intrusion activity. This may compromise the integrity of security solutions by causing notable events to go unreported. This activity may also impede forensic analysis and incident response, due to lack of sufficient data to determine what occurred.


### Tactic
- [[Defense Evasion]] (TA0005)

### Platforms
- Linux
- macOS
- Windows
- Containers
- Network
- Office 365
- Google Workspace

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Remote Data Storage\|M1029]] | Remote Data Storage | Automatically forward events to a log server or data repository to prevent conditions in which the adversary can locate and manipulate data on the local system. When possible, minimize time delay on event reporting to avoid prolonged storage on the local system.  |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities. |
| [[Encrypt Sensitive Information\|M1041]] | Encrypt Sensitive Information | Obfuscate/encrypt event files locally and in transit to avoid giving feedback to an adversary. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Clear Linux or Mac System Logs\|T1070.002]] | Clear Linux or Mac System Logs |
| [[Clear Network Connection History and Configurations\|T1070.007]] | Clear Network Connection History and Configurations |
| [[Clear Command History\|T1070.003]] | Clear Command History |
| [[Clear Mailbox Data\|T1070.008]] | Clear Mailbox Data |
| [[Timestomp\|T1070.006]] | Timestomp |
| [[Clear Windows Event Logs\|T1070.001]] | Clear Windows Event Logs |
| [[Network Share Connection Removal\|T1070.005]] | Network Share Connection Removal |
| [[Clear Persistence\|T1070.009]] | Clear Persistence |
| [[File Deletion\|T1070.004]] | File Deletion |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1070
