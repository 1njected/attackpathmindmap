---
alias: T1563
---

## T1563

Adversaries may take control of preexisting sessions with remote services to move laterally in an environment. Users may use valid credentials to log into a service specifically designed to accept remote connections, such as telnet, SSH, and RDP. When a user logs into a service, a session will be established that will allow them to maintain a continuous interaction with that service.

Adversaries may commandeer these sessions to carry out actions on remote systems. [Remote Service Session Hijacking](https://attack.mitre.org/techniques/T1563) differs from use of [Remote Services](https://attack.mitre.org/techniques/T1021) because it hijacks an existing session rather than creating a new session using [Valid Accounts](https://attack.mitre.org/techniques/T1078).(Citation: RDP Hijacking Medium)(Citation: Breach Post-mortem SSH Hijack)


### Tactic
- [[Lateral Movement]] (TA0008)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required
- SYSTEM
- root

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Network Segmentation\|M1030]] | Network Segmentation | Enable firewall rules to block unnecessary traffic between network security zones within a network. |
| [[User Account Management\|M1018]] | User Account Management | Limit remote user permissions if remote access is necessary. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Do not allow remote access to services as a privileged account unless necessary. |
| [[Disable or Remove Feature or Program\|M1042]] | Disable or Remove Feature or Program | Disable the remote service (ex: SSH, RDP, etc.) if it is unnecessary. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[SSH Hijacking\|T1563.001]] | SSH Hijacking |
| [[RDP Hijacking\|T1563.002]] | RDP Hijacking |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1563
- RDP Hijacking Medium: https://medium.com/@networksecurity/rdp-hijacking-how-to-hijack-rds-and-remoteapp-sessions-transparently-to-move-through-an-da2a1e73a5f6
- Breach Post-mortem SSH Hijack: https://matrix.org/blog/2019/05/08/post-mortem-and-remediations-for-apr-11-security-incident
