---
alias: M1045
---

## M1045

Enforce binary and application integrity with digital signature verification to prevent untrusted code from executing.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Server Software Component\|T1505]] | Server Software Component | Ensure all application component binaries are signed by the correct application developers. |
| [[Malicious Image\|T1204.003]] | Malicious Image | Utilize a trust model such as Docker Content Trust with digital signatures to ensure runtime verification of the integrity and publisher of specific image tags.(Citation: Content trust in Docker)(Citation: Content trust in Azure Container Registry) |
| [[Implant Internal Image\|T1525]] | Implant Internal Image | Several cloud service providers support content trust models that require container images be signed by trusted sources.(Citation: Content trust in Azure Container Registry)(Citation: Content trust in Docker) |
| [[AppleScript\|T1059.002]] | AppleScript | Require that all AppleScript be signed by a trusted developer ID before being executed - this will prevent random AppleScript code from executing.(Citation: applescript signing) This subjects AppleScript code to the same scrutiny as other .app files passing through Gatekeeper. |
| [[Command and Scripting Interpreter\|T1059]] | Command and Scripting Interpreter | Where possible, only permit execution of signed scripts. |
| [[Match Legitimate Name or Location\|T1036.005]] | Match Legitimate Name or Location | Require signed binaries and images. |
| [[Invalid Code Signature\|T1036.001]] | Invalid Code Signature | Require signed binaries. |
| [[PowerShell Profile\|T1546.013]] | PowerShell Profile | Enforce execution of only signed PowerShell scripts. Sign profiles to avoid them from being modified. |
| [[Masquerading\|T1036]] | Masquerading | Require signed binaries. |
| [[Compromise Client Software Binary\|T1554]] | Compromise Client Software Binary | Ensure all application component binaries are signed by the correct application developers. |
| [[Patch System Image\|T1601.001]] | Patch System Image | Many vendors provide digitally signed operating system images to validate the integrity of the software used on their platform.  Make use of this feature where possible in order to prevent and/or detect attempts by adversaries to compromise the system image. (Citation: Cisco IOS Software Integrity Assurance - Deploy Signed IOS) |
| [[Downgrade System Image\|T1601.002]] | Downgrade System Image | Many vendors provide digitally signed operating system images to validate the integrity of the software used on their platform.  Make use of this feature where possible in order to prevent and/or detect attempts by adversaries to compromise the system image. (Citation: Cisco IOS Software Integrity Assurance - Deploy Signed IOS) |
| [[Windows Service\|T1543.003]] | Windows Service | Enforce registration and execution of only legitimately signed service drivers where possible. |
| [[PowerShell\|T1059.001]] | PowerShell | Set PowerShell execution policy to execute only signed scripts. |
| [[SQL Stored Procedures\|T1505.001]] | SQL Stored Procedures | Ensure all application component binaries are signed by the correct application developers.  |
| [[Create or Modify System Process\|T1543]] | Create or Modify System Process | Enforce registration and execution of only legitimately signed service drivers where possible. |
| [[Modify System Image\|T1601]] | Modify System Image | Many vendors provide digitally signed operating system images to validate the integrity of the software used on their platform.  Make use of this feature where possible in order to prevent and/or detect attempts by adversaries to compromise the system image. (Citation: Cisco IOS Software Integrity Assurance - Deploy Signed IOS) |
| [[IIS Components\|T1505.004]] | IIS Components | Ensure IIS DLLs and binaries are signed by the correct application developers. |
| [[LC_LOAD_DYLIB Addition\|T1546.006]] | LC_LOAD_DYLIB Addition | Enforce that all binaries be signed by the correct Apple Developer IDs. |
| [[Transport Agent\|T1505.002]] | Transport Agent | Ensure all application component binaries are signed by the correct application developers.  |
| [[PowerShell Profile\|T1504]] | PowerShell Profile | Enforce execution of only signed PowerShell scripts. Sign profiles to avoid them from being modified.  |
| [[PowerShell\|T1086]] | PowerShell | Set PowerShell execution policy to execute only signed scripts.  |
| [[AppleScript\|T1155]] | AppleScript | Require that all AppleScript be signed by a trusted developer ID before being executed - this will prevent random AppleScript code from executing.(Citation: applescript signing) This subjects AppleScript code to the same scrutiny as other .app files passing through Gatekeeper. |
| [[Application Deployment Software\|T1017]] | Application Deployment Software | If the application deployment system can be configured to deploy only signed binaries, then ensure that the trusted signing certificates are not co-located with the application deployment system and are instead located on a system that cannot be accessed remotely or to which remote access is tightly controlled. |
| [[LSASS Driver\|T1177]] | LSASS Driver | On Windows 8.1 and Server 2012 R2, enable LSA Protection by setting the Registry key <code>HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Lsa\\RunAsPPL</code> to <code>dword:00000001</code>. (Citation: Microsoft LSA Protection Mar 2014) LSA Protection ensures that LSA plug-ins and drivers are only loaded if they are digitally signed with a Microsoft signature and adhere to the Microsoft Security Development Lifecycle (SDL) process guidance. |
| [[LC_LOAD_DYLIB Addition\|T1161]] | LC_LOAD_DYLIB Addition | Enforce that all binaries be signed by the correct Apple Developer IDs. |
