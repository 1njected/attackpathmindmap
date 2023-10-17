---
alias: T1537
---

## T1537

Adversaries may exfiltrate data by transferring the data, including backups of cloud environments, to another cloud account they control on the same service to avoid typical file transfers/downloads and network-based exfiltration detection.

A defender who is monitoring for large transfers to outside the cloud environment through normal file transfers or over command and control channels may not be watching for data transfers to another account within the same cloud provider. Such transfers may utilize existing cloud provider APIs and the internal address space of the cloud provider to blend into normal traffic or avoid data transfers over external network interfaces.

Incidents have been observed where adversaries have created backups of cloud instances and transferred them to separate accounts.(Citation: DOJ GRU Indictment Jul 2018) 


### Tactic
- [[Exfiltration]] (TA0010)

### Platforms
- IaaS

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Filter Network Traffic\|M1037]] | Filter Network Traffic | Implement network-based filtering restrictions to prohibit data transfers to untrusted VPCs. |
| [[Password Policies\|M1027]] | Password Policies | Consider rotating access keys within a certain number of days to reduce the effectiveness of stolen credentials. |
| [[User Account Management\|M1018]] | User Account Management | Limit user account and IAM policies to the least privileges required. Consider using temporary credentials for accounts that are only valid for a certain period of time to reduce the effectiveness of compromised accounts. |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1537
- AWS EBS Snapshot Sharing: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-modifying-snapshot-permissions.html
- Azure Shared Access Signature: https://docs.microsoft.com/en-us/rest/api/storageservices/delegate-access-with-shared-access-signature
- Azure Blob Snapshots: https://docs.microsoft.com/en-us/azure/storage/blobs/snapshots-overview
- DOJ GRU Indictment Jul 2018: https://www.justice.gov/file/1080281/download
