**Recall:** We used `-sn` to discover the **live hosts**
**Now**:
- We want to discover the network services listening on these live hosts
- **Network Service**: Any process that is listening for incoming connections on a UDP or TCP port
- **Example**: TCP listens on port 80 and 443, DNS typically uses port 53


**Scanning TCP Ports**
- Easiest way to know whether a TCP port is open would be to telnet to the port
- Only open TCP ports would respond appropriately and allow a TCP connection to be established


**Connect Scan**
- Can be triggered using `-sT`
- Attempts to complete the TCP three-way handshake with every **target TCP port**
- If TCP port is open and Nmap connects, Nmap will tear down connection
- Attempting to connect to a closed port ---> TCP RST-ACK Packet


**SYN Scan (Stealth)**
- Differs from Connect Scan which attempts to connect to a TCP Port
- Scan only executes the first part of the 3 way handshake
	- Sends a TCP SYN Packets
	- The 3 way handshake is never completed
	- Expected to lead to fewer logs as connection is **never established** 
	- `Stealth Scan`, `-sS`


**Scanning UDP Ports**
- Does not require establishing a connection and tearing it down afterwards
- Suitable for real time applications 
- Nmap offers `-su` to scan for UDP services
- ICMP Destination unreachable as a **response** of UDP packets sent to closed UDP ports


**More on Nmap: Targeting Ports**
----------------------------------------------------------------
**Note**: Nmap scans the most common 1,000 ports by default
- `-F` - Invokes Fast mode, scans for the 100 most common ports
- `-p[range]` allows you to specify a **range of ports** to scan `-p10-1024` will scan ports from 10 - 1024
- `-p- scans all ports 1-65535`


![[Pasted image 20250630152615.png]]


**Questions**

`How many TCP ports are open on the target system at `10.10.200.168`?`
- `nmap -sT 10.10.200.168`
- `map scan report for ip-10-10-200-168.eu-west-1.compute.internal (10.10.200.168)
	Host is up (0.00042s latency).
	Not shown: 994 closed ports
	PORT     STATE SERVICE
	7/tcp    open  echo
	9/tcp    open  discard
	13/tcp   open  daytime
	17/tcp   open  qotd
	22/tcp   open  ssh
	8008/tcp open  http
	MAC Address: 02:D4:92:D5:D3:91 (Unknown)
	- **Answer: 6 Ports**



Find the listening web server on `10.10.200.168` and access it with your browser. What is the flag that appears on its main page?
- `nmap -sT 10.10.200.168`
- HTTP://10.10.200.168:8008
- Port 8008 ---> HTTP Service as a result of scan
- Flag -> THM{SECRET_PAGE_38B9P6}