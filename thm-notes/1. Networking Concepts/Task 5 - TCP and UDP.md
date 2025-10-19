
**UDP**
--
- Simple Connectionless protocol 
- Operates at the **transport** **layer**

**Connectionless**: Does not need to establish a connection

- Does not provide reliable data transfer and recovery

**TCP**
--
- Connection-oriented transport protocol
- Ensures reliable data delivery
- **Transport layer**


**Three-Way Handshake**
- **SYN Packet**: Client initiates the connection by sending a SYN Packet to the server -> Contains random chosen initial seq number
- **SYN-ACK Packet**: Server responds with SYN-ACK, adds initial sequence number randomly chosen by server
- **ACK Packet:** Completed as the client sends an ACK for the  SYN-ACK

![[Pasted image 20250624174721.png]]


