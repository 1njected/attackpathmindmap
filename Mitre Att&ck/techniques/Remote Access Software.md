---
alias: T1219
---

## T1219

An adversary may use legitimate desktop support and remote access software, such as Team Viewer, AnyDesk, Go2Assist, LogMein, AmmyyAdmin, etc, to establish an interactive command and control channel to target systems within networks. These services are commonly used as legitimate technical support software, and may be allowed by application control within a target environment. Remote access tools like VNC, Ammyy, and Teamviewer are used frequently when compared with other legitimate software commonly used by adversaries.(Citation: Symantec Living off the Land)

Remote access tools may be installed and used post-compromise as alternate communications channel for redundant access or as a way to establish an interactive remote desktop session with the target system. They may also be used as a component of malware to establish a reverse connection or back-connect to a service or adversary controlled system. Installation of many remote access tools may also include persistence (ex: the tool's installation routine creates a [Windows Service](https://attack.mitre.org/techniques/T1543/003)).

Admin tools such as TeamViewer have been used by several groups targeting institutions in countries of interest to the Russian state and criminal campaigns.(Citation: CrowdStrike 2015 Global Threat Report)(Citation: CrySyS Blog TeamSpy)


### Tactic
- [[Command and Control]] (TA0011)

### Platforms
- Linux
- Windows
- macOS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Network Intrusion Prevention\|M1031]] | Network Intrusion Prevention | Network intrusion detection and prevention systems that use network signatures may be able to prevent traffic to remote access services. |
| [[Filter Network Traffic\|M1037]] | Filter Network Traffic | Properly configure firewalls, application firewalls, and proxies to limit outgoing traffic to sites and services used by remote access tools. |
| [[Execution Prevention\|M1038]] | Execution Prevention | Use application control to mitigate installation and use of unapproved software that can be used for remote access. |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1219
- CrowdStrike 2015 Global Threat Report: https://go.crowdstrike.com/rs/281-OBQ-266/images/15GlobalThreatReport.pdf
- CrySyS Blog TeamSpy: https://blog.crysys.hu/2013/03/teamspy/
- Symantec Living off the Land: https://www.symantec.com/content/dam/symantec/docs/security-center/white-papers/istr-living-off-the-land-and-fileless-attack-techniques-en.pdf
