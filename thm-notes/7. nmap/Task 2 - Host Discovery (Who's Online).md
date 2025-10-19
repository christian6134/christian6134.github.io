
**NMAP - Ways to specify a target**
- **IP Range** using `-`: If you want to scan IP addresses from 192.168.0.1 to 192.168.0.10 -> `192.168.0.1-10`
- **IP Subnet** using `/` : Express 192.168.0.1 as `192.168.0.1/24` is equivalent to 192.168.0.0-255
- **Hostname**: `example.thm`

Discover the online hosts on a network: use -`sn` 
Use sudo (root) when using nmap, because if not it will default to limitations present in ping and tcp scans


**Scanning a "Local Network"**
-----------------------------------------------------
{Local Network}
- Refers to the network that one is directly connected to (Ethernet or WiFI)
- If our ip address is 192.168.66.89 we will `nmap -sn 192.168.66.0/24`

- We can look up MAC addresses of devices
- Nmap sends ARP requests, when a device responds --> Nmap labels `Host is up`



**Scanning a "Remote Network"**
{Remote Network}
- At least one router separates our system from this network
- All traffic to target system must travel **through routers**
- **Cannot** send ARP requests


**More Control**
`-PS[portlist]
`-PA[portlist]`
`-PU[portlist]`
For TCP SYN, TCP ACK, UDP Discovery

`-sL` - List scan - simply lists targets to scan


**Question**
-What is the last IP address that will be scanned when your scan target is `192.168.0.1/27`?
- `sudo nmap -sL 192.168.0.1/27`
- 192.168.0.31