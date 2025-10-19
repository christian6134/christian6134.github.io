**tcpdump options on how packets are printed and displayed**
--------------------
**Quick Options**
- -q: Quick output, brief packet information
- -e: Print the link level header
- -A: Show packet data in ASCII
- -xx: Show packet data in hex
- -X: Show packet headers and data in ASCII


`-q`
- Prints timestamp
- Source and Destination IP
- Source and Destination port

`-e` 
- Includes MAC addresses in TCPDUMP
- Learning ARP and DHCP


`-A`
- Bytes mapped to English


![[Pasted image 20250629122240.png]]


**Questions**
What is the MAC address of the host that sent an ARP request?
- `sudo tcpdump -r traffic.pcap arp -e`
- 52:54:00:7c:d3:5b