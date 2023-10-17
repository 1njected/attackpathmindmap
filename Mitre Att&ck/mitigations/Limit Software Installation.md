---
alias: M1033
---

## M1033

Block users or groups from installing unapproved software.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Browser Extensions\|T1176]] | Browser Extensions | Only install browser extensions from trusted sources that can be verified. Browser extensions for some browsers can be controlled through Group Policy. Change settings to prevent the browser from installing extensions without sufficient permissions. |
| [[Create or Modify System Process\|T1543]] | Create or Modify System Process | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
| [[XDG Autostart Entries\|T1547.013]] | XDG Autostart Entries | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
| [[Python\|T1059.006]] | Python | Prevent users from installing Python where not required. |
| [[Systemd Service\|T1543.002]] | Systemd Service | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
| [[VNC\|T1021.005]] | VNC | Restrict software installation to user groups that require it. A VNC server must be manually installed by the user or adversary. |
| [[Systemd Service\|T1501]] | Systemd Service | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
