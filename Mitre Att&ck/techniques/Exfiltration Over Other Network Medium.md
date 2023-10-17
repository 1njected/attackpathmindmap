---
alias: T1011
---

## T1011

Adversaries may attempt to exfiltrate data over a different network medium than the command and control channel. If the command and control network is a wired Internet connection, the exfiltration may occur, for example, over a WiFi connection, modem, cellular data connection, Bluetooth, or another radio frequency (RF) channel.

Adversaries may choose to do this if they have sufficient access or proximity, and the connection might not be secured or defended as well as the primary Internet-connected channel because it is not routed through the same enterprise network.


### Tactic
- [[Exfiltration]] (TA0010)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Prevent the creation of new network adapters where possible.(Citation: Microsoft GPO Bluetooth FEB 2009)(Citation: TechRepublic Wireless GPO FEB 2009) |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Exfiltration Over Bluetooth\|T1011.001]] | Exfiltration Over Bluetooth |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1011
