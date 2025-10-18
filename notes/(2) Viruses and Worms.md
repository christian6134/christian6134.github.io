
# 2.4.2 Viruses and Worms

*How does the virus start?*
- Requires some form of intervention
- Needs you to execute a program

*What does the virus do?*
- Reproduces through file systems or the network
- May or may not cause problems
- Most common from a user's perspective


##### Virus Types
-----
Program viruses
- A part of the application

Boot sector viruses
- Who needs an OS?

Script Viruses
- Operating system and browser-based

Macro viruses
- Common in Microsoft Office


##### Fileless virus
------
Never writes any software or malicious code to storage drives.
- A `stealth attack`
- Avoids anti-virus software
- Operates within `memory` does not install in `a file or application`

Example:
- User clicks on a malicious link
- User is sent to a website set up to exploit a vulnerability on the operating system
-  Launches powershell and downloads payload in RAM


#### Worms 
-----
Malware that self-replicates
- Doesn't need user intervention
- Uses the network as a transmission medium
- Self-propagates and spreads quickly

*Mitigations?*
- IDS/IPS can mitigate many worm infections
- Doesn't help much once the worm is inside.

*What is Worm v Virus?*
- Worms don't require user intervention where as viruses need user intervention (like clicking on a phishing link)