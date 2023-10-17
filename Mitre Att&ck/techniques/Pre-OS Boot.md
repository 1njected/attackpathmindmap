---
alias: T1542
---

## T1542

Adversaries may abuse Pre-OS Boot mechanisms as a way to establish persistence on a system. During the booting process of a computer, firmware and various startup services are loaded before the operating system. These programs control flow of execution before the operating system takes control.(Citation: Wikipedia Booting)

Adversaries may overwrite data in boot drivers or firmware such as BIOS (Basic Input/Output System) and The Unified Extensible Firmware Interface (UEFI) to persist on systems at a layer below the operating system. This can be particularly difficult to detect as malware at this level will not be detected by host software-based defenses.


### Tactic
- [[Defense Evasion]] (TA0005)
- [[Persistence]] (TA0003)

### Platforms
- Linux
- Windows
- Network
- macOS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Boot Integrity\|M1046]] | Boot Integrity | Use Trusted Platform Module technology and a secure or trusted boot process to prevent system integrity from being compromised. Check the integrity of the existing BIOS or EFI to determine if it is vulnerable to modification. (Citation: TCG Trusted Platform Module) (Citation: TechNet Secure Boot Process) |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Ensure proper permissions are in place to help prevent adversary access to privileged accounts necessary to perform these actions |
| [[Update Software\|M1051]] | Update Software | Patch the BIOS and EFI as necessary. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[System Firmware\|T1542.001]] | System Firmware |
| [[Bootkit\|T1542.003]] | Bootkit |
| [[TFTP Boot\|T1542.005]] | TFTP Boot |
| [[Component Firmware\|T1542.002]] | Component Firmware |
| [[ROMMONkit\|T1542.004]] | ROMMONkit |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1542
- ITWorld Hard Disk Health Dec 2014: https://www.itworld.com/article/2853992/3-tools-to-check-your-hard-drives-health-and-make-sure-its-not-already-dying-on-you.html
- Wikipedia Booting: https://en.wikipedia.org/wiki/Booting
