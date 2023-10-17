---
alias: T1003.005
---

## T1003.005

Adversaries may attempt to access cached domain credentials used to allow authentication to occur in the event a domain controller is unavailable.(Citation: Microsoft - Cached Creds)

On Windows Vista and newer, the hash format is DCC2 (Domain Cached Credentials version 2) hash, also known as MS-Cache v2 hash.(Citation: PassLib mscache) The number of default cached credentials varies and can be altered per system. This hash does not allow pass-the-hash style attacks, and instead requires [Password Cracking](https://attack.mitre.org/techniques/T1110/002) to recover the plaintext password.(Citation: ired mscache)

With SYSTEM access, the tools/utilities such as [Mimikatz](https://attack.mitre.org/software/S0002), [Reg](https://attack.mitre.org/software/S0075), and secretsdump.py can be used to extract the cached credentials.

Note: Cached credentials for Windows Vista are derived using PBKDF2.(Citation: PassLib mscache)


### Tactic
- [[Credential Access]] (TA0006)

### Platforms
- Windows

### Permissions Required
- SYSTEM

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[User Training\|M1017]] | User Training | Limit credential overlap across accounts and systems by training users and administrators not to use the same password for multiple accounts. |
| [[Operating System Configuration\|M1028]] | Operating System Configuration | Consider limiting the number of cached credentials (HKLM\SOFTWARE\Microsoft\Windows NT\Current Version\Winlogon\cachedlogonscountvalue)(Citation: Tilbury Windows Credentials) |
| [[Password Policies\|M1027]] | Password Policies | Ensure that local administrator accounts have complex, unique passwords across all systems on the network. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | Do not put user or admin domain accounts in the local administrator groups across systems unless they are tightly controlled, as this is often equivalent to having a local administrator account with the same password on all systems. Follow best practices for design and administration of an enterprise network to limit privileged account use across administrative tiers. |
| [[Active Directory Configuration\|M1015]] | Active Directory Configuration | Consider adding users to the "Protected Users" Active Directory security group. This can help limit the caching of users' plaintext credentials.(Citation: Microsoft Protected Users Security Group) |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1003/005
- Microsoft - Cached Creds: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/hh994565(v%3Dws.11)
- PassLib mscache: https://passlib.readthedocs.io/en/stable/lib/passlib.hash.msdcc2.html
- ired mscache: https://ired.team/offensive-security/credential-access-and-credential-dumping/dumping-and-cracking-mscash-cached-domain-credentials
- Powersploit: https://github.com/mattifestation/PowerSploit
