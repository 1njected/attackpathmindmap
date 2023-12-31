---
alias: T1547.013
---

## T1547.013

Adversaries may modify XDG autostart entries to execute programs or commands during system boot. Linux desktop environments that are XDG compliant implement functionality for XDG autostart entries. These entries will allow an application to automatically start during the startup of a desktop environment after user logon. By default, XDG autostart entries are stored within the <code>/etc/xdg/autostart</code> or <code>~/.config/autostart</code> directories and have a .desktop file extension.(Citation: Free Desktop Application Autostart Feb 2006)

Within an XDG autostart entry file, the <code>Type</code> key specifies if the entry is an application (type 1), link (type 2) or directory (type 3). The <code>Name</code> key indicates an arbitrary name assigned by the creator and the <code>Exec</code> key indicates the application and command line arguments to execute.(Citation: Free Desktop Entry Keys)

Adversaries may use XDG autostart entries to maintain persistence by executing malicious commands and payloads, such as remote access tools, during the startup of a desktop environment. Commands included in XDG autostart entries with execute after user logon in the context of the currently logged on user. Adversaries may also use [Masquerading](https://attack.mitre.org/techniques/T1036) to make XDG autostart entries look as if they are associated with legitimate programs.


### Tactic
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Linux

### Permissions Required
- User
- root

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Limit Software Installation\|M1033]] | Limit Software Installation | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
| [[User Account Management\|M1018]] | User Account Management | Limit privileges of user accounts so only authorized privileged users can create and modify XDG autostart entries. |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Restrict write access to XDG autostart entries to only select privileged users. |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1547/013
- Free Desktop Application Autostart Feb 2006: https://specifications.freedesktop.org/autostart-spec/autostart-spec-latest.html
- Free Desktop Entry Keys: https://specifications.freedesktop.org/desktop-entry-spec/1.2/ar01s06.html
