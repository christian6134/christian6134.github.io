# 2.5.2 Mitigation Techniques

## Learning Objectives
- Understand key mitigation strategies for security incidents
- Explain patch management and encryption controls
- Describe monitoring and least privilege principles

## Overview
Mitigation techniques reduce the impact of security incidents through proactive measures including patching, encryption, monitoring, and access controls.

## Patching
**Purpose:** System stability and security fixes

### Patch Management
- **Monthly Updates** - Regular security patches
- **Third-Party Updates** - Application and driver updates
- **Auto-Update** - Automated patch deployment
- **Emergency Updates** - Out-of-band critical patches

### Implementation
- Centralized patch management systems
- Testing patches before deployment
- Rollback procedures for problematic patches
- Regular vulnerability scanning

## Encryption
**Purpose:** Prevent unauthorized access to data

### Encryption Types
- **File System Encryption** - Protect application data files
- **File Level Encryption** - Windows EFS (Encrypting File System)
- **Full Disk Encryption (FDE)** - Encrypt entire drive (BitLocker, FileVault)
- **Application Data Encryption** - Managed by applications

### Benefits
- Data protection at rest
- Compliance with data protection regulations
- Defense against data theft
- Always-on protection

## Monitoring
**Purpose:** Aggregate information from security devices and sensors

### Monitoring Components
**Sensors:**
- Intrusion prevention systems
- Firewall logs
- Authentication logs
- Web server access logs
- Database transaction logs
- Email logs

**Collectors:**
- SIEM (Security Information and Event Management) console
- Correlation engines
- Real-time analysis tools

### Benefits
- Centralized security visibility
- Correlation of diverse data sources
- Rapid incident detection
- Compliance reporting

## Least Privilege
**Principle:** Rights and permissions set to bare minimum required

### Implementation
- Limit user account permissions
- Avoid administrative privileges for regular users
- Limit scope of malicious behavior
- Regular access reviews

### Benefits
- Reduced attack surface
- Limited damage from compromised accounts
- Easier access management
- Compliance with security frameworks

## Configuration Enforcement
**Purpose:** Ensure systems meet security standards

### Posture Assessment
**Checks Performed:**
- Operating system patches
- EDR (Endpoint Detection and Response) version
- Firewall and EDR status
- Certificate validity
- Security policy compliance

### Non-Compliant Systems
- Private VLAN with limited access
- Quarantine until corrections made
- Automatic remediation where possible
- Regular compliance reporting

## Decommissioning
**Purpose:** Secure disposal of systems and data

### Policy Requirements
- Formal decommissioning procedures
- Secure data destruction
- Physical device disposal
- Documentation of disposal process

### Device Types
- Hard disk drives (HDD)
- Solid state drives (SSD)
- USB storage devices
- Mobile devices

### Options
- **Recycling** - Secure reuse in other systems
- **Destruction** - Physical destruction of devices
- **Certified Disposal** - Third-party secure disposal services