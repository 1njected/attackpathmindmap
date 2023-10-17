---
alias: T1583
---

## T1583

Adversaries may buy, lease, or rent infrastructure that can be used during targeting. A wide variety of infrastructure exists for hosting and orchestrating adversary operations. Infrastructure solutions include physical or cloud servers, domains, and third-party web services.(Citation: TrendmicroHideoutsLease) Additionally, botnets are available for rent or purchase.

Use of these infrastructure solutions allows adversaries to stage, launch, and execute operations. Solutions may help adversary operations blend in with traffic that is seen as normal, such as contacting third-party web services or acquiring infrastructure to support [Proxy](https://attack.mitre.org/techniques/T1090).(Citation: amnesty_nso_pegasus) Depending on the implementation, adversaries may use infrastructure that makes it difficult to physically tie back to them as well as utilize infrastructure that can be rapidly provisioned, modified, and shut down.


### Tactic
- [[Resource Development]] (TA0042)

### Platforms
- PRE

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Pre-compromise\|M1056]] | Pre-compromise | This technique cannot be easily mitigated with preventive controls since it is based on behaviors performed outside of the scope of enterprise defenses and controls. |

### Sub-techniques

| ID | Name |
| --- | --- |
| [[Serverless\|T1583.007]] | Serverless |
| [[Malvertising\|T1583.008]] | Malvertising |
| [[DNS Server\|T1583.002]] | DNS Server |
| [[Botnet\|T1583.005]] | Botnet |
| [[Domains\|T1583.001]] | Domains |
| [[Server\|T1583.004]] | Server |
| [[Virtual Private Server\|T1583.003]] | Virtual Private Server |
| [[Web Services\|T1583.006]] | Web Services |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1583
- amnesty_nso_pegasus: https://www.amnesty.org/en/latest/research/2021/07/forensic-methodology-report-how-to-catch-nso-groups-pegasus/
- Koczwara Beacon Hunting Sep 2021: https://michaelkoczwara.medium.com/cobalt-strike-c2-hunting-with-shodan-c448d501a6e2
- TrendmicroHideoutsLease: https://documents.trendmicro.com/assets/wp/wp-criminal-hideouts-for-lease.pdf
- Mandiant SCANdalous Jul 2020: https://www.mandiant.com/resources/scandalous-external-detection-using-network-scan-data-and-automation
- ThreatConnect Infrastructure Dec 2020: https://threatconnect.com/blog/infrastructure-research-hunting/
