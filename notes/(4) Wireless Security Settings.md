# 4.1.4 Wireless Security Settings

## Learning Objectives
- Understand WPA2 PSK vulnerabilities and WPA3 improvements
- Explain SAE (Simultaneous Authentication of Equals) and dragon fly handshake
- Describe wireless authentication methods and security modes
- Identify AAA/Remote Authentication, RADIUS, IEEE 802.1X, and EAP protocols

## Overview
Wireless security settings involve implementing proper authentication methods, encryption protocols, and access controls to protect wireless networks from various attacks and unauthorized access.

## WPA2 PSK Vulnerabilities

### Pre-Shared Key Problems
**Core Issue:** WPA2 PSK has a brute-force vulnerability

**Attack Method:**
- **Handshake Capture** - Attackers listen to the four-way handshake
- **Hash Derivation** - Some methods can derive PSK hash without handshake
- **Brute Force** - With the hash, attackers can brute force the pre-shared key (PSK)
- **Weak Passwords** - Weak PSK passwords are easily cracked

**Security Implications:**
- **Password Cracking** - Weak passwords can be cracked
- **Network Compromise** - Entire network can be compromised
- **Data Interception** - All network traffic can be intercepted
- **Unauthorized Access** - Attackers gain network access

## WPA3 Security Improvements

### Enhanced Encryption
**Technology:** Wi-Fi Protected Access 3 (WPA3)

**GCMP Block Cipher Mode:**
- **Galois/Counter Mode Protocol** - Stronger encryption than WPA2
- **Message Integrity Check** - Ensures message integrity
- **Data Confidentiality** - Protects data confidentiality
- **Enhanced Security** - Improved security over WPA2

### SAE (Simultaneous Authentication of Equals)
**Revolutionary Change:** WPA3 changes the PSK authentication process

**Key Features:**
- **Mutual Authentication** - Both parties authenticate each other
- **Shared Session Key** - Generate shared session key without sending key across network
- **No Handshake Vulnerability** - No more handshake, no more brute force attacks
- **Enhanced Security** - Significantly improved security

**Dragon Fly Handshake:**
- **Diffie-Hellman Derived** - Uses Diffie-Hellman key exchange with authentication
- **Authentication Component** - Includes authentication component
- **Unique Session Keys** - Everyone uses different session key, even with same PSK
- **IEEE Standard** - IEEE standard implementation

## Wireless Authentication Methods

### Authentication Credentials
**Shared Password/PSK:**
- **Pre-Shared Key** - Shared password for network access
- **Simple Implementation** - Easy to implement and configure
- **Home Networks** - Common in home and small office networks
- **Security Limitations** - Limited security compared to enterprise methods

**Centralized Authentication (802.1X):**
- **Enterprise Authentication** - Centralized authentication server
- **Individual Authentication** - Each user authenticated individually
- **Strong Security** - Enhanced security for enterprise environments
- **Scalability** - Scales to large numbers of users

### Configuration Process
**Network Connection:** Part of wireless network connection process
**User Prompting:** Prompted during connection process
**Credential Management:** Secure credential storage and management
**Session Management:** Manage authentication sessions

## Wireless Security Modes

### WAP/Router Configuration
**Authentication Configuration:** Configure authentication on WAP/Wireless Router

**Open System:**
- **No Authentication** - No authentication password required
- **Public Access** - Open access to anyone
- **No Security** - No security protection
- **Risk Level** - High security risk

**WPA3:**
- **Pre-Shared Key** - Everyone uses the pre-shared key
- **Enhanced Security** - Improved security over WPA2
- **SAE Authentication** - Uses SAE for authentication
- **Home/Small Office** - Suitable for home and small office use

**WPA3 Enterprise:**
- **Individual Authentication** - Authenticates users individually
- **Authentication Server** - Uses authentication server (RADIUS)
- **Enterprise Security** - Enhanced security for enterprise environments
- **Scalable** - Scales to large numbers of users

## AAA/Remote Authentication

### Authentication Framework
**Identification:**
- **Identity Claim** - Who do you claim to be
- **Username** - User identification
- **Account Information** - Basic account information
- **Initial Step** - First step in authentication process

**Authentication:**
- **Identity Proof** - Prove you are who you say you are
- **Password/Other** - Password or other authentication factors
- **Credential Verification** - Verify provided credentials
- **Access Decision** - Determine if access should be granted

**Authorization:**
- **Access Rights** - Based on identification/authentication
- **Resource Access** - What access do you have
- **Permission Levels** - Determine permission levels
- **Resource Control** - Control access to specific resources

**Accounting:**
- **Resource Usage** - Track resources used
- **Login Time** - Record login times
- **Data Transfer** - Monitor data sent and received
- **Audit Trail** - Maintain audit trail

## RADIUS (Remote Authentication Dial-In User Service)

### Centralized Authentication
**Definition:** Remote Authentication Dial-In User Service

**Platform Support:** Supported on wide variety of platforms and devices

**Centralized Authentication Uses:**
- **Routers** - Router authentication
- **Switches** - Switch authentication
- **Firewalls** - Firewall authentication
- **Server Authentication** - Server access authentication
- **Remote VPN Access** - VPN authentication
- **802.1X Enterprise Access** - Enterprise wireless authentication

**Benefits:**
- **Centralized Management** - Single point of authentication management
- **Scalability** - Scales to large numbers of users
- **Consistency** - Consistent authentication across all devices
- **Audit Capability** - Centralized audit and logging

## IEEE 802.1X

### Port-Based Network Access Control
**Definition:** Provides prompt for username and password

**Alternative Name:** Port-Based Network Access Control (NAC)

**Core Principle:** NO ACCESS until authenticated

**Integration:** Used in combination with RADIUS, LDAP, etc.

**Implementation:**
- **Network Access Control** - Control access to network ports
- **Authentication Required** - Authentication required before network access
- **Centralized Management** - Centralized authentication management
- **Enterprise Standard** - Enterprise network access standard

## EAP (Extensible Authentication Protocol)

### Authentication Framework
**Definition:** Extensible Authentication Protocol (EAP)

**Key Features:**
- **Authentication Framework** - Flexible authentication framework
- **Multiple Methods** - Many ways to authenticate
- **802.1X Integration** - Integrates with 802.1X
- **Standards-Based** - RFC-compliant authentication

**EAP Types:**
- **EAP-TLS** - Certificate-based authentication
- **EAP-TTLS** - Tunneled TLS authentication
- **PEAP** - Protected EAP authentication
- **EAP-MD5** - Challenge-response authentication

**Benefits:**
- **Flexibility** - Flexible authentication methods
- **Security** - Strong authentication security
- **Standards Compliance** - Follows established standards
- **Interoperability** - Works with various systems

## Best Practices
- **Use WPA3** - Implement WPA3 when possible
- **Strong Passwords** - Use strong, complex passwords
- **Enterprise Authentication** - Use enterprise authentication for business networks
- **Regular Updates** - Keep wireless equipment updated
- **Network Segmentation** - Segment wireless networks appropriately
- **Monitoring** - Monitor wireless network activities
- **Access Control** - Implement proper access controls
- **Incident Response** - Have incident response procedures