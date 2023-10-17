---
alias: T1136.003
---

## T1136.003

Adversaries may create a cloud account to maintain access to victim systems. With a sufficient level of access, such accounts may be used to establish secondary credentialed access that does not require persistent remote access tools to be deployed on the system.(Citation: Microsoft O365 Admin Roles)(Citation: Microsoft Support O365 Add Another Admin, October 2019)(Citation: AWS Create IAM User)(Citation: GCP Create Cloud Identity Users)(Citation: Microsoft Azure AD Users)

Adversaries may create accounts that only have access to specific cloud services, which can reduce the chance of detection.

Once an adversary has created a cloud account, they can then manipulate that account to ensure persistence and allow access to additional resources - for example, by adding [Additional Cloud Credentials](https://attack.mitre.org/techniques/T1098/001) or assigning [Additional Cloud Roles](https://attack.mitre.org/techniques/T1098/003).


### Tactic
- [[Persistence]] (TA0003)

### Platforms
- Azure AD
- Office 365
- IaaS
- Google Workspace
- SaaS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Network Segmentation\|M1030]] | Network Segmentation | Configure access controls and firewalls to limit access to critical systems and domain controllers. Most cloud environments support separate virtual private cloud (VPC) instances that enable further segmentation of cloud systems. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Do not allow privileged accounts to be used for day-to-day operations that may expose them to potential adversaries on unprivileged systems. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Use multi-factor authentication for user and privileged accounts. |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1136/003
- Microsoft O365 Admin Roles: https://docs.microsoft.com/en-us/office365/admin/add-users/about-admin-roles?view=o365-worldwide
- AWS Create IAM User: https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html
- GCP Create Cloud Identity Users: https://support.google.com/cloudidentity/answer/7332836?hl=en&ref_topic=7558554
- Microsoft Azure AD Users: https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-users-azure-active-directory
- Microsoft Support O365 Add Another Admin, October 2019: https://support.office.com/en-us/article/add-another-admin-f693489f-9f55-4bd0-a637-a81ce93de22d
