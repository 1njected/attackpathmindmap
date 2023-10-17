---
alias: M1042
---

## M1042

Remove or deny access to unnecessary and potentially vulnerable software to prevent abuse by adversaries.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Re-opened Applications\|T1547.007]] | Re-opened Applications | This feature can be disabled entirely with the following terminal command: <code>defaults write -g ApplePersistence -bool no</code>. |
| [[SSH\|T1021.004]] | SSH | Disable the SSH daemon on systems that do not require it. For macOS ensure Remote Login is disabled under Sharing Preferences.(Citation: Apple Unified Log Analysis Remote Login and Screen Sharing) |
| [[VNC\|T1021.005]] | VNC | Uninstall any VNC server software where not required. |
| [[Exploitation of Remote Services\|T1210]] | Exploitation of Remote Services | Minimize available services to only those that are necessary. |
| [[Visual Basic\|T1059.005]] | Visual Basic | Turn off or restrict access to unneeded VB components. |
| [[Wordlist Scanning\|T1595.003]] | Wordlist Scanning | Remove or disable access to any systems, resources, and infrastructure that are not explicitly required to be available externally. |
| [[Windows Remote Management\|T1021.006]] | Windows Remote Management | Disable the WinRM service. |
| [[Inter-Process Communication\|T1559]] | Inter-Process Communication | Registry keys specific to Microsoft Office feature control security can be set to disable automatic DDE/OLE execution. (Citation: Microsoft DDE Advisory Nov 2017)(Citation: BleepingComputer DDE Disabled in Word Dec 2017)(Citation: GitHub Disable DDEAUTO Oct 2017) Microsoft also created, and enabled by default, Registry keys to completely disable DDE execution in Word and Excel.(Citation: Microsoft ADV170021 Dec 2017) |
| [[Run Virtual Instance\|T1564.006]] | Run Virtual Instance | Disable Hyper-V if not necessary within a given environment. |
| [[LLMNR／NBT-NS Poisoning and SMB Relay\|T1557.001]] | LLMNR／NBT-NS Poisoning and SMB Relay | Disable LLMNR and NetBIOS in local computer security settings or by group policy if they are not needed within an environment. (Citation: ADSecurity Windows Secure Baseline) |
| [[Network Service Discovery\|T1046]] | Network Service Discovery | Ensure that unnecessary ports and services are closed to prevent risk of discovery and potential exploitation. |
| [[Steal or Forge Authentication Certificates\|T1649]] | Steal or Forge Authentication Certificates | Consider disabling old/dangerous authentication protocols (e.g. NTLM), as well as unnecessary certificate features, such as potentially vulnerable AD CS web and other enrollment server roles.(Citation: SpecterOps Certified Pre Owned) |
| [[Email Forwarding Rule\|T1114.003]] | Email Forwarding Rule | Consider disabling external email forwarding.(Citation: Microsoft BEC Campaign) |
| [[Adversary-in-the-Middle\|T1557]] | Adversary-in-the-Middle | Disable legacy network protocols that may be used   to intercept network traffic if applicable, especially those that are not needed within an environment. |
| [[Exfiltration over USB\|T1052.001]] | Exfiltration over USB | Disable Autorun if it is unnecessary. (Citation: Microsoft Disable Autorun) Disallow or restrict removable media at an organizational policy level if they are not required for business operations. (Citation: TechNet Removable Media Control) |
| [[Mark-of-the-Web Bypass\|T1553.005]] | Mark-of-the-Web Bypass | Consider disabling auto-mounting of disk image files (i.e., .iso, .img, .vhd, and .vhdx). This can be achieved by modifying the Registry values related to the Windows Explorer file associations in order to disable the automatic Explorer "Mount and Burn" dialog for these file extensions. Note: this will not deactivate the mount functionality itself.(Citation: GitHub MOTW) |
| [[Server Software Component\|T1505]] | Server Software Component | Consider disabling software components from servers when possible to prevent abuse by adversaries.(Citation: ITSyndicate Disabling PHP functions) |
| [[PowerShell\|T1059.001]] | PowerShell | It may be possible to remove PowerShell from systems when not needed, but a review should be performed to assess the impact to an environment, since it could be in use for many legitimate purposes and administrative functions.<br /><br />Disable/restrict the WinRM Service to help prevent uses of PowerShell for remote execution. |
| [[Odbcconf\|T1218.008]] | Odbcconf | Odbcconf.exe may not be necessary within a given environment. |
| [[Replication Through Removable Media\|T1091]] | Replication Through Removable Media | Disable Autorun if it is unnecessary. (Citation: Microsoft Disable Autorun) Disallow or restrict removable media at an organizational policy level if it is not required for business operations. (Citation: TechNet Removable Media Control) |
| [[Office Application Startup\|T1137]] | Office Application Startup | Follow Office macro security best practices suitable for your environment. Disable Office VBA macros from executing.<br /><br />Disable Office add-ins. If they are required, follow best practices for securing them by requiring them to be signed and disabling user notification for allowing add-ins. For some add-ins types (WLL, VBA) additional mitigation is likely required as disabling add-ins in the Office Trust Center does not disable WLL nor does it prevent VBA code from executing. (Citation: MRWLabs Office Persistence Add-ins) |
| [[Screensaver\|T1546.002]] | Screensaver | Use Group Policy to disable screensavers if they are unnecessary.(Citation: TechNet Screensaver GP) |
| [[Command and Scripting Interpreter\|T1059]] | Command and Scripting Interpreter | Disable or remove any unnecessary or unused shells or interpreters. |
| [[Distributed Component Object Model\|T1021.003]] | Distributed Component Object Model | Consider disabling DCOM through Dcomcnfg.exe.(Citation: Microsoft Disable DCOM) |
| [[Remote Desktop Protocol\|T1021.001]] | Remote Desktop Protocol | Disable the RDP service if it is unnecessary. |
| [[Windows Credential Manager\|T1555.004]] | Windows Credential Manager | Consider enabling the “Network access: Do not allow storage of passwords and credentials for network authentication” setting that will prevent network credentials from being stored by the Credential Manager.(Citation: Microsoft Network access Credential Manager) |
| [[Communication Through Removable Media\|T1092]] | Communication Through Removable Media | Disable Autoruns if it is unnecessary.(Citation: Microsoft Disable Autorun) |
| [[RDP Hijacking\|T1563.002]] | RDP Hijacking | Disable the RDP service if it is unnecessary. |
| [[Mavinject\|T1218.013]] | Mavinject | Consider removing mavinject.exe if Microsoft App-V is not used within a given environment. |
| [[Remote Service Session Hijacking\|T1563]] | Remote Service Session Hijacking | Disable the remote service (ex: SSH, RDP, etc.) if it is unnecessary. |
| [[SSH Authorized Keys\|T1098.004]] | SSH Authorized Keys | Disable SSH if it is not necessary on a host or restrict SSH access for specific users/groups using <code>/etc/ssh/sshd_config</code>. |
| [[ARP Cache Poisoning\|T1557.002]] | ARP Cache Poisoning | Consider disabling updating the ARP cache on gratuitous ARP replies. |
| [[Verclsid\|T1218.012]] | Verclsid | Consider removing verclsid.exe if it is not necessary within a given environment. |
| [[Mshta\|T1218.005]] | Mshta | Mshta.exe may not be necessary within a given environment since its functionality is tied to older versions of Internet Explorer that have reached end of life. |
| [[SSH Hijacking\|T1563.001]] | SSH Hijacking | Ensure that agent forwarding is disabled on systems that do not explicitly require this feature to prevent misuse. (Citation: Symantec SSH and ssh-agent) |
| [[External Remote Services\|T1133]] | External Remote Services | Disable or block remotely available services that may be unnecessary. |
| [[Msiexec\|T1218.007]] | Msiexec | Consider disabling the <code>AlwaysInstallElevated</code> policy to prevent elevated execution of Windows Installer packages.(Citation: Microsoft AlwaysInstallElevated 2018) |
| [[VBA Stomping\|T1564.007]] | VBA Stomping | Turn off or restrict access to unneeded VB components.(Citation: Microsoft Disable VBA Jan 2020) |
| [[JavaScript\|T1059.007]] | JavaScript | Turn off or restrict access to unneeded scripting components. |
| [[Container Administration Command\|T1609]] | Container Administration Command | Remove unnecessary tools and software from containers. |
| [[InstallUtil\|T1218.004]] | InstallUtil | InstallUtil may not be necessary within a given environment. |
| [[MSBuild\|T1127.001]] | MSBuild | MSBuild.exe may not be necessary within an environment and should be removed if not being used. |
| [[Exfiltration Over Bluetooth\|T1011.001]] | Exfiltration Over Bluetooth | Disable Bluetooth in local computer security settings or by group policy if it is not needed within an environment. |
| [[MMC\|T1218.014]] | MMC | MMC may not be necessary within a given environment since it is primarily used by system administrators, not regular users or clients.  |
| [[Cloud Instance Metadata API\|T1552.005]] | Cloud Instance Metadata API | Disable unnecessary metadata services and restrict or disable insecure versions of metadata services that are in use to prevent adversary access.(Citation: Amazon AWS IMDS V2) |
| [[Emond\|T1546.014]] | Emond | Consider disabling emond by removing the [Launch Daemon](https://attack.mitre.org/techniques/T1543/004) plist file. |
| [[Office Template Macros\|T1137.001]] | Office Template Macros | Follow Office macro security best practices suitable for your environment. Disable Office VBA macros from executing.<br /><br />Disable Office add-ins. If they are required, follow best practices for securing them by requiring them to be signed and disabling user notification for allowing add-ins. For some add-ins types (WLL, VBA) additional mitigation is likely required as disabling add-ins in the Office Trust Center does not disable WLL nor does it prevent VBA code from executing. (Citation: MRWLabs Office Persistence Add-ins)<br /> |
| [[Web Shell\|T1505.003]] | Web Shell | Consider disabling functions from web technologies such as PHP’s <code>eval()</code> that may be abused for web shells.(Citation: ITSyndicate Disabling PHP functions) |
| [[Traffic Signaling\|T1205]] | Traffic Signaling | Disable Wake-on-LAN if it is not needed within an environment. |
| [[System Binary Proxy Execution\|T1218]] | System Binary Proxy Execution | Many native binaries may not be necessary within a given environment. |
| [[Exfiltration Over Physical Medium\|T1052]] | Exfiltration Over Physical Medium | Disable Autorun if it is unnecessary. (Citation: Microsoft Disable Autorun) Disallow or restrict removable media at an organizational policy level if they are not required for business operations. (Citation: TechNet Removable Media Control) |
| [[Regsvcs／Regasm\|T1218.009]] | Regsvcs／Regasm | Regsvcs and Regasm may not be necessary within a given environment. |
| [[Template Injection\|T1221]] | Template Injection | Consider disabling Microsoft Office macros/active content to prevent the execution of malicious payloads in documents (Citation: Microsoft Disable Macros), though this setting may not mitigate the [Forced Authentication](https://attack.mitre.org/techniques/T1187) use for this technique. |
| [[Dynamic Data Exchange\|T1559.002]] | Dynamic Data Exchange | Registry keys specific to Microsoft Office feature control security can be set to disable automatic DDE/OLE execution. (Citation: Microsoft DDE Advisory Nov 2017)(Citation: BleepingComputer DDE Disabled in Word Dec 2017)(Citation: GitHub Disable DDEAUTO Oct 2017) Microsoft also created, and enabled by default, Registry keys to completely disable DDE execution in Word and Excel.(Citation: Microsoft ADV170021 Dec 2017) |
| [[Downgrade Attack\|T1562.010]] | Downgrade Attack | Consider removing previous versions of tools that are unnecessary to the environment when possible. |
| [[Additional Email Delegate Permissions\|T1098.002]] | Additional Email Delegate Permissions | If email delegation is not required, disable it. In Google Workspace this can be accomplished through the Google Admin console.(Citation: Gmail Delegation) |
| [[Trusted Developer Utilities Proxy Execution\|T1127]] | Trusted Developer Utilities Proxy Execution | Specific developer utilities may not be necessary within a given environment and should be removed if not used. |
| [[Escape to Host\|T1611]] | Escape to Host | Remove unnecessary tools and software from containers. |
| [[CMSTP\|T1218.003]] | CMSTP | CMSTP.exe may not be necessary within a given environment (unless using it for VPN connection installation). |
| [[Windows Remote Management\|T1028]] | Windows Remote Management | Disable the WinRM service. |
| [[Regsvcs／Regasm\|T1121]] | Regsvcs／Regasm | Regsvcs and Regasm may not be necessary within a given environment. |
| [[Dynamic Data Exchange\|T1173]] | Dynamic Data Exchange | Registry keys specific to Microsoft Office feature control security can be set to disable automatic DDE/OLE execution. (Citation: Microsoft DDE Advisory Nov 2017) (Citation: BleepingComputer DDE Disabled in Word Dec 2017) (Citation: GitHub Disable DDEAUTO Oct 2017) Microsoft also created, and enabled by default, Registry keys to completely disable DDE execution in Word and Excel. (Citation: Microsoft ADV170021 Dec 2017) |
| [[Re-opened Applications\|T1164]] | Re-opened Applications | This feature can be disabled entirely with the following terminal command: <code>defaults write -g ApplePersistence -bool no</code>. |
| [[LLMNR／NBT-NS Poisoning and Relay\|T1171]] | LLMNR／NBT-NS Poisoning and Relay | Disable LLMNR and NetBIOS in local computer security settings or by group policy if they are not needed within an environment. (Citation: ADSecurity Windows Secure Baseline) |
| [[Emond\|T1519]] | Emond | Consider disabling emond by removing the [Launch Daemon](https://attack.mitre.org/techniques/T1160) plist file. |
| [[PowerShell\|T1086]] | PowerShell | It may be possible to remove PowerShell from systems when not needed, but a review should be performed to assess the impact to an environment, since it could be in use for many legitimate purposes and administrative functions.<br /><br />Disable/restrict the WinRM Service to help prevent uses of PowerShell for remote execution. |
| [[SSH Hijacking\|T1184]] | SSH Hijacking | Ensure that agent forwarding is disabled on systems that do not explicitly require this feature to prevent misuse. (Citation: Symantec SSH and ssh-agent) |
| [[CMSTP\|T1191]] | CMSTP | CMSTP.exe may not be necessary within a given environment (unless using it for VPN connection installation). |
| [[Mshta\|T1170]] | Mshta | Mshta.exe may not be necessary within a given environment since its functionality is tied to older versions of Internet Explorer that have reached end of life. |
| [[Remote Desktop Protocol\|T1076]] | Remote Desktop Protocol | Disable the RDP service if it is unnecessary. |
| [[InstallUtil\|T1118]] | InstallUtil | InstallUtil may not be necessary within a given environment. |
| [[Screensaver\|T1180]] | Screensaver | Use Group Policy to disable screensavers if they are unnecessary. (Citation: TechNet Screensaver GP) |
