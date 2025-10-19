# Task 3 - TCP and IP Model

## Learning Objectives
- Understand the TCP/IP model structure and layers
- Compare TCP/IP model with OSI model
- Learn how layers are combined in TCP/IP
- Identify protocols and functions of each TCP/IP layer

## Overview
The TCP/IP model is a practical networking model that predates the OSI model and is widely used in modern networking. It consists of four layers that correspond to multiple OSI layers, providing a more streamlined approach to understanding network communications. The TCP/IP model is the foundation of the modern Internet.

### TCP/IP Model Structure

**Four-Layer Model**
The TCP/IP model consolidates the seven OSI layers into four practical layers:

1. **Network Access Layer** (Physical + Data Link)
2. **Internet Layer** (Network)
3. **Transport Layer** (Transport)
4. **Application Layer** (Session + Presentation + Application)

### Layer Comparison: OSI vs TCP/IP

**Application Layer Consolidation**
- **OSI Layers 5, 6, 7** → **TCP/IP Application Layer**
- Combines Session, Presentation, and Application layers
- Provides direct interface to user applications
- Handles all application-specific protocols

**Key Differences**
- TCP/IP model is more practical and implementation-focused
- OSI model is more theoretical and comprehensive
- TCP/IP model reflects actual Internet architecture
- OSI model provides more detailed layer separation

### TCP/IP Layer Functions

**Network Access Layer**
- Combines Physical and Data Link layers
- Handles hardware addressing and physical transmission
- Manages network interface and media access
- Examples: Ethernet, WiFi, PPP

**Internet Layer**
- Corresponds to OSI Network layer
- Provides logical addressing and routing
- Handles packet forwarding between networks
- Examples: IP, ICMP, ARP

**Transport Layer**
- Identical to OSI Transport layer
- Manages end-to-end communication
- Provides reliable or unreliable delivery
- Examples: TCP, UDP

**Application Layer**
- Combines OSI layers 5, 6, and 7
- Provides services directly to applications
- Handles all application-specific protocols
- Examples: HTTP, DNS, SMTP, FTP

### Protocol Stack Examples

**Web Browsing (HTTP over TCP/IP)**
1. Application Layer: HTTP request
2. Transport Layer: TCP connection
3. Internet Layer: IP packet routing
4. Network Access Layer: Ethernet frame

**Email (SMTP over TCP/IP)**
1. Application Layer: SMTP commands
2. Transport Layer: TCP reliable delivery
3. Internet Layer: IP addressing
4. Network Access Layer: Physical transmission

### Practical Applications

**Network Troubleshooting**
- Use TCP/IP model for systematic analysis
- Identify issues by layer
- Apply appropriate troubleshooting tools
- Document findings using layer terminology

**Security Analysis**
- Understand attack vectors by layer
- Implement security controls at appropriate layers
- Analyze network traffic using layer concepts
- Design defense-in-depth strategies

## Best Practices
- Understand both OSI and TCP/IP models
- Use TCP/IP model for practical networking
- Apply layer concepts to troubleshooting
- Practice identifying protocols by layer
- Document network issues using appropriate model