# 3.3.2 States of Data

## Learning Objectives
- Understand the three primary states of data and their security implications
- Explain data at rest protection methods and encryption strategies
- Describe data in transit security and transport encryption
- Identify data in use vulnerabilities and memory protection
- Understand data sovereignty and geolocation considerations

## Overview
Data exists in three primary states throughout its lifecycle, each requiring specific security controls and protection mechanisms. Understanding these states is crucial for implementing comprehensive data protection strategies.

## Data at Rest

### Definition and Characteristics
**Definition:** Data stored on storage devices in a static state

**Storage Devices:**
- **Hard Drives** - Traditional magnetic storage
- **Solid State Drives (SSD)** - Flash-based storage
- **Flash Drives** - Portable storage devices
- **Cloud Storage** - Remote storage services
- **Tape Storage** - Long-term archival storage

### Protection Methods

#### Encryption Strategies
**Whole Disk Encryption:**
- **Full Drive Protection** - Encrypt entire storage device
- **Transparent Operation** - Automatic encryption/decryption
- **Hardware Integration** - TPM and hardware security modules
- **Examples** - BitLocker, FileVault, LUKS

**Database Encryption:**
- **Transparent Data Encryption (TDE)** - Encrypt entire database
- **Column-Level Encryption** - Encrypt specific sensitive columns
- **Application-Level Encryption** - Encrypt data before database storage
- **Key Management** - Secure encryption key handling

**File/Folder-Level Encryption:**
- **Selective Protection** - Encrypt specific files or folders
- **User Control** - Individual user encryption decisions
- **Granular Security** - Fine-grained access control
- **Examples** - EFS, VeraCrypt, individual file encryption

#### Access Control
**Access Control Lists (ACLs):**
- **User Permissions** - Define who can access data
- **Group Permissions** - Role-based access control
- **File Permissions** - Read, write, execute controls
- **Directory Permissions** - Folder-level access control

**Authorization Requirements:**
- **Authentication** - Verify user identity
- **Authorization** - Determine access permissions
- **Audit Logging** - Track access attempts and activities
- **Least Privilege** - Minimum necessary access

## Data in Transit

### Definition and Characteristics
**Definition:** Data transmitted over networks in motion

**Transmission Methods:**
- **Network Protocols** - TCP, UDP, HTTP, HTTPS
- **Wireless Networks** - Wi-Fi, cellular, Bluetooth
- **Wired Networks** - Ethernet, fiber optic
- **Internet Transmission** - Public network communication

### Security Challenges
**Limited Protection:**
- **Multiple Hops** - Data passes through many devices
- **Network Infrastructure** - Switches, routers, gateways
- **Public Networks** - Internet and wireless networks
- **Interception Risk** - Potential for data capture

**Vulnerability Points:**
- **Network Sniffing** - Packet capture and analysis
- **Man-in-the-Middle** - Interception and modification
- **Wireless Eavesdropping** - Unencrypted wireless traffic
- **DNS Hijacking** - Redirecting traffic to malicious servers

### Protection Methods

#### Network-Based Protection
**Firewalls:**
- **Traffic Filtering** - Control data flow
- **Deep Packet Inspection** - Analyze packet contents
- **Application Filtering** - Control application traffic
- **Intrusion Prevention** - Block malicious traffic

**Intrusion Prevention Systems (IPS):**
- **Real-Time Monitoring** - Continuous traffic analysis
- **Threat Detection** - Identify malicious activities
- **Automatic Response** - Block suspicious traffic
- **Signature Updates** - Keep threat signatures current

#### Transport Encryption
**TLS (Transport Layer Security):**
- **Web Traffic** - HTTPS for web communications
- **Email Security** - SMTPS, IMAPS, POP3S
- **Application Security** - Secure application protocols
- **Certificate Validation** - Verify server authenticity

**IPsec (Internet Protocol Security):**
- **Network Layer** - Layer 3 encryption
- **VPN Connections** - Site-to-site and remote access
- **Tunnel Mode** - Encrypt entire IP packets
- **Transport Mode** - Encrypt payload only

## Data in Use

### Definition and Characteristics
**Definition:** Data actively being processed in system memory

**Processing Locations:**
- **System RAM** - Random access memory
- **CPU Registers** - Processor registers
- **CPU Cache** - Processor cache memory
- **Virtual Memory** - Paged memory systems

### Security Vulnerabilities
**Decrypted State:**
- **Memory Exposure** - Data visible in memory
- **Process Memory** - Application memory space
- **System Memory** - Operating system memory
- **Cache Memory** - CPU cache exposure

**Attack Vectors:**
- **Memory Dumps** - System crash dumps
- **Memory Scraping** - Malware memory analysis
- **Side-Channel Attacks** - Timing and power analysis
- **Cold Boot Attacks** - Memory persistence after shutdown

### Protection Methods
**Memory Protection:**
- **Address Space Layout Randomization (ASLR)** - Randomize memory layout
- **Data Execution Prevention (DEP)** - Prevent code execution in data areas
- **Memory Encryption** - Encrypt sensitive data in memory
- **Secure Enclaves** - Isolated processing environments

## Data Sovereignty

### Definition and Legal Implications
**Definition:** Information stored within a specific country's jurisdiction

**Legal Requirements:**
- **Local Laws** - Subject to country-specific regulations
- **Court Orders** - Legal monitoring and access
- **Government Access** - Law enforcement capabilities
- **Compliance Requirements** - Regulatory obligations

### Geographic Restrictions
**GDPR Requirements:**
- **EU Data Storage** - Data collected on EU citizens must be stored in EU
- **Cross-Border Transfers** - Restricted data movement
- **Data Localization** - Require local data storage
- **Privacy Rights** - Enhanced privacy protections

**Other Regulations:**
- **Data Localization Laws** - Country-specific requirements
- **Export Controls** - Restrictions on data export
- **National Security** - Government access requirements
- **Industry Regulations** - Sector-specific requirements

## Geolocation

### Location-Based Access Control
**Definition:** Using location details to manage data access

**Technologies:**
- **802.11 Networks** - Wi-Fi access point location
- **Mobile Networks** - Cellular tower triangulation
- **GPS** - Global positioning system
- **IP Geolocation** - Internet protocol address location

### Access Management
**Geographic Restrictions:**
- **Country-Based Access** - Prevent access from other countries
- **Regional Controls** - Restrict access by geographic region
- **Time Zone Restrictions** - Limit access by time zones
- **Compliance Requirements** - Meet regulatory restrictions

**Administrative Controls:**
- **Secure Areas** - Require secure locations for administrative tasks
- **VPN Requirements** - Force secure connections
- **Location Verification** - Verify user location
- **Audit Logging** - Track location-based access

## Best Practices
- **Comprehensive Protection** - Secure data in all states
- **Encryption Everywhere** - Encrypt data at rest, in transit, and in use
- **Access Controls** - Implement strong authentication and authorization
- **Monitoring** - Continuous security monitoring and logging
- **Compliance** - Ensure regulatory compliance
- **Staff Training** - Educate users on data protection requirements
- **Regular Assessments** - Periodic security evaluations
- **Incident Response** - Prepared response procedures