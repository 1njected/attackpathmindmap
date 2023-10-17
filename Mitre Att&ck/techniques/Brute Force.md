---
alias: T1110
---

## T1110

Adversaries may use brute force techniques to gain access to accounts when passwords are unknown or when password hashes are obtained. Without knowledge of the password for an account or set of accounts, an adversary may systematically guess the password using a repetitive or iterative mechanism. Brute forcing passwords can take place via interaction with a service that will check the validity of those credentials or offline against previously acquired credential data, such as password hashes.

Brute forcing credentials may take place at various points during a breach. For example, adversaries may attempt to brute force access to [Valid Accounts](https://attack.mitre.org/techniques/T1078) within a victim environment leveraging knowledge gathered from other post-compromise behaviors such as [OS Credential Dumping](https://attack.mitre.org/techniques/T1003), [Account Discovery](https://attack.mitre.org/techniques/T1087), or [Password Policy Discovery](https://attack.mitre.org/techniques/T1201). Adversaries may also combine brute forcing activity with behaviors such as [External Remote Services](https://attack.mitre.org/techniques/T1133) as part of Initial Access.


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
| [[Password Policies\|M1027]] | Password Policies | Refer to NIST guidelines when creating password policies.(Citation: NIST 800-63-3) |
| [[User Account Management\|M1018]] | User Account Management | Proactively reset accounts that are known to be part of breached credentials either immediately, or after detecting bruteforce attempts. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Account Use Policies\|M1036]] | Account Use Policies | Set account lockout policies after a certain number of failed login attempts to prevent passwords from being guessed. Too strict a policy may create a denial of service condition and render environments un-usable, with all accounts used in the brute force being locked-out. Use conditional access policies to block logins from non-compliant devices or from outside defined organization IP ranges.(Citation: Microsoft Common Conditional Access Policies) |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Password Guessing\|T1110.001]] | Password Guessing |
| [[Password Cracking\|T1110.002]] | Password Cracking |
| [[Password Spraying\|T1110.003]] | Password Spraying |
| [[Credential Stuffing\|T1110.004]] | Credential Stuffing |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1110
