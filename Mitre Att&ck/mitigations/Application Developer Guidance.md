---
alias: M1013
---

## M1013

This mitigation describes any guidance or training given to developers of applications to avoid introducing security weaknesses that an adversary may be able to take advantage of.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Plist File Modification\|T1647]] | Plist File Modification | Ensure applications are using Apple's developer guidance which enables hardened runtime.(Citation: Apple Developer Doco Hardened Runtime) |
| [[Hijack Execution Flow\|T1574]] | Hijack Execution Flow | When possible, include hash values in manifest files to help prevent side-loading of malicious libraries.(Citation: FireEye DLL Side-Loading) |
| [[XPC Services\|T1559.003]] | XPC Services | Enable the Hardened Runtime capability when developing applications. Do not include the <code>com.apple.security.get-task-allow</code> entitlement with the value set to any variation of true.  |
| [[Code Repositories\|T1593.003]] | Code Repositories | Application developers uploading to public code repositories should be careful to avoid publishing sensitive information such as credentials and API keys. |
| [[Valid Accounts\|T1078]] | Valid Accounts | Ensure that applications do not store sensitive data or credentials insecurely. (e.g. plaintext credentials in code, published credentials in repositories, or credentials in public cloud storage). |
| [[Resource Forking\|T1564.009]] | Resource Forking | Configure applications to use the application bundle structure which leverages the <code>/Resources</code> folder location.(Citation: Apple App Security Overview)  |
| [[DLL Side-Loading\|T1574.002]] | DLL Side-Loading | When possible, include hash values in manifest files to help prevent side-loading of malicious libraries.(Citation: FireEye DLL Side-Loading) |
| [[Search Open Websites／Domains\|T1593]] | Search Open Websites／Domains | Application developers uploading to public code repositories should be careful to avoid publishing sensitive information such as credentials and API keys. |
| [[Inter-Process Communication\|T1559]] | Inter-Process Communication | Enable the Hardened Runtime capability when developing applications. Do not include the <code>com.apple.security.get-task-allow</code> entitlement with the value set to any variation of true.  |
| [[Plist Modification\|T1547.011]] | Plist Modification | Ensure applications are using Apple's developer guidance which enables hardened runtime.(Citation: Apple Developer Doco Hardened Runtime) |
