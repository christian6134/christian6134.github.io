
**Focusing attention to a specific person or conversation at a social gathering**


**Filtering By Host**
----------
**Scenario:** You are only interested in IP packets exchanged with your network printer or specific game server
- Limit captured packets to this host using `host IP` or `host HOSTNAME`
- Limit captured packets from a certain source host `src host IP or src host HOSTNAME`
- Similarly, `dst host IP or dst host HOSTNAME`


**Filtering By Port**
---------------------------
**Scenario:** If you want to capture all DNS traffic, limit captured packets to `port 53`
- DNS uses UDP and TCP ports 53 by default


**Filtering by Protocol**
`ip, ip6, udp, tcp, icmp`
Limit capture to certain packets



**Questions**
--------------------

**How many packets in `traffic.pcap` use the ICMP protocol?**
- `tcpdump -r traffic.pcap icmp | wc -l`


**What is the IP address of the host that asked for the MAC address of 192.168.124.137?**
![[Pasted image 20250628174852.png]]


**What hostname (subdomain) appears in the first DNS query?**
`tcpdump -r traffic.pcap port 53 -c 3`
![[Pasted image 20250628175217.png]]
