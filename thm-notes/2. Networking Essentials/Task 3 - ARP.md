**Address Resolution Protocol (ARP)** (LAYER 2)
-------------------------------------------------------
- 2 Common Data Link Layers we use are Ethernet and Wi-Fi
- When one host needs to communicate with another on the same Ethernet or Wi-Fi
	- Send IP packet with Data Link Layer Frame
	- Knows IP Address of Target Host, needs to look up MAC address
- Only need to know MAC address when communicating


**MAC ADDRESS FORMAT**:
- 48-bit number
- Example: 7C:DF:A1:D3:8C:5C


**ARP Purpose**
Makes it possible to **find the MAC address of another device on the Ethernet**


**Example:**
- ARP Request is sent from MAC address of the requester to the broadcast MAC address (ff:ff:ff:ff:ff:ff)
- ARP reply arrives with the Hosts IP address
- Two hosts can exchange data link layer frames


`tcpdump` -> Displays packets in the terms of ARP request and ARP reply


**NOTE**: ARP Reply and Request packets are not encapsulated within UDP or IP packets … encapsulated within a **Ethernet Frame**





