---
alias: T1554
---

## T1554

Adversaries may modify client software binaries to establish persistent access to systems. Client software enables users to access services provided by a server. Common client software types are SSH clients, FTP clients, email clients, and web browsers.

Adversaries may make modifications to client software binaries to carry out malicious tasks when those applications are in use. For example, an adversary may copy source code for the client software, add a backdoor, compile for the target, and replace the legitimate application binary (or support files) with the backdoored one. Since these applications may be routinely executed by the user, the adversary can leverage this for persistent access to the host.


### Tactic
- [[Persistence]] (TA0003)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Mitre Att&ck/techniques/Code Signing|M1045]] | Code Signing | Ensure all application component binaries are signed by the correct application developers. |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1554
