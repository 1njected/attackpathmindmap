---
alias: T1090.003
---

## T1090.003

To disguise the source of malicious traffic, adversaries may chain together multiple proxies. Typically, a defender will be able to identify the last proxy traffic traversed before it enters their network; the defender may or may not be able to identify any previous proxies before the last-hop proxy. This technique makes identifying the original source of the malicious traffic even more difficult by requiring the defender to trace malicious traffic through several proxies to identify its source. A particular variant of this behavior is to use onion routing networks, such as the publicly available TOR network. (Citation: Onion Routing)

In the case of network infrastructure, particularly routers, it is possible for an adversary to leverage multiple compromised devices to create a multi-hop proxy chain within the Wide-Area Network (WAN) of the enterprise.  By leveraging [Patch System Image](https://attack.mitre.org/techniques/T1601/001), adversaries can add custom code to the affected network devices that will implement onion routing between those nodes.  This custom onion routing network will transport the encrypted C2 traffic through the compromised population, allowing adversaries to communicate with any device within the onion routing network.  This method is dependent upon the [Network Boundary Bridging](https://attack.mitre.org/techniques/T1599) method in order to allow the adversaries to cross the protected network boundary of the Internet perimeter and into the organization’s WAN. Protocols such as ICMP may be used as a transport.


### Tactic
- [[Command and Control]] (TA0011)

### Platforms
- Linux
- macOS
- Windows
- Network

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Filter Network Traffic\|M1037]] | Filter Network Traffic | Traffic to known anonymity networks and C2 infrastructure can be blocked through the use of network allow and block lists. It should be noted that this kind of blocking may be circumvented by other techniques like [Domain Fronting](https://attack.mitre.org/techniques/T1090/004). |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1090/003
- Onion Routing: https://en.wikipedia.org/wiki/Onion_routing
