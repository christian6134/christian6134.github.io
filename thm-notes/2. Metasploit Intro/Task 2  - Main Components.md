
`msfconsole`  
- Main interface to interact with different **modules**

`Modules`
- Small components within the Framework that are **built to perform a specific task**
	- Exploiting a vulnerability
	- Scanning a target
	- Performing brute-force attacks


**Some Clarifications:**
- **Exploit**: A piece of code that uses a vulnerability present on the target system.
- **Vulnerability**: A design, coding or logic flaw affecting the target system. Exploitation of a vulnerability can result in **disclosing confidential information**
	- Allows the attacker to execute code on the target system 
- **Payload:** 
	- An exploit will take advantage of a vulnerability.
	- Payloads are the code that will run on the target system
		- Results -> Gaining access, reading confidential information.


**Auxiliary**
- Any supporting module such as **scanners, crawlers and fuzzers**.


**Encoders**
- Allow you to encode the exploit and payload.
	- Hope that a signature-based antivirus will miss them


**Signature-Based Antivirus / Security**:
- Contain a database of known threats
- Detect threats by comparing suspicious files to the database
- Raise alert with matches


**Evasion**:
- Encoders will encode the payload -> Not considered a direct attempt to evade antivirus software.
- **Evasion** modules will try that, with more or less success.


**NOPs (No operation):**
- Do nothing literally
- `0x90` on Intel x86 CPU family.
- Used as a buffer to achieve consistent payload sizes.


**Payloads:**
- Exploits leverage a vulnerability on the target system.
- To achieve the desired result we will need a payload.
- **Examples**: 
	- Getting a shell
	- Loading malware or backdoor to target system
	- Running a command
- Ability to send different payloads that can open shells on target systems


**4 Directories under the Payloads:**
- **Adapters**: 
	- Wraps single payloads to convert them into different formats
	- Example: Normal single payload wrapped inside a Powershell adapter, which will make a single powershell command execute the payload

- **Singles:** Self-contained payloads (add user, launch notepad) that do not need to download an additional component to run

- **Stagers:** Responsible for **setting up a connection channel** between Metasploit and target system
	- Useful when working with Staged Payloads
	- Staged payloads will first upload a stager on the target system then download the rest of the payload
	- Initial size of payload will be relatively small

**Stages:**
- Downloaded by stager, allow larger sized payloads


`generic/shell_reverse_tcp`
	- Inline(Single) payload, indicated by `_` between shell and reverse

`windows/x64/shell/reverse_tcp`
	- Staged payload as indicated by the `/` between shell and reverse



**Post**: 
- Useful on the final stage of penetration testing


### Questions
----
-  What is the name of the code taking advantage of a flaw on the target system
- **Exploit**

-  What is the name of the code that runs on the target system to achieve the attacker's goal?
- **Payload**

- What are self-contained payloads called?
  - **Singles**

- Is "windows/x64/pingback_reverse_tcp" among singles or stage payloads
- **Singles**
- 

