---
alias: M1032
---

## M1032

Use two or more pieces of evidence to authenticate to a system; such as username and password in addition to a token from a physical smart card or token generator.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Additional Cloud Credentials\|T1098.001]] | Additional Cloud Credentials | Use multi-factor authentication for user and privileged accounts. Consider enforcing multi-factor authentication for the <code>CreateKeyPair</code> and <code>ImportKeyPair</code> API calls through IAM policies.(Citation: Expel IO Evil in AWS) |
| [[Network Sniffing\|T1040]] | Network Sniffing | Use multi-factor authentication wherever possible. |
| [[Local Account\|T1136.001]] | Local Account | Use multi-factor authentication for user and privileged accounts. |
| [[Pluggable Authentication Modules\|T1556.003]] | Pluggable Authentication Modules | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. |
| [[Modify Authentication Process\|T1556]] | Modify Authentication Process | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. MFA can also be used to restrict access to cloud resources and APIs.  |
| [[Network Boundary Bridging\|T1599]] | Network Boundary Bridging | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control.(Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Email Collection\|T1114]] | Email Collection | Use of multi-factor authentication for public-facing webmail servers is a recommended best practice to minimize the usefulness of usernames and passwords to adversaries. |
| [[Multi-Factor Authentication Request Generation\|T1621]] | Multi-Factor Authentication Request Generation | Implement more secure 2FA/MFA mechanisms in replacement of simple push or one-click 2FA/MFA options. For example, having users enter a one-time code provided by the login screen into the 2FA/MFA application or utilizing other out-of-band 2FA/MFA mechanisms (such as rotating code-based hardware tokens providing rotating codes that need an accompanying user pin) may be more secure. Furthermore, change default configurations and implement limits upon the maximum number of 2FA/MFA request prompts that can be sent to users in period of time.(Citation: MFA Fatigue Attacks - PortSwigger) |
| [[Modify System Image\|T1601]] | Modify System Image | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control.(Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Domain Accounts\|T1078.002]] | Domain Accounts | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. MFA can also be used to restrict access to cloud resources and APIs. |
| [[Domain Account\|T1136.002]] | Domain Account | Use multi-factor authentication for user and privileged accounts. |
| [[Cloud Account\|T1136.003]] | Cloud Account | Use multi-factor authentication for user and privileged accounts. |
| [[Device Registration\|T1098.005]] | Device Registration | Require multi-factor authentication to register devices in Azure AD.(Citation: Microsoft - Device Registration) Configure multi-factor authentication systems to disallow enrolling new devices for inactive accounts.(Citation: CISA MFA PrintNightmare) When first enrolling MFA, use conditional access policies to restrict device enrollment to trusted locations or devices, and consider using temporary access passes as an initial MFA solution to enroll a device.(Citation: Mandiant APT29 Microsoft 365 2022) |
| [[Password Spraying\|T1110.003]] | Password Spraying | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Cloud Accounts\|T1078.004]] | Cloud Accounts | Use multi-factor authentication for cloud accounts, especially privileged accounts. This can be implemented in a variety of forms (e.g. hardware, virtual, SMS), and can also be audited using administrative reporting features.(Citation: AWS - IAM Console Best Practices) |
| [[Downgrade System Image\|T1601.002]] | Downgrade System Image | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control.(Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Account Manipulation\|T1098]] | Account Manipulation | Use multi-factor authentication for user and privileged accounts. |
| [[Hybrid Identity\|T1556.007]] | Hybrid Identity | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. MFA can also be used to restrict access to cloud resources and APIs.  |
| [[SSH\|T1021.004]] | SSH | Require multi-factor authentication for SSH connections wherever possible, such as password protected SSH keys. |
| [[Steal Web Session Cookie\|T1539]] | Steal Web Session Cookie | A physical second factor key that uses the target login domain as part of the negotiation protocol will prevent session cookie theft through proxy methods.(Citation: Evilginx 2 July 2018) |
| [[Network Address Translation Traversal\|T1599.001]] | Network Address Translation Traversal | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control. (Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Additional Cloud Roles\|T1098.003]] | Additional Cloud Roles | Use multi-factor authentication for user and privileged accounts. |
| [[Password Guessing\|T1110.001]] | Password Guessing | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Remote Email Collection\|T1114.002]] | Remote Email Collection | Use of multi-factor authentication for public-facing webmail servers is a recommended best practice to minimize the usefulness of usernames and passwords to adversaries. |
| [[Trusted Relationship\|T1199]] | Trusted Relationship | Require MFA for all delegated administrator accounts.(Citation: Microsoft Nobelium Admin Privileges) |
| [[Remote Desktop Protocol\|T1021.001]] | Remote Desktop Protocol | Use multi-factor authentication for remote logins.(Citation: Berkley Secure) |
| [[Create Account\|T1136]] | Create Account | Use multi-factor authentication for user and privileged accounts. |
| [[Domain Controller Authentication\|T1556.001]] | Domain Controller Authentication | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. MFA can also be used to restrict access to cloud resources and APIs.  |
| [[Cloud Services\|T1021.007]] | Cloud Services | Use multi-factor authentication on cloud services whenever possible. |
| [[Software Deployment Tools\|T1072]] | Software Deployment Tools | Ensure proper system and access isolation for critical network systems through use of multi-factor authentication. |
| [[Brute Force\|T1110]] | Brute Force | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Credential Stuffing\|T1110.004]] | Credential Stuffing | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Password Cracking\|T1110.002]] | Password Cracking | Use multi-factor authentication. Where possible, also enable multi-factor authentication on externally facing services. |
| [[Remote Services\|T1021]] | Remote Services | Use multi-factor authentication on remote service logons where possible. |
| [[External Remote Services\|T1133]] | External Remote Services | Use strong two-factor or multi-factor authentication for remote service accounts to mitigate an adversary's ability to leverage stolen credentials, but be aware of [Multi-Factor Authentication Interception](https://attack.mitre.org/techniques/T1111) techniques for some two-factor authentication implementations. |
| [[Additional Email Delegate Permissions\|T1098.002]] | Additional Email Delegate Permissions | Use multi-factor authentication for user and privileged accounts. |
| [[Mitre Att&ck/mitigations/Multi-factor Authentication|T1556.006]] | Multi-Factor Authentication | Ensure that MFA and MFA policies and requirements are properly implemented for existing and deactivated or dormant accounts and devices. If possible, consider configuring MFA solutions to "fail closed" rather than grant access in case of serious errors. |
| [[Data from Cloud Storage\|T1530]] | Data from Cloud Storage | Consider using multi-factor authentication to restrict access to resources and cloud storage APIs.(Citation: Amazon S3 Security, 2019) |
| [[Patch System Image\|T1601.001]] | Patch System Image | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control.(Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Code Repositories\|T1213.003]] | Code Repositories | Use multi-factor authentication for logons to code repositories. |
| [[Network Device Authentication\|T1556.004]] | Network Device Authentication | Use multi-factor authentication for user and privileged accounts. Most embedded network devices support TACACS+ and/or RADIUS.  Follow vendor prescribed best practices for hardening access control. (Citation: Cisco IOS Software Integrity Assurance - TACACS) |
| [[Remote Desktop Protocol\|T1076]] | Remote Desktop Protocol | Use multi-factor authentication for remote logins. (Citation: Berkley Secure) |
| [[Application Deployment Software\|T1017]] | Application Deployment Software | Use multi-factor authentication for accounts used with application deployment software. |
| [[Remote Services\|T1021]] | Remote Services | Use multi-factor authentication on remote service logons where possible. |
| [[Valid Accounts\|T1078]] | Valid Accounts | Integrating multi-factor authentication (MFA) as part of organizational policy can greatly reduce the risk of an adversary gaining control of valid credentials that may be used for additional tactics such as initial access, lateral movement, and collecting information. MFA can also be used to restrict access to cloud resources and APIs. |
