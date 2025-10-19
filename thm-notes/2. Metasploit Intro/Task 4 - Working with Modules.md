
- Enter the context of a module using `use` followed by the module name
	- You will have to set **parameters**
	- Based on the module, additional or different parameters will need to be set.
	- **GOOD PRACTICE**: use `show options` command to list required parameters


Setting parameters syntax:
- `set PARAMETER_NAME VALUE`


- `msfconsole prompt`
	- `a context prompt`: once you have decided what module to use you will be able to use context-specific commands
	- `meterpreter prompt`: important payload -> meterpreter agent was loaded to the target system and connected back to you.
	- `shell on the target system`: once exploit is completed you may have access to a command shell on the target system.


### Often used Parameters:
-----
**RHOSTS**: 
- REMOTE HOST, IP address of target system
- single address or network range (CIDR)
- also can use .txt file where targets are listed


**RPORT**:
- REMOTE PORT, the port on the target system the vulnerable application is running on.


**PAYLOAD:**
- Payload that you will use on the exploit


**LHOST:**
- Localhost, the attacking machine (IP address)


**LPORT:**
- Local port
- Port that you will use for the reverse shell to connect back to
- Port on `your attacking machine`
- Can set it to any port not being used by any other application


**SESSION**:
- Each connection established to the target system using Metasploit will have a session ID. 
- Used with post-exploitation modules that will connect to the target system using an existing connection.


Override set parameters using `unset` or `unsetall`

Global Parameters will be set (remain even after context changes) using `gset and gunset`



### Using Modules
---
Once all module parameters are set...
- Launch the module using `exploit` command
- You can also use `run` command -> alias for the exploit command.
- `exploit -z` invokes a background session
- `background` command -> to background session prompt

Viewing Sessions:
- `sessions` -> to list all active sessions
- `sessions -i <session number>` to enter a session context.



**Questions**
-----------------
(1) How would you set the LPORT value to `6666`?
- set LPORT 6666

(2) How would you set the global value for RHOSTS to `10.10.19.23`?
- setg RHOSTS 10.10.19.23

(3) What command would you use to clear a set payload?
- unset PAYLOAD

(4) What command do you use to proceed with the exploitation phase?
- exploit



