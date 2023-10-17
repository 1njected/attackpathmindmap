---
alias: M1041
---

## M1041

Protect sensitive information with strong encryption.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Unsecured Credentials\|T1552]] | Unsecured Credentials | When possible, store keys on separate cryptographic hardware instead of on the local system.  |
| [[ARP Cache Poisoning\|T1557.002]] | ARP Cache Poisoning | Ensure that all wired and/or wireless traffic is encrypted appropriately. Use best practices for authentication protocols, such as Kerberos, and ensure web traffic that may contain credentials is protected by SSL/TLS. |
| [[Adversary-in-the-Middle\|T1557]] | Adversary-in-the-Middle | Ensure that all wired and/or wireless traffic is encrypted appropriately. Use best practices for authentication protocols, such as Kerberos, and ensure web traffic that may contain credentials is protected by SSL/TLS. |
| [[Indicator Removal\|T1070]] | Indicator Removal | Obfuscate/encrypt event files locally and in transit to avoid giving feedback to an adversary. |
| [[Network Device Configuration Dump\|T1602.002]] | Network Device Configuration Dump | Configure SNMPv3 to use the highest level of security (authPriv) available.(Citation: US-CERT TA17-156A SNMP Abuse 2017)  |
| [[OS Credential Dumping\|T1003]] | OS Credential Dumping | Ensure Domain Controller backups are properly secured. |
| [[Transmitted Data Manipulation\|T1565.002]] | Transmitted Data Manipulation | Encrypt all important data flows to reduce the impact of tailored modifications on data in transit. |
| [[Data Manipulation\|T1565]] | Data Manipulation | Consider encrypting important information to reduce an adversary’s ability to perform tailored data modifications. |
| [[Steal or Forge Kerberos Tickets\|T1558]] | Steal or Forge Kerberos Tickets | Enable AES Kerberos encryption (or another stronger encryption algorithm), rather than RC4, where possible.(Citation: AdSecurity Cracking Kerberos Dec 2015) |
| [[Data from Cloud Storage\|T1530]] | Data from Cloud Storage | Encrypt data stored at rest in cloud storage.(Citation: Amazon S3 Security, 2019)(Citation: Microsoft Azure Storage Security, 2019) Managed encryption keys can be rotated by most providers. At a minimum, ensure an incident response plan to storage breach includes rotating the keys and test for impact on client applications.(Citation: Google Cloud Encryption Key Rotation) |
| [[Network Sniffing\|T1040]] | Network Sniffing | Ensure that all wired and/or wireless traffic is encrypted appropriately. Use best practices for authentication protocols, such as Kerberos, and ensure web traffic that may contain credentials is protected by SSL/TLS. |
| [[Clear Windows Event Logs\|T1070.001]] | Clear Windows Event Logs | Obfuscate/encrypt event files locally and in transit to avoid giving feedback to an adversary. |
| [[Remote Email Collection\|T1114.002]] | Remote Email Collection | Use of encryption provides an added layer of security to sensitive information sent over email. Encryption using public key cryptography requires the adversary to obtain the private certificate along with an encryption key to decrypt messages. |
| [[SNMP (MIB Dump)\|T1602.001]] | SNMP (MIB Dump) | Configure SNMPv3 to use the highest level of security (authPriv) available.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[Automated Collection\|T1119]] | Automated Collection | Encryption and off-system storage of sensitive information may be one way to mitigate collection of files, but may not stop an adversary from acquiring the information if an intrusion persists over a long period of time and the adversary is able to discover and access the data through other means. Strong passwords should be used on certain encrypted documents that use them to prevent offline cracking through [Brute Force](https://attack.mitre.org/techniques/T1110) techniques. |
| [[Steal or Forge Authentication Certificates\|T1649]] | Steal or Forge Authentication Certificates | Ensure certificates as well as associated private keys are appropriately secured. Consider utilizing additional hardware credential protections such as trusted platform modules (TPM) or hardware security modules (HSM). Enforce HTTPS and enable Extended Protection for<br />Authentication.(Citation: SpecterOps Certified Pre Owned) |
| [[Email Forwarding Rule\|T1114.003]] | Email Forwarding Rule | Use of encryption provides an added layer of security to sensitive information sent over email. Encryption using public key cryptography requires the adversary to obtain the private certificate along with an encryption key to decrypt messages. |
| [[Stored Data Manipulation\|T1565.001]] | Stored Data Manipulation | Consider encrypting important information to reduce an adversary’s ability to perform tailored data modifications. |
| [[AS-REP Roasting\|T1558.004]] | AS-REP Roasting | Enable AES Kerberos encryption (or another stronger encryption algorithm), rather than RC4, where possible.(Citation: AdSecurity Cracking Kerberos Dec 2015) |
| [[Email Collection\|T1114]] | Email Collection | Use of encryption provides an added layer of security to sensitive information sent over email. Encryption using public key cryptography requires the adversary to obtain the private certificate along with an encryption key to decrypt messages. |
| [[Kerberoasting\|T1558.003]] | Kerberoasting | Enable AES Kerberos encryption (or another stronger encryption algorithm), rather than RC4, where possible.(Citation: AdSecurity Cracking Kerberos Dec 2015) |
| [[Traffic Duplication\|T1020.001]] | Traffic Duplication | Ensure that all wired and/or wireless traffic is encrypted appropriately. Use best practices for authentication protocols, such as Kerberos, and ensure web traffic that may contain credentials is protected by SSL/TLS. |
| [[Clear Linux or Mac System Logs\|T1070.002]] | Clear Linux or Mac System Logs | Obfuscate/encrypt event files locally and in transit to avoid giving feedback to an adversary. |
| [[Data from Configuration Repository\|T1602]] | Data from Configuration Repository | Configure SNMPv3 to use the highest level of security (authPriv) available.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[NTDS\|T1003.003]] | NTDS | Ensure Domain Controller backups are properly secured.(Citation: Metcalf 2015) |
| [[Private Keys\|T1552.004]] | Private Keys | When possible, store keys on separate cryptographic hardware instead of on the local system. For example, on Windows systems use a TPM to secure keys and other sensitive credential material.(Citation: Microsoft Primary Refresh Token) |
| [[Application Access Token\|T1550.001]] | Application Access Token | File encryption should be enforced across email communications containing sensitive information that may be obtained through access to email services. |
| [[Local Email Collection\|T1114.001]] | Local Email Collection | Use of encryption provides an added layer of security to sensitive information sent over email. Encryption using public key cryptography requires the adversary to obtain the private certificate along with an encryption key to decrypt messages. |
| [[Silver Ticket\|T1558.002]] | Silver Ticket | Enable AES Kerberos encryption (or another stronger encryption algorithm), rather than RC4, where possible.(Citation: AdSecurity Cracking Kerberos Dec 2015) |
| [[Stored Data Manipulation\|T1492]] | Stored Data Manipulation | Consider encrypting important information to reduce an adversaries ability to perform tailored data modifications. |
| [[Kerberoasting\|T1208]] | Kerberoasting | Enable AES Kerberos encryption (or another stronger encryption algorithm), rather than RC4, where possible. (Citation: AdSecurity Cracking Kerberos Dec 2015) |
| [[Private Keys\|T1145]] | Private Keys | When possible, store keys on separate cryptographic hardware instead of on the local system.  |
| [[Transmitted Data Manipulation\|T1493]] | Transmitted Data Manipulation | Encrypt all important data flows to reduce the impact of tailored modifications on data in transit. |
| [[Application Access Token\|T1527]] | Application Access Token | File encryption should be enforced across email communications containing sensitive information that may be obtained through access to email services. |
