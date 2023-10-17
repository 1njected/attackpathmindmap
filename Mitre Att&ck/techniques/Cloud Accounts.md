---
alias: T1078.004
---

## T1078.004

Adversaries may obtain and abuse credentials of a cloud account as a means of gaining Initial Access, Persistence, Privilege Escalation, or Defense Evasion. Cloud accounts are those created and configured by an organization for use by users, remote support, services, or for administration of resources within a cloud service provider or SaaS application. In some cases, cloud accounts may be federated with traditional identity management systems, such as Windows Active Directory.(Citation: AWS Identity Federation)(Citation: Google Federating GC)(Citation: Microsoft Deploying AD Federation)

Compromised credentials for cloud accounts can be used to harvest sensitive data from online storage accounts and databases. Access to cloud accounts can also be abused to gain Initial Access to a network by abusing a [Trusted Relationship](https://attack.mitre.org/techniques/T1199). Similar to [Domain Accounts](https://attack.mitre.org/techniques/T1078/002), compromise of federated cloud accounts may allow adversaries to more easily move laterally within an environment.

Once a cloud account is compromised, an adversary may perform [Account Manipulation](https://attack.mitre.org/techniques/T1098) - for example, by adding [Additional Cloud Roles](https://attack.mitre.org/techniques/T1098/003) - to maintain persistence and potentially escalate their privileges.


### Tactic
- [[Defense Evasion]] (TA0005)
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)
- [[Initial Access]] (TA0001)

### Platforms
- Azure AD
- Office 365
- SaaS
- IaaS
- Google Workspace

### Permissions Required
- User
- Administrator

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Applications may send push notifications to verify a login as a form of multi-factor authentication (MFA). Train users to only accept valid push notifications and to report suspicious push notifications. |
| [[Password Policies\|M1027]] | Password Policies | Ensure that cloud accounts, particularly privileged accounts, have complex, unique passwords across all systems on the network. Passwords and access keys should be rotated regularly. This limits the amount of time credentials can be used to access resources if a credential is compromised without your knowledge. Cloud service providers may track access key age to help audit and identify keys that may need to be rotated.(Citation: AWS - IAM Console Best Practices) |
| [[User Account Management\|M1018]] | User Account Management | Periodically review user accounts and remove those that are inactive or unnecessary. Limit the ability for user accounts to create additional accounts. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Review privileged cloud account permission levels routinely to look for those that could allow an adversary to gain wide access, such as Global Administrator and Privileged Role Administrator in Azure AD.(Citation: TechNet Credential Theft)(Citation: TechNet Least Privilege)(Citation: Microsoft Azure security baseline for Azure Active Directory) These reviews should also check if new privileged cloud accounts have been created that were not authorized. For example, in Azure AD environments configure alerts to notify when accounts have gone many days without using privileged roles, as these roles may be able to be removed.(Citation: Microsoft Security Alerts for Azure AD Roles) Consider using temporary, just-in-time (JIT) privileged access to Azure AD resources rather than permanently assigning privileged roles.(Citation: Microsoft Azure security baseline for Azure Active Directory) |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use multi-factor authentication for cloud accounts, especially privileged accounts. This can be implemented in a variety of forms (e.g. hardware, virtual, SMS), and can also be audited using administrative reporting features.(Citation: AWS - IAM Console Best Practices) |
| [[Active Directory Configuration\|M1015]] | Active Directory Configuration | Disable legacy authentication, which does not support MFA, and require the use of modern authentication protocols instead.  |
| [[Account Use Policies\|M1036]] | Account Use Policies | Use conditional access policies to block logins from non-compliant devices or from outside defined organization IP ranges.(Citation: Microsoft Common Conditional Access Policies) |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1078/004
- AWS Identity Federation: https://aws.amazon.com/identity/federation/
- Google Federating GC: https://cloud.google.com/solutions/federating-gcp-with-active-directory-introduction
- Microsoft Deploying AD Federation: https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/how-to-connect-fed-azure-adfs
