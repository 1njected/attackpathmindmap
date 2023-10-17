---
alias: M1030
---

## M1030

Architect sections of the network to isolate critical systems, functions, or resources. Use physical and logical segmentation to prevent access to potentially sensitive systems and information. Use a DMZ to contain any internet-facing services that should not be exposed from the internal network. Configure separate virtual private cloud (VPC) instances to isolate critical cloud systems.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Runtime Data Manipulation\|T1565.003]] | Runtime Data Manipulation | Identify critical business and system processes that may be targeted by adversaries and work to isolate and secure those systems against unauthorized access and tampering. |
| [[Container and Resource Discovery\|T1613]] | Container and Resource Discovery | Deny direct remote access to internal systems through the use of network proxies, gateways, and firewalls. |
| [[Account Manipulation\|T1098]] | Account Manipulation | Configure access controls and firewalls to limit access to critical systems and domain controllers. Most cloud environments support separate virtual private cloud (VPC) instances that enable further segmentation of cloud systems. |
| [[Create Account\|T1136]] | Create Account | Configure access controls and firewalls to limit access to domain controllers and systems used to create and manage accounts. |
| [[Remote Desktop Protocol\|T1021.001]] | Remote Desktop Protocol | Do not leave RDP accessible from the internet. Enable firewall rules to block RDP traffic between network security zones within a network. |
| [[Exploit Public-Facing Application\|T1190]] | Exploit Public-Facing Application | Segment externally facing servers and services from the rest of the network with a DMZ or on separate hosting infrastructure. |
| [[Network Device Configuration Dump\|T1602.002]] | Network Device Configuration Dump | Segregate SNMP traffic on a separate management network.(Citation: US-CERT TA17-156A SNMP Abuse 2017)  |
| [[Cloud Account\|T1136.003]] | Cloud Account | Configure access controls and firewalls to limit access to critical systems and domain controllers. Most cloud environments support separate virtual private cloud (VPC) instances that enable further segmentation of cloud systems. |
| [[RDP Hijacking\|T1563.002]] | RDP Hijacking | Enable firewall rules to block RDP traffic between network security zones within a network. |
| [[Service Stop\|T1489]] | Service Stop | Operate intrusion detection, analysis, and response systems on a separate network from the production environment to lessen the chances that an adversary can see and interfere with critical response functions. |
| [[Exploitation of Remote Services\|T1210]] | Exploitation of Remote Services | Segment networks and systems appropriately to reduce access to critical systems and services to controlled methods. |
| [[Exfiltration Over Alternative Protocol\|T1048]] | Exfiltration Over Alternative Protocol | Follow best practices for network firewall configurations to allow only necessary ports and traffic to enter and exit the network.(Citation: TechNet Firewall Design) |
| [[Build Image on Host\|T1612]] | Build Image on Host | Deny direct remote access to internal systems through the use of network proxies, gateways, and firewalls. |
| [[Domain Trust Discovery\|T1482]] | Domain Trust Discovery | Employ network segmentation for sensitive domains.(Citation: Harmj0y Domain Trusts). |
| [[Additional Cloud Credentials\|T1098.001]] | Additional Cloud Credentials | Configure access controls and firewalls to limit access to critical systems and domain controllers. Most cloud environments support separate virtual private cloud (VPC) instances that enable further segmentation of cloud systems. |
| [[Deploy Container\|T1610]] | Deploy Container | Deny direct remote access to internal systems through the use of network proxies, gateways, and firewalls. |
| [[Network Service Discovery\|T1046]] | Network Service Discovery | Ensure proper network segmentation is followed to protect critical servers and devices. |
| [[Remote Service Session Hijacking\|T1563]] | Remote Service Session Hijacking | Enable firewall rules to block unnecessary traffic between network security zones within a network. |
| [[Non-Standard Port\|T1571]] | Non-Standard Port | Properly configure firewalls and proxies to limit outgoing traffic to only necessary ports for that particular network segment. |
| [[External Remote Services\|T1133]] | External Remote Services | Deny direct remote access to internal systems through the use of network proxies, gateways, and firewalls. |
| [[Software Deployment Tools\|T1072]] | Software Deployment Tools | Ensure proper system isolation for critical network systems through use of firewalls. |
| [[Distributed Component Object Model\|T1021.003]] | Distributed Component Object Model | Enable Windows firewall, which prevents DCOM instantiation by default. |
| [[Exfiltration Over Asymmetric Encrypted Non-C2 Protocol\|T1048.002]] | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Follow best practices for network firewall configurations to allow only necessary ports and traffic to enter and exit the network.(Citation: TechNet Firewall Design) |
| [[Adversary-in-the-Middle\|T1557]] | Adversary-in-the-Middle | Network segmentation can be used to isolate infrastructure components that do not require broad network access. This may mitigate, or at least alleviate, the scope of AiTM activity. |
| [[Container API\|T1552.007]] | Container API | Deny direct remote access to internal systems through the use of network proxies, gateways, and firewalls. |
| [[Data from Configuration Repository\|T1602]] | Data from Configuration Repository | Segregate SNMP traffic on a separate management network.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[Exfiltration Over Unencrypted Non-C2 Protocol\|T1048.003]] | Exfiltration Over Unencrypted Non-C2 Protocol | Follow best practices for network firewall configurations to allow only necessary ports and traffic to enter and exit the network.(Citation: TechNet Firewall Design) |
| [[Non-Application Layer Protocol\|T1095]] | Non-Application Layer Protocol | Properly configure firewalls and proxies to limit outgoing traffic to only necessary ports and through proper network gateway systems. Also ensure hosts are only provisioned to communicate over authorized interfaces. |
| [[Data Manipulation\|T1565]] | Data Manipulation | Identify critical business and system processes that may be targeted by adversaries and work to isolate and secure those systems against unauthorized access and tampering. |
| [[SNMP (MIB Dump)\|T1602.001]] | SNMP (MIB Dump) | Segregate SNMP traffic on a separate management network.(Citation: US-CERT TA17-156A SNMP Abuse 2017) |
| [[LLMNR／NBT-NS Poisoning and SMB Relay\|T1557.001]] | LLMNR／NBT-NS Poisoning and SMB Relay | Network segmentation can be used to isolate infrastructure components that do not require broad network access. This may mitigate, or at least alleviate, the scope of AiTM activity. |
| [[Windows Remote Management\|T1021.006]] | Windows Remote Management | If the service is necessary, lock down critical enclaves with separate WinRM infrastructure and follow WinRM best practices on use of host firewalls to restrict WinRM access to allow communication only to/from specific devices.(Citation: NSA Spotting) |
| [[Exfiltration Over Symmetric Encrypted Non-C2 Protocol\|T1048.001]] | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Follow best practices for network firewall configurations to allow only necessary ports and traffic to enter and exit the network.(Citation: TechNet Firewall Design) |
| [[Domain Account\|T1136.002]] | Domain Account | Configure access controls and firewalls to limit access to domain controllers and systems used to create and manage accounts. |
| [[Trusted Relationship\|T1199]] | Trusted Relationship | Network segmentation can be used to isolate infrastructure components that do not require broad network access. |
| [[Runtime Data Manipulation\|T1494]] | Runtime Data Manipulation | Identify critical business and system processes that may be targeted by adversaries and work to isolate and secure those systems against unauthorized access and tampering.  |
| [[Custom Command and Control Protocol\|T1094]] | Custom Command and Control Protocol | Properly configure firewalls and proxies to limit outgoing traffic to only necessary ports and through proper network gateway systems. Also ensure hosts are only provisioned to communicate over authorized interfaces. |
| [[Private Keys\|T1145]] | Private Keys | Use separate infrastructure for managing critical systems to prevent overlap of credentials and permissions on systems that could be used as vectors for lateral movement. |
| [[Windows Remote Management\|T1028]] | Windows Remote Management | If the service is necessary, lock down critical enclaves with separate WinRM infrastructure and follow WinRM best practices on use of host firewalls to restrict WinRM access to allow communication only to/from specific devices. (Citation: NSA Spotting) |
| [[Remote Desktop Protocol\|T1076]] | Remote Desktop Protocol | Do not leave RDP accessible from the internet. Enable firewall rules to block RDP traffic between network security zones within a network. |
| [[Uncommonly Used Port\|T1065]] | Uncommonly Used Port | Properly configure firewalls and proxies to limit outgoing traffic to only necessary ports for that particular network segment. |
| [[Application Deployment Software\|T1017]] | Application Deployment Software | Ensure proper system and access isolation for critical network systems through use of firewalls, account privilege separation, group policy, and multi-factor authentication. |
