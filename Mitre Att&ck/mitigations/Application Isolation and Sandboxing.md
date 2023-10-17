---
alias: M1048
---

## M1048

Restrict execution of code to a virtual environment on or in transit to an endpoint system.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Exploit Public-Facing Application\|T1190]] | Exploit Public-Facing Application | Application isolation will limit what other processes and system features the exploited target can access. |
| [[Escape to Host\|T1611]] | Escape to Host | Consider utilizing seccomp, seccomp-bpf, or a similar solution that restricts certain system calls such as mount. In Kubernetes environments, consider defining Pod Security Standards that limit container access to host process namespaces, the host network, and the host file system.(Citation: Kubernetes Hardening Guide) |
| [[Drive-by Compromise\|T1189]] | Drive-by Compromise | Browser sandboxes can be used to mitigate some of the impact of exploitation, but sandbox escapes may still exist.(Citation: Windows Blogs Microsoft Edge Sandbox)(Citation: Ars Technica Pwn2Own 2017 VM Escape)<br /><br />Other types of virtualization and application microsegmentation may also mitigate the impact of client-side exploitation. The risks of additional exploits and weaknesses in implementation may still exist for these types of systems.(Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Exploitation for Privilege Escalation\|T1068]] | Exploitation for Privilege Escalation | Make it difficult for adversaries to advance their operation through exploitation of undiscovered or unpatched vulnerabilities by using sandboxing. Other types of virtualization and application microsegmentation may also mitigate the impact of some types of exploitation. Risks of additional exploits and weaknesses in these systems may still exist. (Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Inter-Process Communication\|T1559]] | Inter-Process Communication | Ensure all COM alerts and Protected View are enabled.(Citation: Microsoft Protected View) |
| [[Distributed Component Object Model\|T1021.003]] | Distributed Component Object Model | Ensure all COM alerts and Protected View are enabled.(Citation: Microsoft Protected View) |
| [[Component Object Model\|T1559.001]] | Component Object Model | Ensure all COM alerts and Protected View are enabled.(Citation: Microsoft Protected View) |
| [[Exploitation of Remote Services\|T1210]] | Exploitation of Remote Services | Make it difficult for adversaries to advance their operation through exploitation of undiscovered or unpatched vulnerabilities by using sandboxing. Other types of virtualization and application microsegmentation may also mitigate the impact of some types of exploitation. Risks of additional exploits and weaknesses in these systems may still exist. (Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Dynamic Data Exchange\|T1559.002]] | Dynamic Data Exchange | Ensure Protected View is enabled.(Citation: Microsoft Protected View) |
| [[Exploitation for Client Execution\|T1203]] | Exploitation for Client Execution | Browser sandboxes can be used to mitigate some of the impact of exploitation, but sandbox escapes may still exist. (Citation: Windows Blogs Microsoft Edge Sandbox) (Citation: Ars Technica Pwn2Own 2017 VM Escape)<br /><br />Other types of virtualization and application microsegmentation may also mitigate the impact of client-side exploitation. Risks of additional exploits and weaknesses in those systems may still exist. (Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Exploitation for Credential Access\|T1212]] | Exploitation for Credential Access | Make it difficult for adversaries to advance their operation through exploitation of undiscovered or unpatched vulnerabilities by using sandboxing. Other types of virtualization and application microsegmentation may also mitigate the impact of some types of exploitation. Risks of additional exploits and weaknesses in these systems may still exist.(Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Exploitation for Defense Evasion\|T1211]] | Exploitation for Defense Evasion | Make it difficult for adversaries to advance their operation through exploitation of undiscovered or unpatched vulnerabilities by using sandboxing. Other types of virtualization and application microsegmentation may also mitigate the impact of some types of exploitation. Risks of additional exploits and weaknesses in these systems may still exist. (Citation: Ars Technica Pwn2Own 2017 VM Escape) |
| [[Dynamic Data Exchange\|T1173]] | Dynamic Data Exchange | Ensure Protected View is enabled.(Citation: Microsoft Protected View) |
