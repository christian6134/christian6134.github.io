
Whenever our devices connects to a new network, configurations must be set according to the new network:
- IP Address and Subnet Mask
- Route (gateway)
- DNS Server

**Dynamic Host Configuration Protocol (DHCP)**
--------------------------------
- Application-level protocol that relies on **UDP**
- Server listens on port 67, sends from port 68

**DHCP follows 4 step process**
1. **DHCP Discover:** Client broadcasts DHCPDISCOVER message seeking the local DHCP server if it exits `Use 255.255.255.255 (Broadcast)`
2. **DHCP Offer**: Server responds with DHCPOFFER message with an IP address available for the client to accept
3. **DHCP Request**: Client responds with DHCPREQUEST message to indicate it has accepted the IP address
4. **DHCP Ack**: Server responds with DHCPACK message to confirm that IP address is now assigned to client

**ALSO KNOWN AS DORA**

![[Pasted image 20250624182538.png]]

**In the end we expect:**
- Leased IP address to access network resources
- Gateway to route our packets **outside** our network
- A DNS server to resolve domain names

![[Pasted image 20250624182830.png]]


