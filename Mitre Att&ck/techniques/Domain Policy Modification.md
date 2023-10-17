---
alias: T1484
---

## T1484

Adversaries may modify the configuration settings of a domain to evade defenses and/or escalate privileges in domain environments. Domains provide a centralized means of managing how computer resources (ex: computers, user accounts) can act, and interact with each other, on a network. The policy of the domain also includes configuration settings that may apply between domains in a multi-domain/forest environment. Modifications to domain settings may include altering domain Group Policy Objects (GPOs) or changing trust settings for domains, including federation trusts.

With sufficient permissions, adversaries can modify domain policy settings. Since domain configuration settings control many of the interactions within the Active Directory (AD) environment, there are a great number of potential attacks that can stem from this abuse. Examples of such abuse include modifying GPOs to push a malicious [Scheduled Task](https://attack.mitre.org/techniques/T1053/005) to computers throughout the domain environment(Citation: ADSecurity GPO Persistence 2016)(Citation: Wald0 Guide to GPOs)(Citation: Harmj0y Abusing GPO Permissions) or modifying domain trusts to include an adversary controlled domain where they can control access tokens that will subsequently be accepted by victim domain resources.(Citation: Microsoft - Customer Guidance on Recent Nation-State Cyber Attacks) Adversaries can also change configuration settings within the AD environment to implement a [Rogue Domain Controller](https://attack.mitre.org/techniques/T1207).

Adversaries may temporarily modify domain policy, carry out a malicious action(s), and then revert the change to remove suspicious indicators.


### Tactic
- [[Defense Evasion]] (TA0005)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Windows
- Azure AD

### Permissions Required
- Administrator
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Account Management\|M1018]] | User Account Management | Consider implementing WMI and security filtering to further tailor which users and computers a GPO will apply to.(Citation: Wald0 Guide to GPOs)(Citation: Microsoft WMI Filters)(Citation: Microsoft GPO Security Filtering) |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Use least privilege and protect administrative access to the Domain Controller and Active Directory Federation Services (AD FS) server. Do not create service accounts with administrative privileges. |
| [[Audit\|M1047]] | Audit | Identify and correct GPO permissions abuse opportunities (ex: GPO modification privileges) using auditing tools such as [BloodHound](https://attack.mitre.org/software/S0521) (version 1.5.1 and later)(Citation: GitHub Bloodhound). |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Domain Trust Modification\|T1484.002]] | Domain Trust Modification |
| [[Group Policy Modification\|T1484.001]] | Group Policy Modification |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1484
- ADSecurity GPO Persistence 2016: https://adsecurity.org/?p=2716
- Wald0 Guide to GPOs: https://wald0.com/?p=179
- Harmj0y Abusing GPO Permissions: http://www.harmj0y.net/blog/redteaming/abusing-gpo-permissions/
- Microsoft - Customer Guidance on Recent Nation-State Cyber Attacks: https://msrc-blog.microsoft.com/2020/12/13/customer-guidance-on-recent-nation-state-cyber-attacks/
- Microsoft - Azure Sentinel ADFSDomainTrustMods: https://github.com/Azure/Azure-Sentinel/blob/master/Detections/AuditLogs/ADFSDomainTrustMods.yaml
- Microsoft 365 Defender Solorigate: https://www.microsoft.com/security/blog/2020/12/28/using-microsoft-365-defender-to-coordinate-protection-against-solorigate/
- Sygnia Golden SAML: https://www.sygnia.co/golden-saml-advisory
- CISA SolarWinds Cloud Detection: https://us-cert.cisa.gov/ncas/alerts/aa21-008a
- Microsoft - Update or Repair Federated domain: https://docs.microsoft.com/en-us/office365/troubleshoot/active-directory/update-federated-domain-office-365
