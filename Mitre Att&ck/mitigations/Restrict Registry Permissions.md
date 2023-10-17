---
alias: M1024
---

## M1024

Restrict the ability to modify certain hives or keys in the Windows Registry.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Time Providers\|T1547.003]] | Time Providers | Consider using Group Policy to configure and block modifications to W32Time parameters in the Registry. (Citation: Microsoft W32Time May 2017) |
| [[COR_PROFILER\|T1574.012]] | COR_PROFILER | Ensure proper permissions are set for Registry hives to prevent users from modifying keys associated with COR_PROFILER. |
| [[Logon Script (Windows)\|T1037.001]] | Logon Script (Windows) | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for logon scripts that may lead to persistence. |
| [[Network Provider DLL\|T1556.008]] | Network Provider DLL | Restrict Registry permissions to disallow the modification of sensitive Registry keys such as `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NetworkProvider\Order`. |
| [[Modify Authentication Process\|T1556]] | Modify Authentication Process | Restrict Registry permissions to disallow the modification of sensitive Registry keys such as `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NetworkProvider\Order`. |
| [[Server Software Component\|T1505]] | Server Software Component | Consider using Group Policy to configure and block modifications to service and other critical server parameters in the Registry.(Citation: Microsoft System Services Fundamentals) |
| [[Terminal Services DLL\|T1505.005]] | Terminal Services DLL | Consider using Group Policy to configure and block modifications to Terminal Services parameters in the Registry.(Citation: Microsoft System Services Fundamentals) |
| [[Services Registry Permissions Weakness\|T1574.011]] | Services Registry Permissions Weakness | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for system components that may lead to privilege escalation.  |
| [[Disable Windows Event Logging\|T1562.002]] | Disable Windows Event Logging | Ensure proper Registry permissions are in place to prevent adversaries from disabling or interfering logging. The addition of the MiniNT registry key disables Event Viewer.(Citation: def_ev_win_event_logging) |
| [[Clear Network Connection History and Configurations\|T1070.007]] | Clear Network Connection History and Configurations | Protect generated event files and logs that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities. |
| [[Modify Registry\|T1112]] | Modify Registry | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for system components that may lead to privilege escalation. |
| [[Hijack Execution Flow\|T1574]] | Hijack Execution Flow | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for system components that may lead to privilege escalation. |
| [[SIP and Trust Provider Hijacking\|T1553.003]] | SIP and Trust Provider Hijacking | Ensure proper permissions are set for Registry hives to prevent users from modifying keys related to SIP and trust provider components. Components may still be able to be hijacked to suitable functions already present on disk if malicious modifications to Registry keys are not prevented.  |
| [[Boot or Logon Initialization Scripts\|T1037]] | Boot or Logon Initialization Scripts | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for logon scripts that may lead to persistence. |
| [[Subvert Trust Controls\|T1553]] | Subvert Trust Controls | Ensure proper permissions are set for Registry hives to prevent users from modifying keys related to SIP and trust provider components. Components may still be able to be hijacked to suitable functions already present on disk if malicious modifications to Registry keys are not prevented. |
| [[Disable or Modify Tools\|T1562.001]] | Disable or Modify Tools | Ensure proper Registry permissions are in place to prevent adversaries from disabling or interfering with security services. |
| [[Service Stop\|T1489]] | Service Stop | Ensure proper registry permissions are in place to inhibit adversaries from disabling or interfering with critical services. |
| [[Impair Defenses\|T1562]] | Impair Defenses | Ensure proper Registry permissions are in place to prevent adversaries from disabling or interfering with security/logging services. |
| [[Disable or Modify System Firewall\|T1562.004]] | Disable or Modify System Firewall | Ensure proper Registry permissions are in place to prevent adversaries from disabling or modifying firewall settings. |
| [[Code Signing Policy Modification\|T1553.006]] | Code Signing Policy Modification | Ensure proper permissions are set for the Registry to prevent users from modifying keys related to code signing policies. |
| [[Service Registry Permissions Weakness\|T1058]] | Service Registry Permissions Weakness | Ensure proper permissions are set for Registry hives to prevent users from modifying keys for system components that may lead to privilege escalation. |
| [[Time Providers\|T1209]] | Time Providers | Consider using Group Policy to configure and block modifications to W32Time parameters in the Registry. (Citation: Microsoft W32Time May 2017) |
| [[SIP and Trust Provider Hijacking\|T1198]] | SIP and Trust Provider Hijacking | Ensure proper permissions are set for Registry hives to prevent users from modifying keys related to SIP and trust provider components. Components may still be able to be hijacked to suitable functions already present on disk if malicious modifications to Registry keys are not prevented.  |
