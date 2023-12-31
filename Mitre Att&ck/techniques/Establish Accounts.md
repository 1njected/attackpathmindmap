---
alias: T1585
---

## T1585

Adversaries may create and cultivate accounts with services that can be used during targeting. Adversaries can create accounts that can be used to build a persona to further operations. Persona development consists of the development of public information, presence, history and appropriate affiliations. This development could be applied to social media, website, or other publicly available information that could be referenced and scrutinized for legitimacy over the course of an operation using that persona or identity.(Citation: NEWSCASTER2014)(Citation: BlackHatRobinSage)

For operations incorporating social engineering, the utilization of an online persona may be important. These personas may be fictitious or impersonate real people. The persona may exist on a single site or across multiple sites (ex: Facebook, LinkedIn, Twitter, Google, GitHub, Docker Hub, etc.). Establishing a persona may require development of additional documentation to make them seem real. This could include filling out profile information, developing social networks, or incorporating photos.(Citation: NEWSCASTER2014)(Citation: BlackHatRobinSage)

Establishing accounts can also include the creation of accounts with email providers, which may be directly leveraged for [Phishing for Information](https://attack.mitre.org/techniques/T1598) or [Phishing](https://attack.mitre.org/techniques/T1566).(Citation: Mandiant APT1)


### Tactic
- [[Resource Development]] (TA0042)

### Platforms
- PRE

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Pre-compromise\|M1056]] | Pre-compromise | This technique cannot be easily mitigated with preventive controls since it is based on behaviors performed outside of the scope of enterprise defenses and controls. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Email Accounts\|T1585.002]] | Email Accounts |
| [[Cloud Accounts\|T1585.003]] | Cloud Accounts |
| [[Social Media Accounts\|T1585.001]] | Social Media Accounts |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1585
- NEWSCASTER2014: https://www.securityweek.com/iranian-hackers-targeted-us-officials-elaborate-social-media-attack-operation
- BlackHatRobinSage: http://media.blackhat.com/bh-us-10/whitepapers/Ryan/BlackHat-USA-2010-Ryan-Getting-In-Bed-With-Robin-Sage-v1.0.pdf
- Mandiant APT1: https://www.fireeye.com/content/dam/fireeye-www/services/pdfs/mandiant-apt1-report.pdf
