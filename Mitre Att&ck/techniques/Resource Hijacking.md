---
alias: T1496
---

## T1496

Adversaries may leverage the resources of co-opted systems in order to solve resource intensive problems, which may impact system and/or hosted service availability. 

One common purpose for Resource Hijacking is to validate transactions of cryptocurrency networks and earn virtual currency. Adversaries may consume enough system resources to negatively impact and/or cause affected machines to become unresponsive.(Citation: Kaspersky Lazarus Under The Hood Blog 2017) Servers and cloud-based systems are common targets because of the high potential for available resources, but user endpoint systems may also be compromised and used for Resource Hijacking and cryptocurrency mining.(Citation: CloudSploit - Unused AWS Regions) Containerized environments may also be targeted due to the ease of deployment via exposed APIs and the potential for scaling mining activities by deploying or compromising multiple containers within an environment or cluster.(Citation: Unit 42 Hildegard Malware)(Citation: Trend Micro Exposed Docker APIs)

Additionally, some cryptocurrency mining malware identify then kill off processes for competing malware to ensure it’s not competing for resources.(Citation: Trend Micro War of Crypto Miners)

Adversaries may also use malware that leverages a system's network bandwidth as part of a botnet in order to facilitate [Network Denial of Service](https://attack.mitre.org/techniques/T1498) campaigns and/or to seed malicious torrents.(Citation: GoBotKR)


### Tactic
- [[Impact]] (TA0040)

### Platforms
- Windows
- IaaS
- Linux
- macOS
- Containers

### Permissions Required

### Mitigations

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1496
- Unit 42 Hildegard Malware: https://unit42.paloaltonetworks.com/hildegard-malware-teamtnt/
- CloudSploit - Unused AWS Regions: https://blog.cloudsploit.com/the-danger-of-unused-aws-regions-af0bf1b878fc
- Kaspersky Lazarus Under The Hood Blog 2017: https://securelist.com/lazarus-under-the-hood/77908/
- Trend Micro Exposed Docker APIs: https://www.trendmicro.com/en_us/research/19/e/infected-cryptocurrency-mining-containers-target-docker-hosts-with-exposed-apis-use-shodan-to-find-additional-victims.html
- Trend Micro War of Crypto Miners: https://www.trendmicro.com/en_us/research/20/i/war-of-linux-cryptocurrency-miners-a-battle-for-resources.html
- GoBotKR: https://www.welivesecurity.com/2019/07/08/south-korean-users-backdoor-torrents/
