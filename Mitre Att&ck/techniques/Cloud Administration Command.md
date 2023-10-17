---
alias: T1651
---

## T1651

Adversaries may abuse cloud management services to execute commands within virtual machines or hybrid-joined devices. Resources such as AWS Systems Manager, Azure RunCommand, and Runbooks allow users to remotely run scripts in virtual machines by leveraging installed virtual machine agents. Similarly, in Azure AD environments, Microsoft Endpoint Manager allows Global or Intune Administrators to run scripts as SYSTEM on on-premises devices joined to the Azure AD.(Citation: AWS Systems Manager Run Command)(Citation: Microsoft Run Command)(Citation: SpecterOps Lateral Movement from Azure to On-Prem AD 2020)

If an adversary gains administrative access to a cloud environment, they may be able to abuse cloud management services to execute commands in the environment’s virtual machines or on-premises hybrid-joined devices. Additionally, an adversary that compromises a service provider or delegated administrator account may similarly be able to leverage a [Trusted Relationship](https://attack.mitre.org/techniques/T1199) to execute commands in connected virtual machines.(Citation: MSTIC Nobelium Oct 2021)


### Tactic
- [[Execution]] (TA0002)

### Platforms
- IaaS
- Azure AD

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Limit the number of cloud accounts with permissions to remotely execute commands on virtual machines, and ensure that these are not used for day-to-day operations. In Azure, limit the number of accounts with the roles Azure Virtual Machine Contributer and above, and consider using temporary Just-in-Time (JIT) roles to avoid permanently assigning privileged access to virtual machines.(Citation: Mandiant Azure Run Command 2021) In Azure AD, limit the number of Global and Intune administrators to only those required. In AWS, limit users with permission to execute the `ssm:SendCommand` action, and use tags to restrict the number of machines those users can execute commands on.(Citation: AWS Setting Up Run Command) |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1651
- SpecterOps Lateral Movement from Azure to On-Prem AD 2020: https://posts.specterops.io/death-from-above-lateral-movement-from-azure-to-on-prem-ad-d18cb3959d4d
- AWS Systems Manager Run Command: https://docs.aws.amazon.com/systems-manager/latest/userguide/run-command.html
- MSTIC Nobelium Oct 2021: https://www.microsoft.com/security/blog/2021/10/25/nobelium-targeting-delegated-administrative-privileges-to-facilitate-broader-attacks/
- Microsoft Run Command: https://learn.microsoft.com/en-us/azure/virtual-machines/run-command-overview
