
**What makes an IP Address?**
- Four Octets (32 bits)
- 8 bits allows a decimal number from 0 and 255

![[Pasted image 20250624173542.png]]

- 0 and 255 are reserved for the **network and broadcast addresses**

Network Address -> 192.168.1.0
Broadcast Address -> 192.168.1.255


**Looking Up a Network Config**
--
On MS WINDOWS:
- `ipconfig`

On LINUX AND UNIX:
- `ifconfig`
- `ip address show` or `ip a s`


**Subnet Masks**
- `255.255.255.0` is also written as /24
- This means the leftmost 24 bits of the IP Address are the same across a network
- 0 -> network Address, 255 -> Broadcast Address

**Private Addresses**
- Need Public IP ADDRESS on a Router
- Network Address Translation (NAT)

![[Pasted image 20250624174046.png]]

**Routing**
--
- Forward data packets to the proper network
- Passes through multiple routers