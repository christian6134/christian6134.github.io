# 2.5.3 Hardening Techniques

## Learning Objectives
- Understand system hardening principles and methods
- Explain endpoint detection and response capabilities
- Describe host-based security controls

## Overview
System hardening involves configuring systems securely by removing unnecessary components, applying security patches, and implementing protective controls.

## System Hardening
**Purpose:** Secure systems by reducing attack surface and implementing security controls

### Operating System Hardening
- **Multi-Platform Support** - Windows, Linux, iOS, Android
- **Regular Updates** - OS updates, service packs, security patches
- **Security Baselines** - Industry-standard configurations

### User Account Security
- **Password Policies** - Minimum length and complexity requirements
- **Account Limitations** - Restricted privileges and access
- **Account Monitoring** - Regular review and cleanup

### Network Security
- **Limited Network Access** - Restrict unnecessary network connections
- **Firewall Configuration** - Block unnecessary ports and services
- **Network Monitoring** - Monitor for unusual activity

## Encryption Implementation
**Purpose:** Prevent unauthorized access to data

### Encryption Types
- **File Level Encryption** - Windows EFS (Encrypting File System)
- **Full Disk Encryption (FDE)** - BitLocker, FileVault
- **Network Communication Encryption** - VPN, application-level encryption

### Benefits
- Data protection at rest and in transit
- Compliance with data protection requirements
- Defense against data theft
- Always-on protection

## Endpoint Detection and Response (EDR)
**Purpose:** Advanced threat protection using behavioral analysis

### EDR Capabilities
**Detection:**
- Behavioral analysis and machine learning
- Process monitoring and anomaly detection
- Lightweight agent deployment
- Real-time threat identification

**Investigation:**
- Root cause analysis
- Threat intelligence correlation
- Forensic data collection
- Attack timeline reconstruction

**Response:**
- System isolation and quarantine
- Threat rollback capabilities
- API-driven automation
- Minimal user intervention required

### Benefits
- Scalable threat protection
- Advanced detection beyond signatures
- Automated response capabilities
- Comprehensive threat visibility

## Host-Based Firewall
**Purpose:** Software-based firewall on every endpoint

### Capabilities
- **Traffic Control** - Allow or disallow incoming/outgoing traffic
- **Application Control** - Control by application process
- **Process Monitoring** - View all data and processes
- **Malware Prevention** - Block unknown processes

### Benefits
- Personal firewall protection
- Application-level control
- Malware prevention
- Network traffic visibility

## Host-Based Intrusion Prevention Systems (HIPS)
**Purpose:** Recognize and block known attacks at the host level

### HIPS Functions
- **Attack Recognition** - Known attack pattern detection
- **OS Security** - Secure operating system configurations
- **Service Validation** - Validate incoming service requests
- **Endpoint Integration** - Built into endpoint protection software

### Detection Methods
- **Signature-Based** - Known attack patterns
- **Behavioral Analysis** - Unusual system behavior
- **Data Access Monitoring** - Non-encrypted data access

## Port and Service Management
**Principle:** Every open port is a potential entry point

### Best Practices
- **Close Unnecessary Ports** - Only required ports open
- **Firewall Control** - Next-generation firewall implementation
- **Service Removal** - Remove unused services
- **Regular Scanning** - Nmap or similar port scanners
- **Ongoing Monitoring** - Continuous port monitoring

## Default Password Management
**Target:** Network devices and application management interfaces

### Critical Systems
- **Network Devices** - Routers, switches, firewalls
- **Management Interfaces** - Device administration portals
- **Application Interfaces** - Software management consoles

### Implementation
- **Change Default Passwords** - Strong, unique passwords
- **Regular Updates** - Password rotation policies
- **Access Control** - Limit management interface access
- **Monitoring** - Log all management access

## Software Removal
**Principle:** All software contains bugs and potential security risks

### Challenges
- **Patching Complexity** - Different update processes
- **Security Risks** - Unpatched vulnerabilities
- **Resource Consumption** - Unnecessary system overhead

### Solution
- **Remove Unused Software** - Eliminate security concerns
- **Regular Audits** - Identify unnecessary applications
- **Minimal Installation** - Install only required software
- **Ongoing Management** - Regular software inventory