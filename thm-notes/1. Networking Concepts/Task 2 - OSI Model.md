# Task 2 - OSI Model

## Learning Objectives
- Understand the seven-layer OSI model structure and purpose
- Learn the functions of each OSI layer
- Master the OSI layer mnemonic and layer numbering
- Identify protocols and technologies associated with each layer

## Overview
The Open Systems Interconnection (OSI) model is a conceptual framework developed by the International Organization for Standardization (ISO) that describes how communications should occur in a network. This seven-layer model provides a standardized approach to understanding network communications and serves as a foundation for network protocol design and troubleshooting.

### OSI Model Fundamentals

**Model Purpose**
- Describes how communications should occur in a network
- Defines a framework for computer network communications
- Provides standardized approach to protocol design
- Enables interoperability between different systems

**Layer Mnemonic**
Remember: **"Please Do Not Throw Spinach Pizza Away"**
1. Physical Layer
2. Data Link Layer  
3. Network Layer
4. Transport Layer
5. Session Layer
6. Presentation Layer
7. Application Layer

### Layer 1: Physical Layer

**Physical Layer Functions**
- Deals with physical connections between devices
- Manages transmission mediums (wires, cables, wireless)
- Handles binary digits (0s and 1s)
- Controls electrical, optical, or wireless data transmission

**Physical Layer Examples**
- Ethernet cables
- Fiber optic cables
- Wireless transmission
- Network interface cards (NICs)

### Layer 2: Data Link Layer

**Data Link Layer Functions**
- Enables data transfer between nodes within the same network
- Describes agreement between different systems on same network
- Manages group of networked devices using shared medium
- Handles error detection and correction

**Data Link Layer Examples**
- Ethernet protocols
- WiFi (802.11)
- Point-to-Point Protocol (PPP)

**MAC Addresses**
- **Media Access Control** addresses
- 3 leftmost bytes identify vendor/manufacturer
- Physical address for network interface
- Destination and source data link addresses

### Layer 3: Network Layer

**Network Layer Functions**
- Concerns sending data across different networks
- Provides logical addressing (IP addresses)
- Handles routing between networks
- Finds path to transfer packets between various networks

**Network Layer Examples**
- Internet Protocol (IP)
- Internet Control Message Protocol (ICMP)
- Virtual Private Network (VPN) protocols
- Routing protocols (OSPF, BGP)

### Layer 4: Transport Layer

**Transport Layer Functions**
- Enables end-to-end communication between applications
- Runs on different hosts across network
- Provides reliable or unreliable data delivery
- Manages flow control and error recovery

**Transport Layer Examples**
- Transmission Control Protocol (TCP)
- User Datagram Protocol (UDP)
- Stream Control Transmission Protocol (SCTP)

### Layer 5: Session Layer

**Session Layer Functions**
- Establishes, maintains, and synchronizes communication
- Between applications running on different hosts
- Manages session establishment and termination
- Handles session recovery and checkpointing

**Session Layer Examples**
- Remote Procedure Call (RPC)
- Network File System (NFS)
- SQL sessions
- NetBIOS sessions

### Layer 6: Presentation Layer

**Presentation Layer Functions**
- Ensures data is delivered in form application layer can understand
- Handles data encoding and decoding
- Manages data compression and decompression
- Provides encryption and decryption services

**Presentation Layer Examples**
- Image formats (JPEG, GIF, PNG)
- Multipurpose Internet Mail Extensions (MIME)
- Data encryption standards
- Character encoding (ASCII, Unicode)

### Layer 7: Application Layer

**Application Layer Functions**
- Provides network services directly to end-user applications
- Top layer of OSI model
- Interfaces with user applications
- Implements specific network services

**Application Layer Examples**
- Hypertext Transfer Protocol (HTTP)
- Domain Name System (DNS)
- Simple Mail Transfer Protocol (SMTP)
- Internet Message Access Protocol (IMAP)
- File Transfer Protocol (FTP)

## Practical Applications
- Network troubleshooting and analysis
- Protocol design and implementation
- Security assessment and monitoring
- Network architecture planning
- Interoperability testing

## Best Practices
- Use the mnemonic to remember layer order
- Understand data flow through layers
- Practice identifying protocols by layer
- Apply OSI model to troubleshooting scenarios
- Document network issues using layer terminology