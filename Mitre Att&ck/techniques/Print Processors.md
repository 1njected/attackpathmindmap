---
alias: T1547.012
---

## T1547.012

Adversaries may abuse print processors to run malicious DLLs during system boot for persistence and/or privilege escalation. Print processors are DLLs that are loaded by the print spooler service, spoolsv.exe, during boot. 

Adversaries may abuse the print spooler service by adding print processors that load malicious DLLs at startup. A print processor can be installed through the <code>AddPrintProcessor</code> API call with an account that has <code>SeLoadDriverPrivilege</code> enabled. Alternatively, a print processor can be registered to the print spooler service by adding the <code>HKLM\SYSTEM\\[CurrentControlSet or ControlSet001]\Control\Print\Environments\\[Windows architecture: e.g., Windows x64]\Print Processors\\[user defined]\Driver</code> Registry key that points to the DLL. For the print processor to be correctly installed, it must be located in the system print-processor directory that can be found with the <code>GetPrintProcessorDirectory</code> API call.(Citation: Microsoft AddPrintProcessor May 2018) After the print processors are installed, the print spooler service, which starts during boot, must be restarted in order for them to run.(Citation: ESET PipeMon May 2020) The print spooler service runs under SYSTEM level permissions, therefore print processors installed by an adversary may run under elevated privileges.


### Tactic
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Windows

### Permissions Required
- Administrator
- SYSTEM

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Account Management\|M1018]] | User Account Management | Limit user accounts that can load or unload device drivers by disabling <code>SeLoadDriverPrivilege</code>. |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1547/012
- Microsoft AddPrintProcessor May 2018: https://docs.microsoft.com/en-us/windows/win32/printdocs/addprintprocessor
- ESET PipeMon May 2020: https://www.welivesecurity.com/2020/05/21/no-game-over-winnti-group/
