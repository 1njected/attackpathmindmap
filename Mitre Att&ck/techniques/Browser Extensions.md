---
alias: T1176
---

## T1176

Adversaries may abuse Internet browser extensions to establish persistent access to victim systems. Browser extensions or plugins are small programs that can add functionality and customize aspects of Internet browsers. They can be installed directly or through a browser's app store and generally have access and permissions to everything that the browser can access.(Citation: Wikipedia Browser Extension)(Citation: Chrome Extensions Definition)

Malicious extensions can be installed into a browser through malicious app store downloads masquerading as legitimate extensions, through social engineering, or by an adversary that has already compromised a system. Security can be limited on browser app stores so it may not be difficult for malicious extensions to defeat automated scanners.(Citation: Malicious Chrome Extension Numbers) Depending on the browser, adversaries may also manipulate an extension's update url to install updates from an adversary controlled server or manipulate the mobile configuration file to silently install additional extensions.

Previous to macOS 11, adversaries could silently install browser extensions via the command line using the <code>profiles</code> tool to install malicious <code>.mobileconfig</code> files. In macOS 11+, the use of the <code>profiles</code> tool can no longer install configuration profiles, however <code>.mobileconfig</code> files can be planted and installed with user interaction.(Citation: xorrior chrome extensions macOS)

Once the extension is installed, it can browse to websites in the background, steal all information that a user enters into a browser (including credentials), and be used as an installer for a RAT for persistence.(Citation: Chrome Extension Crypto Miner)(Citation: ICEBRG Chrome Extensions)(Citation: Banker Google Chrome Extension Steals Creds)(Citation: Catch All Chrome Extension)

There have also been instances of botnets using a persistent backdoor through malicious Chrome extensions.(Citation: Stantinko Botnet) There have also been similar examples of extensions being used for command & control.(Citation: Chrome Extension C2 Malware)


### Tactic
- [[Persistence]] (TA0003)

### Platforms
- Linux
- macOS
- Windows

### Permissions Required

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Limit Software Installation\|M1033]] | Limit Software Installation | Only install browser extensions from trusted sources that can be verified. Browser extensions for some browsers can be controlled through Group Policy. Change settings to prevent the browser from installing extensions without sufficient permissions. |
| [[User Training\|M1017]] | User Training | <br />Close out all browser sessions when finished using them to prevent any potentially malicious extensions from continuing to run. |
| [[Execution Prevention\|M1038]] | Execution Prevention | Set a browser extension allow or deny list as appropriate for your security policy. (Citation: Technospot Chrome Extensions GP) |
| [[Audit\|M1047]] | Audit |  Ensure extensions that are installed are the intended ones as many malicious extensions will masquerade as legitimate ones. |
| [[Update Software\|M1051]] | Update Software | Ensure operating systems and browsers are using the most current version.  |

### Sub-techniques


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1176
- Chrome Extension Crypto Miner: https://www.ghacks.net/2017/09/19/first-chrome-extension-with-javascript-crypto-miner-detected/
- xorrior chrome extensions macOS: https://www.xorrior.com/No-Place-Like-Chrome/
- Chrome Extensions Definition: https://developer.chrome.com/extensions
- ICEBRG Chrome Extensions: https://www.icebrg.io/blog/malicious-chrome-extensions-enable-criminals-to-impact-over-half-a-million-users-and-global-businesses
- Malicious Chrome Extension Numbers: https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43824.pdf
- Chrome Extension C2 Malware: https://kjaer.io/extension-malware/
- Catch All Chrome Extension: https://isc.sans.edu/forums/diary/CatchAll+Google+Chrome+Malicious+Extension+Steals+All+Posted+Data/22976/https:/threatpost.com/malicious-chrome-extension-steals-data-posted-to-any-website/128680/)
- Banker Google Chrome Extension Steals Creds: https://isc.sans.edu/forums/diary/BankerGoogleChromeExtensiontargetingBrazil/22722/
- Stantinko Botnet: https://www.welivesecurity.com/2017/07/20/stantinko-massive-adware-campaign-operating-covertly-since-2012/
- Wikipedia Browser Extension: https://en.wikipedia.org/wiki/Browser_extension
