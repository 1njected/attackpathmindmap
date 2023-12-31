---
alias: T1530
---

## T1530

Adversaries may access data from improperly secured cloud storage.

Many cloud service providers offer solutions for online data object storage such as Amazon S3, Azure Storage, and Google Cloud Storage. These solutions differ from other storage solutions (such as SQL or Elasticsearch) in that there is no overarching application. Data from these solutions can be retrieved directly using the cloud provider's APIs. 

In other cases, SaaS application providers such as Slack, Confluence, and Salesforce also provide cloud storage solutions as a peripheral use case of their platform. These cloud objects can be extracted directly from their associated application.(Citation: EA Hacked via Slack - June 2021)(Citation: SecureWorld - How Secure Is Your Slack Channel - Dec 2021)(Citation: HackerNews - 3 SaaS App Cyber Attacks - April 2022)(Citation: Dark Clouds_Usenix_Mulazzani_08_2011)

Adversaries may collect sensitive data from these cloud storage solutions. Providers typically offer security guides to help end users configure systems, though misconfigurations are a common problem.(Citation: Amazon S3 Security, 2019)(Citation: Microsoft Azure Storage Security, 2019)(Citation: Google Cloud Storage Best Practices, 2019) There have been numerous incidents where cloud storage has been improperly secured, typically by unintentionally allowing public access to unauthenticated users, overly-broad access by all users, or even access for any anonymous person outside the control of the Identity Access Management system without even needing basic user permissions.

This open access may expose various types of sensitive data, such as credit cards, personally identifiable information, or medical records.(Citation: Trend Micro S3 Exposed PII, 2017)(Citation: Wired Magecart S3 Buckets, 2019)(Citation: HIPAA Journal S3 Breach, 2017)(Citation: Rclone-mega-extortion_05_2021)

Adversaries may also obtain then abuse leaked credentials from source repositories, logs, or other means as a way to gain access to cloud storage objects.


### Tactic
- [[Collection]] (TA0009)

### Platforms
- IaaS
- SaaS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Filter Network Traffic\|M1037]] | Filter Network Traffic | Cloud service providers support IP-based restrictions when accessing cloud resources. Consider using IP allowlisting along with user account management to ensure that data access is restricted not only to valid users but only from expected IP ranges to mitigate the use of stolen credentials to access data. |
| [[User Account Management\|M1018]] | User Account Management | Configure user permissions groups and roles for access to cloud storage.(Citation: Microsoft Azure Storage Security, 2019) Implement strict Identity and Access Management (IAM) controls to prevent access to storage solutions except for the applications, users, and services that require access.(Citation: Amazon S3 Security, 2019) Ensure that temporary access tokens are issued rather than permanent credentials, especially when access is being granted to entities outside of the internal security boundary.(Citation: Amazon  AWS Temporary Security Credentials) |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Use access control lists on storage systems and objects. |
| [[Mitre Att&ck/techniques/Multi-Factor Authentication|M1032]] | Multi-factor Authentication | Consider using multi-factor authentication to restrict access to resources and cloud storage APIs.(Citation: Amazon S3 Security, 2019) |
| [[Audit\|M1047]] | Audit | Frequently check permissions on cloud storage to ensure proper permissions are set to deny open or unprivileged access to resources.(Citation: Amazon S3 Security, 2019) |
| [[Encrypt Sensitive Information\|M1041]] | Encrypt Sensitive Information | Encrypt data stored at rest in cloud storage.(Citation: Amazon S3 Security, 2019)(Citation: Microsoft Azure Storage Security, 2019) Managed encryption keys can be rotated by most providers. At a minimum, ensure an incident response plan to storage breach includes rotating the keys and test for impact on client applications.(Citation: Google Cloud Encryption Key Rotation) |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1530
- SecureWorld - How Secure Is Your Slack Channel - Dec 2021: https://www.secureworld.io/industry-news/how-secure-is-your-slack-channel#:~:text=Electronic%20Arts%20hacked%20through%20Slack%20channel&text=In%20total%2C%20the%20hackers%20claim,credentials%20over%20a%20Slack%20channel.
- Amazon S3 Security, 2019: https://aws.amazon.com/premiumsupport/knowledge-center/secure-s3-resources/
- Microsoft Azure Storage Security, 2019: https://docs.microsoft.com/en-us/azure/storage/common/storage-security-guide
- EA Hacked via Slack - June 2021: https://www.techradar.com/news/ea-hack-reportedly-used-stolen-cookies-and-slack-to-hack-gaming-giant
- Wired Magecart S3 Buckets, 2019: https://www.wired.com/story/magecart-amazon-cloud-hacks/
- Google Cloud Storage Best Practices, 2019: https://cloud.google.com/storage/docs/best-practices
- HackerNews - 3 SaaS App Cyber Attacks - April 2022: https://thehackernews.com/2022/04/into-breach-breaking-down-3-saas-app.html
- HIPAA Journal S3 Breach, 2017: https://www.hipaajournal.com/47gb-medical-records-unsecured-amazon-s3-bucket/
- Rclone-mega-extortion_05_2021: https://redcanary.com/blog/rclone-mega-extortion/
- Dark Clouds_Usenix_Mulazzani_08_2011: https://www.usenix.org/conference/usenix-security-11/dark-clouds-horizon-using-cloud-storage-attack-vector-and-online-slack
- Trend Micro S3 Exposed PII, 2017: https://www.trendmicro.com/vinfo/us/security/news/virtualization-and-cloud/a-misconfigured-amazon-s3-exposed-almost-50-thousand-pii-in-australia
