---
alias: T1539
---

## T1539

An adversary may steal web application or service session cookies and use them to gain access to web applications or Internet services as an authenticated user without needing credentials. Web applications and services often use session cookies as an authentication token after a user has authenticated to a website.

Cookies are often valid for an extended period of time, even if the web application is not actively used. Cookies can be found on disk, in the process memory of the browser, and in network traffic to remote systems. Additionally, other applications on the targets machine might store sensitive authentication cookies in memory (e.g. apps which authenticate to cloud services). Session cookies can be used to bypasses some multi-factor authentication protocols.(Citation: Pass The Cookie)

There are several examples of malware targeting cookies from web browsers on the local system.(Citation: Kaspersky TajMahal April 2019)(Citation: Unit 42 Mac Crypto Cookies January 2019) There are also open source frameworks such as Evilginx 2 and Muraena that can gather session cookies through a malicious proxy (ex: [Adversary-in-the-Middle](https://attack.mitre.org/techniques/T1557)) that can be set up by an adversary and used in phishing campaigns.(Citation: Github evilginx2)(Citation: GitHub Mauraena)

After an adversary acquires a valid cookie, they can then perform a [Web Session Cookie](https://attack.mitre.org/techniques/T1550/004) technique to login to the corresponding web application.


### Tactic
- [[Credential Access]] (TA0006)

### Platforms
- Linux
- macOS
- Windows
- Office 365
- SaaS
- Google Workspace

### Permissions Required
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Train users to identify aspects of phishing attempts where they're asked to enter credentials into a site that has the incorrect domain for the application they are logging into. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | A physical second factor key that uses the target login domain as part of the negotiation protocol will prevent session cookie theft through proxy methods.(Citation: Evilginx 2 July 2018) |
| [[Software Configuration\|M1054]] | Software Configuration | Configure browsers or tasks to regularly delete persistent cookies. |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1539
- Pass The Cookie: https://wunderwuzzi23.github.io/blog/passthecookie.html
- Kaspersky TajMahal April 2019: https://securelist.com/project-tajmahal/90240/
- Unit 42 Mac Crypto Cookies January 2019: https://unit42.paloaltonetworks.com/mac-malware-steals-cryptocurrency-exchanges-cookies/
- Github evilginx2: https://github.com/kgretzky/evilginx2
- GitHub Mauraena: https://github.com/muraenateam/muraena
