
**SCRIPTING**: Writing and executing a series of commands contained in a **text file** aka a **script**
- Goal: Automate tasks that are generally done manually within PowerShell

**Analogy**: 
- Giving the computer a to-do list, where each line in the script is a task that the computer will carry out automatically
- Saves time
- Reduces Error propagation
- Allows complex tasks to be carried out (**not manually**)

**BLUE**
- Log Analysis
- Anomalies
- Extracting indicators of compromise (IOCS)
- Used to reverse engineer malicious code
- Automate scanning of systems for **signs of intrusion**

**RED**
- Enumeration
- Executing remote commands
- Crafting obfuscated scripts to bypass defenses
- Simulates attacks and tests systems resilience

**INVOKE-COMMAND**
-`Invoke-Command` cmdlet
- useful for executing commands on **remote systems**
- Combined with scripting, automation of tasks across **multiple machines**
- Used to execute **payloads / commands** on target systems 

`Get-Help Invoke-Command`
- Examples 1 - **Run a script on a server**
- `Invoke-Command -FilePath "./path" -ComputerName "Name"`
-     The FilePath parameter specifies a script that is located on the local computer. The script runs on the remote computer and the results are returned to the local computer.

- Examples 2 - **Run a command on a remote server**
- `Invoke-Command -ComputerName Name -ScriptBlock {Get-...}`

**Question**
----------------
What is the syntax to execute the command Get-Service on a remote computer named "RoyalFortune"? Assume you don't need to provide credentials to establish the connection. 
- `Invoke-Command -ComputerName RoyalFortune .ScriptBlock {Get-Service}`

