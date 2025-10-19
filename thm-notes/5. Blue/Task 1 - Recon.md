
**How many ports are open with a port number under 1000?**
- `nmap -sV -vv -script vuln TARGET_IP`
- Simply count the ports

**What is this machine vulnerable to?**
- View Vulnerabilities, invoke same command 
- `ms17-010`


**Purpose**:
- Scanned the target using NMAP, to list out what Vulnerabilities can be exploited
- We found out that we can exploit the eternal_blue ms17_010 vulnerability on this target machine