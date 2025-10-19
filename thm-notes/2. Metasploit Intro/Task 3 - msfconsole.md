
`METASPLOIT` console can be used just like a regular command-line shell.
	`ls`
	`tab completion`
	`ping`
	`clear`
	`history
	`help set`
	`use` ...`exploit`
	`show options`
	`info`
	`search`



**Nuances**:
- `msfconsole` is managed by context
- unless set as a global variable, all parameter settings will be **LOST** if you change the module.


**Define {Session}**:
- Existing connection to the target system that the post-exploitation module will use.


**Exploit rankings (based on reliability)**
- https://github.com/rapid7/metasploit-framework/wiki/Exploit-Ranking


**Questions**:
- How would you search for a module related to Apache?
- `search apache`

- `Who provided the axuiliary/scanner/ssh/ssh_login` Module?
- `info axuiliary/scanner/ssh/ssh_login``
- **Answer: todb**


