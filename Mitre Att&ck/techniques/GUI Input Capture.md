---
alias: T1056.002
---

## T1056.002

Adversaries may mimic common operating system GUI components to prompt users for credentials with a seemingly legitimate prompt. When programs are executed that need additional privileges than are present in the current user context, it is common for the operating system to prompt the user for proper credentials to authorize the elevated privileges for the task (ex: [Bypass User Account Control](https://attack.mitre.org/techniques/T1548/002)).

Adversaries may mimic this functionality to prompt users for credentials with a seemingly legitimate prompt for a number of reasons that mimic normal usage, such as a fake installer requiring additional access or a fake malware removal suite.(Citation: OSX Malware Exploits MacKeeper) This type of prompt can be used to collect credentials via various languages such as [AppleScript](https://attack.mitre.org/techniques/T1059/002)(Citation: LogRhythm Do You Trust Oct 2014)(Citation: OSX Keydnap malware)(Citation: Spoofing credential dialogs) and [PowerShell](https://attack.mitre.org/techniques/T1059/001).(Citation: LogRhythm Do You Trust Oct 2014)(Citation: Enigma Phishing for Credentials Jan 2015)(Citation: Spoofing credential dialogs) On Linux systems adversaries may launch dialog boxes prompting users for credentials from malicious shell scripts or the command line (i.e. [Unix Shell](https://attack.mitre.org/techniques/T1059/004)).(Citation: Spoofing credential dialogs) 


### Tactic
- [[Collection]] (TA0009)
- [[Credential Access]] (TA0006)

### Platforms
- macOS
- Windows
- Linux

### Permissions Required
- User

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Use user training as a way to bring awareness and raise suspicion for potentially malicious events and dialog boxes (ex: Office documents prompting for credentials). |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1056/002
- OSX Malware Exploits MacKeeper: https://baesystemsai.blogspot.com/2015/06/new-mac-os-malware-exploits-mackeeper.html
- LogRhythm Do You Trust Oct 2014: https://logrhythm.com/blog/do-you-trust-your-computer/
- OSX Keydnap malware: https://www.welivesecurity.com/2016/07/06/new-osxkeydnap-malware-hungry-credentials/
- Spoofing credential dialogs: https://embracethered.com/blog/posts/2021/spoofing-credential-dialogs/
- Enigma Phishing for Credentials Jan 2015: https://enigma0x3.net/2015/01/21/phishing-for-credentials-if-you-want-it-just-ask/
