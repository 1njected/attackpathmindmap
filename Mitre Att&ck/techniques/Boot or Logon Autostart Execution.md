---
alias: T1547
---

## T1547

Adversaries may configure system settings to automatically execute a program during system boot or logon to maintain persistence or gain higher-level privileges on compromised systems. Operating systems may have mechanisms for automatically running a program on system boot or account logon.(Citation: Microsoft Run Key)(Citation: MSDN Authentication Packages)(Citation: Microsoft TimeProvider)(Citation: Cylance Reg Persistence Sept 2013)(Citation: Linux Kernel Programming) These mechanisms may include automatically executing programs that are placed in specially designated directories or are referenced by repositories that store configuration information, such as the Windows Registry. An adversary may achieve the same goal by modifying or extending features of the kernel.

Since some boot or logon autostart programs run with higher privileges, an adversary may leverage these to elevate privileges.


### Tactic
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required
- User
- Administrator
- root

### Mitigations

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Active Setup\|T1547.014]] | Active Setup |
| [[Print Processors\|T1547.012]] | Print Processors |
| [[Port Monitors\|T1547.010]] | Port Monitors |
| [[Shortcut Modification\|T1547.009]] | Shortcut Modification |
| [[Security Support Provider\|T1547.005]] | Security Support Provider |
| [[Time Providers\|T1547.003]] | Time Providers |
| [[Plist Modification\|T1547.011]] | Plist Modification |
| [[Winlogon Helper DLL\|T1547.004]] | Winlogon Helper DLL |
| [[Login Items\|T1547.015]] | Login Items |
| [[Registry Run Keys ／ Startup Folder\|T1547.001]] | Registry Run Keys ／ Startup Folder |
| [[Kernel Modules and Extensions\|T1547.006]] | Kernel Modules and Extensions |
| [[Authentication Package\|T1547.002]] | Authentication Package |
| [[XDG Autostart Entries\|T1547.013]] | XDG Autostart Entries |
| [[Re-opened Applications\|T1547.007]] | Re-opened Applications |
| [[LSASS Driver\|T1547.008]] | LSASS Driver |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1547
- Cylance Reg Persistence Sept 2013: https://blog.cylance.com/windows-registry-persistence-part-2-the-run-keys-and-search-order
- MSDN Authentication Packages: https://msdn.microsoft.com/library/windows/desktop/aa374733.aspx
- Microsoft Run Key: http://msdn.microsoft.com/en-us/library/aa376977
- Microsoft TimeProvider: https://msdn.microsoft.com/library/windows/desktop/ms725475.aspx
- Linux Kernel Programming: https://www.tldp.org/LDP/lkmpg/2.4/lkmpg.pdf
- TechNet Autoruns: https://technet.microsoft.com/en-us/sysinternals/bb963902
