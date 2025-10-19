
**Meterpreter**: 
- Metasploit payload that supports penetration testing.
- Runs on the target system and acts as an agent with a command and control architecture. 


**How does Meterpreter Work?**
- Runs on target system (not installed)
- Runs in memory and does not write itself to disk
- Avoids being detected during **antivirus scans**
- Exists in **ram**

**Avoids Detection** by the IPS (intrusion prevention system) and IDS (intrusion Detection system) through encrypted communication with the Metasploit server.
`getpid`
`ps`

  
It is also worth noting that Meterpreter will establish an encrypted (TLS) communication channel with the attacker's system.

`msfvenom --list payloads | grep meterpreter`

### Choices
-------
*Your decision on which version of Meterpreter to use will be mostly based on three factors;

- The target operating system (Is the target operating system Linux or Windows? Is it a Mac device? Is it an Android phone? etc.)
- Components available on the target system (Is Python installed? Is this a PHP website? etc.)
- Network connection types you can have with the target system (Do they allow raw TCP connections? Can you only have an HTTPS reverse connection? Are IPv6 addresses not as closely monitored as IPv4 addresses? etc.)*