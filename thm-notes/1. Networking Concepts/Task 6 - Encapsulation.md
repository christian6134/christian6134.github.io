**Encapsulation**
- Refers to the process of every layer adding a header to the received unit of data
- Sends encapsulated data to unit below

**Application Data**
- When user inputs data they want to send
- Writing an email and hitting send
- Application formats this data and sends to **Transport Layer**

**Transport Protocol Segment or Datagram**
- Transport layer (TCP or UDP) adds proper header information
- TCP Segment
- UDP Datagram
- Sent to **Network Layer**

**Network Packet**
- Adds an IP header to the TCP or UDP segment / datagram
- Sent below to Data Link Layer

**Data Link Frame**
- Ethernet or WiFi receives the IP packet and adds header and trailer, creating a frame

![[Pasted image 20250624180004.png]]

**Questions**
--
![[Pasted image 20250624180047.png]]