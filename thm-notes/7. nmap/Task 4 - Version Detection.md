**"Extract More Information"**

Remember, still building off of `nmap`

Enable **OS Detection** by adding the `-O` option
- Triggers nmap to rely on indicators to make an **educated guess** bout the **target OS**
- No perfectly accurate OS detector


**Service and Version Detection**
- Use `-sV` to know what services are listening on open ports
- Gathering information about your target with fewer keystrokes
- Additional column "VERSION" indicates detected SSH server version


**Combine -O and -sV?**
- Just use `-A`, option enables OS Detection, Version Scanning, Traceroute and more.


**Forcing the Scan**
 When running a port scan such as `-sS`
- Possibility that target host does not reply during host phrase
- Nmap will mark host as down and won't launch a port scan against it
- Invoke Nmap to treat all hosts as online and port scan every host using `-Pn` option

![[Pasted image 20250630154424.png]]


**Questions**
---------------
Q: What is the name and detected version of the web server running on `10.10.200.168`

- `nmap -A 10.10.200.168

![[Pasted image 20250630155318.png]]