---
alias: T1114
---

## T1114

Adversaries may target user email to collect sensitive information. Emails may contain sensitive data, including trade secrets or personal information, that can prove valuable to adversaries. Adversaries can collect or forward email from mail servers or clients. 


### Tactic
- [[Collection]] (TA0009)

### Platforms
- Windows
- Office 365
- Google Workspace
- macOS
- Linux

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use of multi-factor authentication for public-facing webmail servers is a recommended best practice to minimize the usefulness of usernames and passwords to adversaries. |
| [[Audit\|M1047]] | Audit | Enterprise email solutions have monitoring mechanisms that may include the ability to audit auto-forwarding rules on a regular basis.<br /><br />In an Exchange environment, Administrators can use Get-InboxRule to discover and remove potentially malicious auto-forwarding rules.(Citation: Microsoft Tim McMichael Exchange Mail Forwarding 2)  |
| [[Encrypt Sensitive Information\|M1041]] | Encrypt Sensitive Information | Use of encryption provides an added layer of security to sensitive information sent over email. Encryption using public key cryptography requires the adversary to obtain the private certificate along with an encryption key to decrypt messages. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Local Email Collection\|T1114.001]] | Local Email Collection |
| [[Email Forwarding Rule\|T1114.003]] | Email Forwarding Rule |
| [[Remote Email Collection\|T1114.002]] | Remote Email Collection |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1114
- Microsoft Tim McMichael Exchange Mail Forwarding 2: https://blogs.technet.microsoft.com/timmcmic/2015/06/08/exchange-and-office-365-mail-forwarding-2/
