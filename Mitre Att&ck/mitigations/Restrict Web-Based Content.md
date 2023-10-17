---
alias: M1021
---

## M1021

Restrict use of certain websites, block downloads/attachments, block Javascript, restrict browser extensions, etc.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Bidirectional Communication\|T1102.002]] | Bidirectional Communication | Web proxies can be used to enforce external network communication policy that prevents use of unauthorized external services. |
| [[Spearphishing Link\|T1566.002]] | Spearphishing Link | Determine if certain websites that can be used for spearphishing are necessary for business operations and consider blocking access if activity cannot be monitored well or if it poses a significant risk. |
| [[Steal Application Access Token\|T1528]] | Steal Application Access Token | Administrators can block end-user consent to OAuth applications, disabling users from authorizing third-party apps through OAuth 2.0 and forcing administrative consent for all requests. They can also block end-user registration of applications by their users, to reduce risk. A Cloud Access Security Broker can also be used to ban applications.<br /><br />Azure offers a couple of enterprise policy settings in the Azure Management Portal that may help:<br /><br />"Users -> User settings -> App registrations: Users can register applications" can be set to "no" to prevent users from registering new applications. <br />"Enterprise applications -> User settings -> Enterprise applications: Users can consent to apps accessing company data on their behalf" can be set to "no" to prevent users from consenting to allow third-party multi-tenant applications |
| [[Compiled HTML File\|T1218.001]] | Compiled HTML File | Consider blocking download/transfer and execution of potentially uncommon file types known to be used in adversary campaigns, such as CHM files |
| [[Dynamic Resolution\|T1568]] | Dynamic Resolution | In some cases a local DNS sinkhole may be used to help prevent behaviors associated with dynamic resolution. |
| [[Dead Drop Resolver\|T1102.001]] | Dead Drop Resolver | Web proxies can be used to enforce external network communication policy that prevents use of unauthorized external services. |
| [[User Execution\|T1204]] | User Execution | If a link is being visited by a user, block unknown or unused files in transit by default that should not be downloaded or by policy from suspicious sites as a best practice to prevent some vectors, such as .scr, .exe, .pif, .cpl, etc. Some download scanning devices can open and analyze compressed and encrypted formats, such as zip and rar that may be used to conceal malicious files. |
| [[Drive-by Compromise\|T1189]] | Drive-by Compromise | For malicious code served up through ads, adblockers can help prevent that code from executing in the first place.<br /><br />Script blocking extensions can help prevent the execution of JavaScript that may commonly be used during the exploitation process. |
| [[Spearphishing via Service\|T1566.003]] | Spearphishing via Service | Determine if certain social media sites, personal webmail services, or other service that can be used for spearphishing is necessary for business operations and consider blocking access if activity cannot be monitored well or if it poses a significant risk. |
| [[Exfiltration Over Web Service\|T1567]] | Exfiltration Over Web Service | Web proxies can be used to enforce an external network communication policy that prevents use of unauthorized external services. |
| [[Domain Generation Algorithms\|T1568.002]] | Domain Generation Algorithms | In some cases a local DNS sinkhole may be used to help prevent DGA-based command and control at a reduced cost. |
| [[Application Access Token\|T1550.001]] | Application Access Token | Update corporate policies to restrict what types of third-party applications may be added to any online service or tool that is linked to the company's information, accounts or network (e.g., Google, Microsoft, Dropbox, Basecamp, GitHub). However, rather than providing high-level guidance on this, be extremely specific—include a list of per-approved applications and deny all others not on the list. Administrators may also block end-user consent through administrative portals, such as the Azure Portal, disabling users from authorizing third-party apps through OAuth and forcing administrative consent.(Citation: Microsoft Azure AD Admin Consent) |
| [[Web Service\|T1102]] | Web Service | Web proxies can be used to enforce external network communication policy that prevents use of unauthorized external services. |
| [[Phishing\|T1566]] | Phishing | Determine if certain websites or attachment types (ex: .scr, .exe, .pif, .cpl, etc.) that can be used for phishing are necessary for business operations and consider blocking access if activity cannot be monitored well or if it poses a significant risk. |
| [[Visual Basic\|T1059.005]] | Visual Basic | Script blocking extensions can help prevent the execution of scripts and HTA files that may commonly be used during the exploitation process. For malicious code served up through ads, adblockers can help prevent that code from executing in the first place. |
| [[One-Way Communication\|T1102.003]] | One-Way Communication | Web proxies can be used to enforce external network communication policy that prevents use of unauthorized external services. |
| [[JavaScript\|T1059.007]] | JavaScript | Script blocking extensions can help prevent the execution of JavaScript and HTA files that may commonly be used during the exploitation process. For malicious code served up through ads, adblockers can help prevent that code from executing in the first place. |
| [[Exfiltration to Cloud Storage\|T1567.002]] | Exfiltration to Cloud Storage | Web proxies can be used to enforce an external network communication policy that prevents use of unauthorized external services. |
| [[Command and Scripting Interpreter\|T1059]] | Command and Scripting Interpreter | Script blocking extensions can help prevent the execution of scripts and HTA files that may commonly be used during the exploitation process. For malicious code served up through ads, adblockers can help prevent that code from executing in the first place. |
| [[Exfiltration to Code Repository\|T1567.001]] | Exfiltration to Code Repository | Web proxies can be used to enforce an external network communication policy that prevents use of unauthorized external services. |
| [[Exfiltration to Text Storage Sites\|T1567.003]] | Exfiltration to Text Storage Sites | Web proxies can be used to enforce an external network communication policy that prevents use of unauthorized external services. |
| [[Malicious Link\|T1204.001]] | Malicious Link | If a link is being visited by a user, block unknown or unused files in transit by default that should not be downloaded or by policy from suspicious sites as a best practice to prevent some vectors, such as .scr, .exe, .pif, .cpl, etc. Some download scanning devices can open and analyze compressed and encrypted formats, such as zip and rar that may be used to conceal malicious files. |
| [[Spearphishing Attachment\|T1566.001]] | Spearphishing Attachment | Block unknown or unused attachments by default that should not be transmitted over email as a best practice to prevent some vectors, such as .scr, .exe, .pif, .cpl, etc. Some email scanning devices can open and analyze compressed and encrypted formats, such as zip and rar that may be used to conceal malicious attachments. |
| [[Application Access Token\|T1527]] | Application Access Token | Update corporate policies to restrict what types of third-party applications may be added to any online service or tool that is linked to the company's information, accounts or network (example: Google, Microsoft, Dropbox, Basecamp, GitHub). However, rather than providing high-level guidance on this, be extremely specific—include a list of pre-approved applications and deny all others not on the list. Administrators may also block end-user consent through administrative portals, such as the Azure Portal, disabling users from authorizing third-party apps through OAuth and forcing administrative consent.(Citation: Microsoft Azure AD Admin Consent) |
| [[Compiled HTML File\|T1223]] | Compiled HTML File | Consider blocking download/transfer and execution of potentially uncommon file types known to be used in adversary campaigns, such as CHM files. |
| [[Spearphishing Link\|T1192]] | Spearphishing Link | Determine if certain websites that can be used for spearphishing are necessary for business operations and consider blocking access if activity cannot be monitored well or if it poses a significant risk. |
| [[Domain Generation Algorithms\|T1483]] | Domain Generation Algorithms | In some cases a local DNS sinkhole may be used to help prevent DGA-based command and control at a reduced cost. |
| [[Spearphishing Attachment\|T1193]] | Spearphishing Attachment | Block unknown or unused attachments by default that should not be transmitted over email as a best practice to prevent some vectors, such as .scr, .exe, .pif, .cpl, etc. Some email scanning devices can open and analyze compressed and encrypted formats, such as zip and rar that may be used to conceal malicious attachments in [Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027). |
| [[Spearphishing via Service\|T1194]] | Spearphishing via Service | Determine if certain social media sites, personal webmail services, or other service that can be used for spearphishing is necessary for business operations and consider blocking access if activity cannot be monitored well or if it poses a significant risk. |