---
alias: T1543.002
---

## T1543.002

Adversaries may create or modify systemd services to repeatedly execute malicious payloads as part of persistence. Systemd is a system and service manager commonly used for managing background daemon processes (also known as services) and other system resources.(Citation: Linux man-pages: systemd January 2014) Systemd is the default initialization (init) system on many Linux distributions replacing legacy init systems, including SysVinit and Upstart, while remaining backwards compatible.  

Systemd utilizes unit configuration files with the `.service` file extension to encode information about a service's process. By default, system level unit files are stored in the `/systemd/system` directory of the root owned directories (`/`). User level unit files are stored in the `/systemd/user` directories of the user owned directories (`$HOME`). (Citation: lambert systemd 2022) 

Service unit files use the following directives to execute system commands:(Citation: freedesktop systemd.service)  

* `ExecStart`, `ExecStartPre`, and `ExecStartPost` directives cover execution of commands when a service is started manually by `systemctl`, or on system start if the service is set to automatically start.
* `ExecReload` directive covers when a service restarts. 
* `ExecStop`, `ExecStopPre`, and `ExecStopPost` directives cover when a service is stopped.  

Adversaries may abuse systemd functionality to establish persistent access to victim systems by creating and/or modifying service unit files systemd uses upon reboot or starting a service.(Citation: Anomali Rocke March 2019) Adversaries may also place symbolic links in these directories, enabling systemd to find these payloads regardless of where they reside on the filesystem.

The `.service` file’s `User` directive can be used to run service as a specific user, which could result in privilege escalation based on specific user/group permissions.(Citation: Rapid7 Service Persistence 22JUNE2016) 


### Tactic
- [[Persistence]] (TA0003)
- [[Privilege Escalation]] (TA0004)

### Platforms
- Linux

### Permissions Required
- User
- root

### Mitigations

| ID | Name | Description |
| --- | --- | --- |
| [[Limit Software Installation\|M1033]] | Limit Software Installation | Restrict software installation to trusted repositories only and be cautious of orphaned software packages. |
| [[User Account Management\|M1018]] | User Account Management | Limit user access to system utilities such as `systemctl` to only users who have a legitimate need. |
| [[Restrict File and Directory Permissions\|M1022]] | Restrict File and Directory Permissions | Restrict read/write access to systemd unit files to only select privileged users who have a legitimate need to manage system services. |
| [[Privileged Account Management\|M1026]] | Privileged Account Management | The creation and modification of systemd service unit files is generally reserved for administrators such as the Linux root user and other users with superuser privileges.  |


---
### References

- mitre-attack: https://attack.mitre.org/techniques/T1543/002
- Anomali Rocke March 2019: https://www.anomali.com/blog/rocke-evolves-its-arsenal-with-a-new-malware-family-written-in-golang
- freedesktop systemd.service: https://www.freedesktop.org/software/systemd/man/systemd.service.html
- Linux man-pages: systemd January 2014: http://man7.org/linux/man-pages/man1/systemd.1.html
- Berba hunting linux systemd: https://pberba.github.io/security/2022/01/30/linux-threat-hunting-for-persistence-systemd-timers-cron/
- Rapid7 Service Persistence 22JUNE2016: https://www.rapid7.com/db/modules/exploit/linux/local/service_persistence
- lambert systemd 2022: https://redcanary.com/blog/attck-t1501-understanding-systemd-service-persistence/
