---
alias: M1022
---

## M1022

Restrict access by setting directory and file permissions that are not specific to users or privileged accounts.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Match Legitimate Name or Location\|T1036.005]] | Match Legitimate Name or Location | Use file system access controls to protect folders such as C:\Windows\System32. |
| [[Stored Data Manipulation\|T1565.001]] | Stored Data Manipulation | Ensure least privilege principles are applied to important information resources to reduce exposure to data manipulation risk. |
| [[RC Scripts\|T1037.004]] | RC Scripts | Limit privileges of user accounts so only authorized users can edit the rc.common file. |
| [[Linux and Mac File and Directory Permissions Modification\|T1222.002]] | Linux and Mac File and Directory Permissions Modification | Applying more restrictive permissions to files and directories could prevent adversaries from modifying the access control lists. |
| [[Disable Windows Event Logging\|T1562.002]] | Disable Windows Event Logging | Ensure proper process and file permissions are in place to prevent adversaries from disabling or interfering with logging or deleting or modifying .evtx logging files. Ensure .evtx files, which are located at <code>C:\Windows\system32\Winevt\Logs</code>(Citation: win_xml_evt_log), have the proper file permissions for limited, legitimate access and audit policies for detection.  |
| [[Startup Items\|T1037.005]] | Startup Items | Since StartupItems are deprecated, preventing all users from writing to the <code>/Library/StartupItems</code> directory would prevent any startup items from getting registered. |
| [[Systemd Timers\|T1053.006]] | Systemd Timers | Restrict read/write access to systemd <code>.timer</code> unit files to only select privileged users who have a legitimate need to manage system services. |
| [[Control Panel\|T1218.002]] | Control Panel | Restrict storage and execution of Control Panel items to protected directories, such as <code>C:\Windows</code>, rather than user directories. |
| [[Time Providers\|T1547.003]] | Time Providers | Consider using Group Policy to configure and block additions/modifications to W32Time DLLs. (Citation: Microsoft W32Time May 2017) |
| [[Clear Windows Event Logs\|T1070.001]] | Clear Windows Event Logs | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities. |
| [[Dylib Hijacking\|T1574.004]] | Dylib Hijacking | Set directory access controls to prevent file writes to the search paths for applications, both in the folders where applications are run from and the standard dylib folders. |
| [[Windows File and Directory Permissions Modification\|T1222.001]] | Windows File and Directory Permissions Modification | Applying more restrictive permissions to files and directories could prevent adversaries from modifying the access control lists. |
| [[Network Logon Script\|T1037.003]] | Network Logon Script | Restrict write access to logon scripts to specific administrators. |
| [[SSH Authorized Keys\|T1098.004]] | SSH Authorized Keys | Restrict access to the <code>authorized_keys</code> file. |
| [[Runtime Data Manipulation\|T1565.003]] | Runtime Data Manipulation | Prevent critical business and system processes from being replaced, overwritten, or reconfigured to load potentially malicious code. |
| [[Private Keys\|T1552.004]] | Private Keys | Ensure permissions are properly set on folders containing sensitive private keys to prevent unintended access. Additionally, on Cisco devices, set the `nonexportable` flag during RSA key pair generation.(Citation: cisco_deploy_rsa_keys) |
| [[Proc Memory\|T1055.009]] | Proc Memory | Restrict the permissions on sensitive files such as <code>/proc/[pid]/maps</code> or <code>/proc/[pid]/mem</code>.  |
| [[Path Interception by PATH Environment Variable\|T1574.007]] | Path Interception by PATH Environment Variable | Ensure that proper permissions and directory access control are set to deny users the ability to write files to the top-level directory <code>C:</code> and system directories, such as <code>C:\Windows\</code>, to reduce places where malicious files could be placed for execution. Require that all executables be placed in write-protected directories. |
| [[Indicator Blocking\|T1562.006]] | Indicator Blocking | Ensure event tracers/forwarders (Citation: Microsoft ETW May 2018), firewall policies, and other associated mechanisms are secured with appropriate permissions and access controls. |
| [[XDG Autostart Entries\|T1547.013]] | XDG Autostart Entries | Restrict write access to XDG autostart entries to only select privileged users. |
| [[NTFS File Attributes\|T1564.004]] | NTFS File Attributes | Consider adjusting read and write permissions for NTFS EA, though this should be tested to ensure routine OS operations are not impeded. (Citation: InsiderThreat NTFS EA Oct 2017) |
| [[Launch Agent\|T1543.001]] | Launch Agent | Set group policies to restrict file permissions to the <code>~/launchagents</code> folder.(Citation: piazza launch agent mitigation) |
| [[Path Interception by Search Order Hijacking\|T1574.008]] | Path Interception by Search Order Hijacking | Ensure that proper permissions and directory access control are set to deny users the ability to write files to the top-level directory <code>C:</code> and system directories, such as <code>C:\Windows\</code>, to reduce places where malicious files could be placed for execution. Require that all executables be placed in write-protected directories. |
| [[PowerShell Profile\|T1546.013]] | PowerShell Profile | Making PowerShell profiles immutable and only changeable by certain administrators will limit the ability for adversaries to easily create user level persistence. |
| [[Indicator Removal\|T1070]] | Indicator Removal | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities. |
| [[Hijack Execution Flow\|T1574]] | Hijack Execution Flow | Install software in write-protected locations. Set directory access controls to prevent file writes to the search paths for applications, both in the folders where applications are run from and the standard library folders. |
| [[Masquerading\|T1036]] | Masquerading | Use file system access controls to protect folders such as C:\\Windows\\System32. |
| [[File and Directory Permissions Modification\|T1222]] | File and Directory Permissions Modification | Applying more restrictive permissions to files and directories could prevent adversaries from modifying their access control lists. Additionally, ensure that user settings regarding local and remote symbolic links are properly set or disabled where unneeded.(Citation: create_sym_links) |
| [[SSH Hijacking\|T1563.001]] | SSH Hijacking | Ensure proper file permissions are set and harden system to prevent root privilege escalation opportunities. |
| [[Clear Mailbox Data\|T1070.008]] | Clear Mailbox Data | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities.  |
| [[Sudo and Sudo Caching\|T1548.003]] | Sudo and Sudo Caching | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Clear Persistence\|T1070.009]] | Clear Persistence | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities.  |
| [[Clear Linux or Mac System Logs\|T1070.002]] | Clear Linux or Mac System Logs | Protect generated event files that are stored locally with proper permissions and authentication and limit opportunities for adversaries to increase privileges by preventing Privilege Escalation opportunities. |
| [[Unsecured Credentials\|T1552]] | Unsecured Credentials | Restrict file shares to specific directories with access only to necessary users. |
| [[Systemd Service\|T1543.002]] | Systemd Service | Restrict read/write access to systemd unit files to only select privileged users who have a legitimate need to manage system services. |
| [[Clear Command History\|T1070.003]] | Clear Command History | Preventing users from deleting or writing to certain files can stop adversaries from maliciously altering their <code>~/.bash_history</code> or <code>ConsoleHost_history.txt</code> files. |
| [[Create or Modify System Process\|T1543]] | Create or Modify System Process | Restrict read/write access to system-level process files to only select privileged users who have a legitimate need to manage system services. |
| [[Login Hook\|T1037.002]] | Login Hook | Restrict write access to logon scripts to specific administrators. |
| [[Modify Authentication Process\|T1556]] | Modify Authentication Process | Restrict write access to the `/Library/Security/SecurityAgentPlugins` directory. |
| [[Abuse Elevation Control Mechanism\|T1548]] | Abuse Elevation Control Mechanism | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Impair Defenses\|T1562]] | Impair Defenses | Ensure proper process and file permissions are in place to prevent adversaries from disabling or interfering with security/logging services. |
| [[Unix Shell Configuration Modification\|T1546.004]] | Unix Shell Configuration Modification | Making these files immutable and only changeable by certain administrators will limit the ability for adversaries to easily create user level persistence. |
| [[Data from Cloud Storage\|T1530]] | Data from Cloud Storage | Use access control lists on storage systems and objects. |
| [[Path Interception by Unquoted Path\|T1574.009]] | Path Interception by Unquoted Path | Ensure that proper permissions and directory access control are set to deny users the ability to write files to the top-level directory <code>C:</code> and system directories, such as <code>C:\Windows\</code>, to reduce places where malicious files could be placed for execution. Require that all executables be placed in write-protected directories. |
| [[Data Manipulation\|T1565]] | Data Manipulation | Ensure least privilege principles are applied to important information resources to reduce exposure to data manipulation risk. |
| [[System Services\|T1569]] | System Services | Ensure that high permission level service binaries cannot be replaced or modified by users with a lower permission level. |
| [[Service Execution\|T1569.002]] | Service Execution | Ensure that high permission level service binaries cannot be replaced or modified by users with a lower permission level. |
| [[Boot or Logon Initialization Scripts\|T1037]] | Boot or Logon Initialization Scripts | Restrict write access to logon scripts to specific administrators. |
| [[Service Stop\|T1489]] | Service Stop | Ensure proper process and file permissions are in place to inhibit adversaries from disabling or interfering with critical services. |
| [[Disable or Modify System Firewall\|T1562.004]] | Disable or Modify System Firewall | Ensure proper process and file permissions are in place to prevent adversaries from disabling or modifying firewall settings. |
| [[Exfiltration Over Alternative Protocol\|T1048]] | Exfiltration Over Alternative Protocol | Use access control lists on cloud storage systems and objects.  |
| [[Rename System Utilities\|T1036.003]] | Rename System Utilities | Use file system access controls to protect folders such as C:\Windows\System32. |
| [[Taint Shared Content\|T1080]] | Taint Shared Content | Protect shared folders by minimizing users who have write access. |
| [[SIP and Trust Provider Hijacking\|T1553.003]] | SIP and Trust Provider Hijacking | Restrict storage and execution of SIP DLLs to protected directories, such as C:\\Windows, rather than user directories. |
| [[Disable or Modify Tools\|T1562.001]] | Disable or Modify Tools | Ensure proper process and file permissions are in place to prevent adversaries from disabling or interfering with security services. |
| [[Credentials In Files\|T1552.001]] | Credentials In Files | Restrict file shares to specific directories with access only to necessary users. |
| [[Service Execution\|T1035]] | Service Execution | Also ensure that high permission level service binaries cannot be replaced or modified by users with a lower permission level. |
| [[Time Providers\|T1209]] | Time Providers | Consider using Group Policy to configure and block additions/modifications to W32Time DLLs. (Citation: Microsoft W32Time May 2017) |
| [[NTFS File Attributes\|T1096]] | NTFS File Attributes | Consider adjusting read and write permissions for NTFS EA, though this should be tested to ensure routine OS operations are not impeded. (Citation: InsiderThreat NTFS EA Oct 2017) |
| [[Sudo\|T1169]] | Sudo | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Disabling Security Tools\|T1089]] | Disabling Security Tools | Ensure proper process, Registry, and file permissions are in place to prevent adversaries from disabling or interfering with security services. |
| [[DLL Side-Loading\|T1073]] | DLL Side-Loading | Install software in write-protected locations. |
| [[PowerShell Profile\|T1504]] | PowerShell Profile | Making PowerShell profiles immutable and only changeable by certain administrators will limit the ability for adversaries to easily create user level persistence. |
| [[Credentials In Files|T1081]] | Credentials in Files | Restrict file shares to specific directories with access only to necessary users. |
| [[Indicator Blocking\|T1054]] | Indicator Blocking | Ensure event tracers/forwarders (Citation: Microsoft ETW May 2018), firewall policies, and other associated mechanisms are secured with appropriate permissions and access controls. |
| [[Dylib Hijacking\|T1157]] | Dylib Hijacking | Set directory access controls to prevent file writes to the search paths for applications, both in the folders where applications are run from and the standard dylib folders. |
| [[Systemd Service\|T1501]] | Systemd Service | Restrict read/write access to systemd unit files to only select privileged users who have a legitimate need to manage system services. |
| [[Stored Data Manipulation\|T1492]] | Stored Data Manipulation | Ensure least privilege principles are applied to important information resources to reduce exposure to data manipulation risk. |
| [[Startup Items\|T1165]] | Startup Items | Since StartupItems are deprecated, preventing all users from writing to the <code>/Library/StartupItems</code> directory would prevent any startup items from getting registered. |
| [[Private Keys\|T1145]] | Private Keys | Ensure permissions are properly set on folders containing sensitive private keys to prevent unintended access. |
| [[SIP and Trust Provider Hijacking\|T1198]] | SIP and Trust Provider Hijacking | Restrict storage and execution of SIP DLLs to protected directories, such as C:\\Windows, rather than user directories. |
| [[Clear Command History\|T1146]] | Clear Command History | Preventing users from deleting or writing to certain files can stop adversaries from maliciously altering their <code>~/.bash_history</code> files. |
| [[SSH Hijacking\|T1184]] | SSH Hijacking | Ensure proper file permissions are set and harden system to prevent root privilege escalation opportunities. |
| [[Malicious Shell Modification\|T1156]] | Malicious Shell Modification | Making these files immutable and only changeable by certain administrators will limit the ability for adversaries to easily create user level persistence. |
| [[Control Panel Items\|T1196]] | Control Panel Items | Restrict storage and execution of Control Panel items to protected directories, such as <code>C:\Windows</code>, rather than user directories. |
| [[Runtime Data Manipulation\|T1494]] | Runtime Data Manipulation | Prevent critical business and system processes from being replaced, overwritten, or reconfigured to load potentially malicious code. |
| [[Sudo and Sudo Caching\|T1548.003]] | Sudo and Sudo Caching | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Sudo and Sudo Caching\|T1548.003]] | Sudo and Sudo Caching | The sudoers file should be strictly edited such that passwords are always required and that users can't spawn risky processes as users with higher privilege. |
| [[Plist Modification\|T1547.011]] | Plist Modification | Prevent plist files from being modified by users by making them read-only. |
| [[Plist Modification\|T1150]] | Plist Modification | Prevent plist files from being modified by users by making them read-only. |
| [[DLL Side-Loading\|T1574.002]] | DLL Side-Loading | Install software in write-protected locations. |
| [[SSH Hijacking\|T1184]] | SSH Hijacking | Ensure proper file permissions are set and harden system to prevent root privilege escalation opportunities. |
| [[SSH Hijacking\|T1184]] | SSH Hijacking | Ensure proper file permissions are set and harden system to prevent root privilege escalation opportunities. |
