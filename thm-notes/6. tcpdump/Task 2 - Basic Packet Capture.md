- Can run `tcpdump` without providing any arguments
- Only useful to test that you have it installed


**Specifying the Network Interface**
Use `-i INTERFACE` to choose to listen on a set interface
- use `-i any` to listen to all available interfaces
- `-i eth0`

`ip address show or ip a s` lists the available network interfaces
- 1 network card `ens5`
- Loopback address


**Saving captured packets**
Use `-w FILE`
- Saving capture packets to a file
- Saved packets can be inspected later
- Most common extension --> .pcap


**Read captured packets from a file**
Use tcpdump to read packets from a file by using `-r FILE`
- Learn about protocol behavior
- Inspect network packet attacks


**Limiting the no. of Captured Packets**
- Specify the no. of packets to capture by specifying the count `-c COUNT`


**Resolving IP Addresses and Port Numbers**
	tcdump will resolve IP addresses and print friendly Domain Names when possible
	- To avoid making DNS lookups use `-n` argument
	- `-nn` stops both DNS and port number lookups


**More Verbose Output**
- `v` ---> Time to live, id, total length, options
- read `man tcpdump`
- `vv` even more verbose


![[Pasted image 20250628160814.png]]


