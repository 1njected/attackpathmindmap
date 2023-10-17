---
alias: T1213.001
---

## T1213.001


Adversaries may leverage Confluence repositories to mine valuable information. Often found in development environments alongside Atlassian JIRA, Confluence is generally used to store development-related documentation, however, in general may contain more diverse categories of useful information, such as:

* Policies, procedures, and standards
* Physical / logical network diagrams
* System architecture diagrams
* Technical system documentation
* Testing / development credentials
* Work / project schedules
* Source code snippets
* Links to network shares and other internal resources



### Tactic
- [[Collection]] (TA0009)

### Platforms
- SaaS

### Permissions Required
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Develop and publish policies that define acceptable information to be stored in Confluence repositories. |
| [[User Account Management\|M1018]] | User Account Management | Enforce the principle of least-privilege. Consider implementing access control mechanisms that include both authentication and authorization. |
| [[Audit\|M1047]] | Audit | Consider periodic review of accounts and privileges for critical and sensitive Confluence repositories. |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1213/001
- Atlassian Confluence Logging: https://confluence.atlassian.com/confkb/how-to-enable-user-access-logging-182943.html
