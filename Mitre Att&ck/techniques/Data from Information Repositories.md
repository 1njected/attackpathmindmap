---
alias: T1213
---

## T1213

Adversaries may leverage information repositories to mine valuable information. Information repositories are tools that allow for storage of information, typically to facilitate collaboration or information sharing between users, and can store a wide variety of data that may aid adversaries in further objectives, or direct access to the target information. Adversaries may also abuse external sharing features to share sensitive documents with recipients outside of the organization. 

The following is a brief list of example information that may hold potential value to an adversary and may also be found on an information repository:

* Policies, procedures, and standards
* Physical / logical network diagrams
* System architecture diagrams
* Technical system documentation
* Testing / development credentials
* Work / project schedules
* Source code snippets
* Links to network shares and other internal resources

Information stored in a repository may vary based on the specific instance or environment. Specific common information repositories include web-based platforms such as [Sharepoint](https://attack.mitre.org/techniques/T1213/002) and [Confluence](https://attack.mitre.org/techniques/T1213/001), specific services such as Code Repositories, IaaS databases, enterprise databases, and other storage infrastructure such as SQL Server.


### Tactic
- [[Collection]] (TA0009)

### Platforms
- Linux
- Windows
- macOS
- SaaS
- Office 365
- Google Workspace
- IaaS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Develop and publish policies that define acceptable information to be stored in repositories. |
| [[User Account Management\|M1018]] | User Account Management | Enforce the principle of least-privilege. Consider implementing access control mechanisms that include both authentication and authorization. |
| [[Audit\|M1047]] | Audit | Consider periodic review of accounts and privileges for critical and sensitive repositories. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Sharepoint\|T1213.002]] | Sharepoint |
| [[Confluence\|T1213.001]] | Confluence |
| [[Code Repositories\|T1213.003]] | Code Repositories |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1213
- Atlassian Confluence Logging: https://confluence.atlassian.com/confkb/how-to-enable-user-access-logging-182943.html
- Microsoft SharePoint Logging: https://support.office.com/en-us/article/configure-audit-settings-for-a-site-collection-a9920c97-38c0-44f2-8bcb-4cf1e2ae22d2
- Sharepoint Sharing Events: https://docs.microsoft.com/en-us/microsoft-365/compliance/use-sharing-auditing?view=o365-worldwide#sharepoint-sharing-events
