---
alias: T1552
---

## T1552

Adversaries may search compromised systems to find and obtain insecurely stored credentials. These credentials can be stored and/or misplaced in many locations on a system, including plaintext files (e.g. [Bash History](https://attack.mitre.org/techniques/T1552/003)), operating system or application-specific repositories (e.g. [Credentials in Registry](https://attack.mitre.org/techniques/T1552/002)), or other specialized files/artifacts (e.g. [Private Keys](https://attack.mitre.org/techniques/T1552/004)).


### Tactic
- [[Credential Access]] (TA0006)

### Platforms
- Windows
- Azure AD
- Office 365
- SaaS
- IaaS
- Linux
- macOS
- Google Workspace
- Containers
- Network

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Limit Access to Resource Over Network\|M1035]] | Limit Access to Resource Over Network | Limit network access to sensitive services, such as the Instance Metadata API. |
| [[Filter Network Traffic\|M1037]] | Filter Network Traffic | Limit access to the Instance Metadata API. A properly configured Web Application Firewall (WAF) may help prevent external adversaries from exploiting Server-side Request Forgery (SSRF) attacks that allow access to the Cloud Instance Metadata API.(Citation: RedLock Instance Metadata API 2018) |
| [[User Training\|M1017]] | User Training | Ensure that developers and system administrators are aware of the risk associated with having plaintext passwords in software configuration files that may be left on endpoint systems or servers. |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | There are multiple methods of preventing a user's command history from being flushed to their .bash_history file, including use of the following commands:<br /><code>set +o history</code> and <code>set -o history</code> to start logging again;<br /><code>unset HISTFILE</code> being added to a user's .bash_rc file; and<br /><code>ln -s /dev/null ~/.bash_history</code> to write commands to <code>/dev/null</code>instead. |
| [[Password Policies\|M1027]] | Password Policies | Use strong passphrases for private keys to make cracking difficult. Do not store credentials within the Registry. Establish an organizational policy that prohibits password storage in files. |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Restrict file shares to specific directories with access only to necessary users. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | If it is necessary that software must store credentials in the Registry, then ensure the associated accounts have limited permissions so they cannot be abused if obtained by an adversary. |
| [[Audit\|M1047]] | Audit | Preemptively search for files containing passwords or other credentials and take actions to reduce the exposure risk when found. |
| [[Active Directory Configuration\|M1015]] | Active Directory Configuration | Remove vulnerable Group Policy Preferences.(Citation: Microsoft MS14-025) |
| [[Update Software\|M1051]] | Update Software | Apply patch KB2962486 which prevents credentials from being stored in GPPs.(Citation: ADSecurity Finding Passwords in SYSVOL)(Citation: MS14-025) |
| [[Encrypt Sensitive Information\|M1041]] | Encrypt Sensitive Information | When possible, store keys on separate cryptographic hardware instead of on the local system.  |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Cloud Instance Metadata API\|T1552.005]] | Cloud Instance Metadata API |
| [[Credentials in Registry\|T1552.002]] | Credentials in Registry |
| [[Private Keys\|T1552.004]] | Private Keys |
| [[Bash History\|T1552.003]] | Bash History |
| [[Credentials In Files\|T1552.001]] | Credentials In Files |
| [[Group Policy Preferences\|T1552.006]] | Group Policy Preferences |
| [[Chat Messages\|T1552.008]] | Chat Messages |
| [[Container API\|T1552.007]] | Container API |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1552
