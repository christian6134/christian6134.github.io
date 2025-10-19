
**Limiting the displayed packets to those smaller or larger than a certain length**
- `greater LENGTH` 
- `less LENGTH`

**PCAP**
`man pcap-filter`


**Header Bytes**
--------------------------
**Big Picture**: Filter packets based on the contents of a header byte
- ARP
- Ethernet
- ICMP
- IP
- TCP, UDP

pcap-filter allows tcpdump to refer to the contents of **any byte** in the header using `proto[expr:size]`
- **proto** refers to the protocol (arp, ether, icmp, tcp)
- **expre** indicates byte offset, where `0` refers to the first byte
- **size** indicates the number of bytes that interests us (1 by default)

**Examples**
- `ether[0] & 1 !=0` takes the first byte (0) in the ethernet header andt he decimal number 1 (0000 0001) in binary. It will return true if the result is ne to the number 0.
- Purpose: Filter is to show packets sent to multicast address which is an address that identifies a group of devices intended to receive the same data 

- `ip[0] & 0xf !=5` takes the first byte in the IP header and compares it to hexadecimal number F (0000 1111) in binary
- Returns true if the result is not equal to 5
- Purpose -> Catch all IP packets with options


`tcp[tcpflags]` refers to the TCP flags field
- tcp-syn
- tcp-ack
- tcp-fin
- tcp-rst (RESET)
- tcp-push

**More examples**
- `tcpdump "tcp[tcpflags] == tcp-syn` captures all TCP packets with only the SYN Packet flagged
- `tcpdump "tcp[tcpflags] & tcp-syn !=0` captures packets with at least the SYN flag set
- `tcpdump "tcp[tcpflags] & (tcp-syn|tcp-ack) != 0` captures TCP packets with at least the SYN or ACK flags set


**Questions**
How many packets have only the TCP Reset (RST) flag set?
- `tcpdump -r (read) traffic.pcap (path) tcp[tcpflags] == tcp-rst | wc (word count) -l (lists by line`
- 57 packets


What is the IP address of the host that sent packets larger than 15000 bytes?
- `tcpdump -r traffic.pcap greater 15000 -n`
