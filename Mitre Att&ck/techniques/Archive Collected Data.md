---
alias: T1560
---

## T1560

An adversary may compress and/or encrypt data that is collected prior to exfiltration. Compressing the data can help to obfuscate the collected data and minimize the amount of data sent over the network. Encryption can be used to hide information that is being exfiltrated from detection or make exfiltration less conspicuous upon inspection by a defender.

Both compression and encryption are done prior to exfiltration, and can be performed using a utility, 3rd party library, or custom method.


### Tactic
- [[Collection]] (TA0009)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Audit\|M1047]] | Audit | System scans can be performed to identify unauthorized archival utilities. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Archive via Utility\|T1560.001]] | Archive via Utility |
| [[Archive via Custom Method\|T1560.003]] | Archive via Custom Method |
| [[Archive via Library\|T1560.002]] | Archive via Library |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1560
- Wikipedia File Header Signatures: https://en.wikipedia.org/wiki/List_of_file_signatures
