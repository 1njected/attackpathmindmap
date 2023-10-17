---
alias: T1071
---

## T1071

Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic. Commands to the remote system, and often the results of those commands, will be embedded within the protocol traffic between the client and server. 

Adversaries may utilize many different protocols, including those used for web browsing, transferring files, electronic mail, or DNS. For connections that occur internally within an enclave (such as those between a proxy or pivot node and other nodes), commonly used protocols are SMB, SSH, or RDP. 


### Tactic
- [[Command and Control]] (TA0011)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Network Intrusion Prevention\|M1031]] | Network Intrusion Prevention | Network intrusion detection and prevention systems that use network signatures to identify traffic for specific adversary malware can be used to mitigate activity at the network level. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[DNS\|T1071.004]] | DNS |
| [[Mail Protocols\|T1071.003]] | Mail Protocols |
| [[File Transfer Protocols\|T1071.002]] | File Transfer Protocols |
| [[Web Protocols\|T1071.001]] | Web Protocols |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1071
- University of Birmingham C2: https://arxiv.org/ftp/arxiv/papers/1408/1408.1136.pdf
