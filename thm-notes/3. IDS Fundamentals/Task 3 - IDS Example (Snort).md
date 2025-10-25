
*What is Snort IDS?*
- Most widely used open-source IDS solution
- Uses `signature and anomaly` based detection.
- Uses built in rule files to hold a variety of known attack patterns.


#### Modes of Snort
---
**1. Packet Sniffer Mode**
- Reads and displays network packets without performing analysis.
- Does not directly employ IDS capabilities.
- Useful for `monitoring and troubleshooting.`
- Display the network traffic on console or even output to a file

*Use Case:*
- Network Performance Issues
	- Team requires detailed insights into the network traffic
	- Utilize Snort's packet sniffer Mode


**2. Packet logging mode**
- Performs detection on network traffic and displays as alerts on the console for action.
- Some cases require network traffic to be `logged later for analysis.`
- Allows you to `log network traffic as a PCAP (standard packet capture file format).`
- Includes all network traffic and detections.

*Use Case:*
- Team needs to initiate a forensic investigation.
- Need traffic logs to perform root cause analysis
- Use packet logging


**3. NIDS**
- Primary mode that monitors network traffic and applies its `rule files` to identify any match to the known attack patterns store as `signatures.`
- Match? -> Generate Alert.

*Use Case:*
- Security team must proactively monitor network or systems to detect potential threats.
- 