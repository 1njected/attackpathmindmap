---
alias: T1565
---

## T1565

Adversaries may insert, delete, or manipulate data in order to influence external outcomes or hide activity, thus threatening the integrity of the data. By manipulating data, adversaries may attempt to affect a business process, organizational understanding, or decision making.

The type of modification and the impact it will have depends on the target application and process as well as the goals and objectives of the adversary. For complex systems, an adversary would likely need special expertise and possibly access to specialized software related to the system that would typically be gained through a prolonged information gathering campaign in order to have the desired impact.


### Tactic
- [[Impact]] (TA0040)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Remote Data Storage\|M1029]] | Remote Data Storage | Consider implementing IT disaster recovery plans that contain procedures for taking regular data backups that can be used to restore organizational data.(Citation: Ready.gov IT DRP) Ensure backups are stored off system and is protected from common methods adversaries may use to gain access and manipulate backups. |
| [[Network Segmentation\|M1030]] | Network Segmentation | Identify critical business and system processes that may be targeted by adversaries and work to isolate and secure those systems against unauthorized access and tampering. |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Ensure least privilege principles are applied to important information resources to reduce exposure to data manipulation risk. |
| [[Encrypt Sensitive Information\|M1041]] | Encrypt Sensitive Information | Consider encrypting important information to reduce an adversary’s ability to perform tailored data modifications. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Stored Data Manipulation\|T1565.001]] | Stored Data Manipulation |
| [[Runtime Data Manipulation\|T1565.003]] | Runtime Data Manipulation |
| [[Transmitted Data Manipulation\|T1565.002]] | Transmitted Data Manipulation |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1565
