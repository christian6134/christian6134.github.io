**Open Systems Interconnection Model**
-----

- Developed by International Organization for Standardization (OSI)
- Describes how communications should occur in a **network**
- Defines a framework for computer network communications

**Remember:**
`Please Do Not Throw Spinach Pizza Away`
	1     2   3        4        5           6        7

![[Pasted image 20250624171636.png]]


**Physical Layer (L1)**
--
- Deals with Physical connections between devices
- Mediums, wires, binary digits 0 and 1
- Data transmission can be electrical, optical or wireless

**Examples**
- Ethernet Cables!



**Data Link Layer (L2)**
--
**Represents the protocol that enables data transfer between nodes within the same network**
- Describes an **agreement** between different systems on the same network
- Group of networked devices using a shared medium
**Examples**
- Ethernet 
- WiFi

**MAC ADDRESSES (Media Access Control)**
- 3 left most bytes identify the vendor
- Physical Address
- Destination data link address
- Source data link address


**Network Layer (L3)**
--
**Concerns sending data across different networks**
- Logical addressing
- Routing
- Finding a path to transfer the network packets between various networks

**Examples**
- Internet Protocol (IP)
- Internet Control Message Protocol (ICMP)
- Virtual Private Network (VPN)



**Transport Layer (L4)**
--
**Enables end-end communication b/w running applications on different hosts**
- Examples
- TCP
- UDP



**! SESSION LAYER (L5)**
--
**Responsible for establishing, maintaining and synchronizing communication between applications running on different hosts**

Examples
- Remote Procedure Call
- Network File System (NFS)


**! PRESENTATION LAYER (L6)**
-- 
**Ensures data is delivered in a form the application layer (l7) can understand**
- Handles data encoding
- Compression
- Encryption

**Example:**
Consider sending an image via email
- JPEG, GIF and PNG to save our images
- MIME ---> Attach file to email


**Application Layer (L7)**
--
**Provides network services directly to end-user applications**
- HTTP Protocol to request a file
- Top layer
- DNS, HTTP, SMTP, IMAP

![[Pasted image 20250624173100.png]]



