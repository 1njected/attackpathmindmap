---
alias: M1039
---

## M1039

Prevent modification of environment variables by unauthorized users and groups.


### Techniques Addressed by Mitigation

| ID | Name | Description |
| --- | --- | --- |
| [[Impair Command History Logging\|T1562.003]] | Impair Command History Logging | Prevent users from changing the <code>HISTCONTROL</code>, <code>HISTFILE</code>, and <code>HISTFILESIZE</code> environment variables. (Citation: Securing bash history) |
| [[Clear Command History\|T1070.003]] | Clear Command History | Making the environment variables associated with command history read only may ensure that the history is preserved.(Citation: Securing bash history) |
| [[Clear Command History\|T1146]] | Clear Command History | Making the associated environment variables read only can make sure that the history is preserved.(Citation: Securing bash history) |
| [[HISTCONTROL\|T1148]] | HISTCONTROL | Prevent users from changing the <code>HISTCONTROL</code> environment variable. (Citation: Securing bash history) |
| [[Impair Command History Logging\|T1562.003]] | Impair Command History Logging | Prevent users from changing the <code>HISTCONTROL</code> environment variable. (Citation: Securing bash history) |
