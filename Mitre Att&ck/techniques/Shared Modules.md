---
alias: T1129
---

## T1129

Adversaries may execute malicious payloads via loading shared modules. The Windows module loader can be instructed to load DLLs from arbitrary local paths and arbitrary Universal Naming Convention (UNC) network paths. This functionality resides in NTDLL.dll and is part of the Windows [Native API](https://attack.mitre.org/techniques/T1106) which is called from functions like <code>CreateProcess</code>, <code>LoadLibrary</code>, etc. of the Win32 API.(Citation: Wikipedia Windows Library Files)

The module loader can load DLLs:

* via specification of the (fully-qualified or relative) DLL pathname in the IMPORT directory;
    
* via EXPORT forwarded to another DLL, specified with (fully-qualified or relative) pathname (but without extension);
    
* via an NTFS junction or symlink program.exe.local with the fully-qualified or relative pathname of a directory containing the DLLs specified in the IMPORT directory or forwarded EXPORTs;
    
* via <code>&#x3c;file name="filename.extension" loadFrom="fully-qualified or relative pathname"&#x3e;</code> in an embedded or external "application manifest". The file name refers to an entry in the IMPORT directory or a forwarded EXPORT.

Adversaries may use this functionality as a way to execute arbitrary payloads on a victim system. For example, malware may execute share modules to load additional components or features.


### Tactic
- [[Execution]] (TA0002)

### Platforms
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Execution Prevention\|M1038]] | Execution Prevention | Identify and block potentially malicious software executed through this technique by using application control tools capable of preventing unknown DLLs from being loaded. |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1129
- Wikipedia Windows Library Files: https://en.wikipedia.org/wiki/Microsoft_Windows_library_files
