**Internet Control Message Protocol**
-------------------------------------------------
Mainly used for **network diagnostics and error reporting**
- `ping` - used to test connectivity to a target system
	- measures RTT (round trip time)
	- learns if a target is alive and that it is **reachable**
- `traceroute` - Uses ICMP to **discover the route** from the host to source


**PING**
--------------
- Sends **ICMP Echo Request** (Type 8)
- Receives **ICMP Echo Reply** (Type 0)
`ping -c 4` ---> ping command to stop after sending four packets


**Traceroute**
---------
**How can we make very router between our system and a target reveal itself**
- TTL field ---> Indicates the maximum number of routers a packet can travel through before its dropped
- Router decrements packets TTL by one before it sends it across
- TTL Reaches 0? -> Router Drops packet and sends **ICMP Time Exceeded Message** (ICMP Type 11)
