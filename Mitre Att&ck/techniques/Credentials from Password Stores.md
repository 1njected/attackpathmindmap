---
alias: T1555
---

## T1555

Adversaries may search for common password storage locations to obtain user credentials. Passwords are stored in several places on a system, depending on the operating system or application holding the credentials. There are also specific applications that store passwords to make it easier for users manage and maintain. Once credentials are obtained, they can be used to perform lateral movement and access restricted information.


### Tactic
- [[Credential Access]] (TA0006)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required
- Administrator

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Password Policies\|M1027]] | Password Policies | The password for the user's login keychain can be changed from the user's login password. This increases the complexity for an adversary because they need to know an additional password.<br /><br />Organizations may consider weighing the risk of storing credentials in password stores and web browsers. If system, software, or web browser credential disclosure is a significant concern, technical controls, policy, and user training may be used to prevent storage of credentials in improper locations. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Securityd Memory\|T1555.002]] | Securityd Memory |
| [[Keychain\|T1555.001]] | Keychain |
| [[Password Managers\|T1555.005]] | Password Managers |
| [[Credentials from Web Browsers\|T1555.003]] | Credentials from Web Browsers |
| [[Windows Credential Manager\|T1555.004]] | Windows Credential Manager |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1555
