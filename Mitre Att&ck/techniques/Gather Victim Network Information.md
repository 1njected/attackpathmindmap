---
alias: T1590
---

## T1590

Adversaries may gather information about the victim's networks that can be used during targeting. Information about networks may include a variety of details, including administrative data (ex: IP ranges, domain names, etc.) as well as specifics regarding its topology and operations.

Adversaries may gather this information in various ways, such as direct collection actions via [Active Scanning](https://attack.mitre.org/techniques/T1595) or [Phishing for Information](https://attack.mitre.org/techniques/T1598). Information about networks may also be exposed to adversaries via online or other accessible data sets (ex: [Search Open Technical Databases](https://attack.mitre.org/techniques/T1596)).(Citation: WHOIS)(Citation: DNS Dumpster)(Citation: Circl Passive DNS) Gathering this information may reveal opportunities for other forms of reconnaissance (ex: [Active Scanning](https://attack.mitre.org/techniques/T1595) or [Search Open Websites/Domains](https://attack.mitre.org/techniques/T1593)), establishing operational resources (ex: [Acquire Infrastructure](https://attack.mitre.org/techniques/T1583) or [Compromise Infrastructure](https://attack.mitre.org/techniques/T1584)), and/or initial access (ex: [Trusted Relationship](https://attack.mitre.org/techniques/T1199)).


### Tactic
- [[Reconnaissance]] (TA0043)

### Platforms
- PRE

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Pre-compromise\|M1056]] | Pre-compromise | This technique cannot be easily mitigated with preventive controls since it is based on behaviors performed outside of the scope of enterprise defenses and controls. Efforts should focus on minimizing the amount and sensitivity of data available to external parties. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[IP Addresses\|T1590.005]] | IP Addresses |
| [[DNS\|T1590.002]] | DNS |
| [[Network Topology\|T1590.004]] | Network Topology |
| [[Network Trust Dependencies\|T1590.003]] | Network Trust Dependencies |
| [[Network Security Appliances\|T1590.006]] | Network Security Appliances |
| [[Domain Properties\|T1590.001]] | Domain Properties |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1590
- WHOIS: https://www.whois.net/
- DNS Dumpster: https://dnsdumpster.com/
- Circl Passive DNS: https://www.circl.lu/services/passive-dns/
