# 4.1.2 Hardening Techniques

## Learning Objectives
- Understand system hardening concepts and attack surface reduction
- Explain service hardening and port/protocol management
- Describe network hardening and VLAN segmentation
- Identify OS hardening, cloud infrastructure, and SCADA/ICS security

## Overview
Hardening involves changing system and application settings to increase overall security and reduce vulnerabilities to attack by minimizing the attack surface through various techniques and configurations.

## Hardening Fundamentals

### Core Concept
**Definition:** Hardening endpoints and other systems relies on techniques that protect the system and software that runs on it

**Key Principle:** Change system/application settings to increase security and reduce vulnerabilities

**Attack Surface Consideration:** Considering the attack surface is vital for effective hardening

### Key Hardening Items
**Essential Hardening Techniques:**
- **Encryption** - Protect data at rest and in transit
- **Endpoint Protection** - Antivirus, antimalware, EDR solutions
- **Host-Based Firewalls** - Local firewall protection
- **Host-Based Intrusion Prevention** - HIPS for local threat prevention
- **Disabling Ports and Protocols** - Close unnecessary network services
- **Changing Default Passwords** - Replace default credentials
- **Removing Bloatware** - Eliminate unnecessary software

## Service Hardening

### Port and Service Reduction
**Primary Strategy:** Reduce open ports and services by disabling unnecessary ports and protocols

**Benefits:**
- **Attack Surface Reduction** - One of the fastest ways to decrease attack surface
- **Target Prioritization** - Port scanners help prioritize hardening targets
- **Security Improvement** - Immediate security improvement

### Hardening Rules
**Rule of Thumb:** Only services and ports that must be available for necessary services should be open

**Access Limitation:** Those ports and services should be limited to only networks or systems that need to interact with them

**Implementation:**
- **Windows:** Use `services.msc` console to disable or enable services
- **Ubuntu Linux:** Use `service --status-all` to list running services
- **Service Control:** Use `sudo service [service name] stop/start` for temporary control
- **Permanent Changes:** Configure `update-rc.d` script for permanent service stoppage

### Common Ports and Services
**Critical Understanding:** Understand the concept of disabling services to reduce attack surface

**Ongoing Maintenance:** Regular review and maintenance required to ensure new services don't appear over time

**Common Services to Review:**
- **Web Services** - HTTP (80), HTTPS (443)
- **Email Services** - SMTP (25), POP3 (110), IMAP (143)
- **File Services** - FTP (21), SMB (445)
- **Remote Access** - SSH (22), RDP (3389), Telnet (23)
- **Database Services** - MySQL (3306), SQL Server (1433)

## Network Hardening

### VLAN Segmentation
**Common Technique:** Use VLANs (Virtual Local Area Networks) for network segmentation

**Segmentation Benefits:**
- **Trust Level Separation** - Segment different trust levels
- **User Group Isolation** - Separate user groups
- **System Isolation** - Isolate different system types
- **IoT Protection** - Place IoT devices on separate, protected VLANs

**Implementation:**
- **Access Controls** - Implement appropriate access controls
- **Dedicated Security** - Use dedicated network security protections
- **Vulnerable Device Protection** - Ensure vulnerable devices are protected
- **Traffic Isolation** - Isolate traffic between segments

## Default Password Management

### Password Security
**Common Hardening Technique:** Changing default passwords

**Critical Importance:**
- **Default Credentials** - Many devices ship with known default passwords
- **Attack Vector** - Default passwords are common attack vectors
- **Compliance** - Required by most security standards
- **Best Practice** - Essential security practice

**Implementation:**
- **Inventory Management** - Maintain inventory of all devices
- **Password Policies** - Implement strong password policies
- **Regular Audits** - Regular audits of default passwords
- **Documentation** - Document all password changes

## Removing Bloatware

### Unnecessary Software Elimination
**Definition:** Removing unnecessary software to reduce attack surface

**Benefits:**
- **Patching Reduction** - Reduce time spent on patching
- **Monitoring Reduction** - Reduce monitoring overhead
- **Attack Surface Reduction** - Eliminate potential vulnerabilities
- **Performance Improvement** - Improve system performance

**Implementation Strategies:**
- **Custom Images** - Organizations build their own system images
- **Fresh Installation** - Reinstall fresh operating system without unwanted software
- **Software Audits** - Regular audits of installed software
- **Approved Software Lists** - Maintain lists of approved software

## OS Hardening

### Operating System Security
**Core Concept:** Change settings to match desired security stances for given systems

**Standards and Benchmarks:**
- **CIS Benchmarks** - Center for Internet Security benchmarks
- **Popular Standards** - Use popular benchmarks as baselines
- **Customization** - Modify standards to meet organizational needs
- **Documentation** - Document all configuration changes

### CIS Benchmark Examples
**Password History:** Set to remember 24 or more passwords
**Maximum Password Age:** Set to "365 or fewer days, but no 0"
- **Prevents Password Cycling** - Prevents users from changing password 24 times to get back to same password
- **Annual Requirement** - Requires password changes every year

**Minimum Password Length:** Set to 14 or more characters
**Password Complexity:** Require complexity in passwords
**Reversible Encryption:** Disable storage of passwords using reversible encryption

### OS Hardening Benefits
**Big Picture:** Operating system hardening uses system settings to reduce attack surface

**Support Tools:** Tools and standards exist to help with hardening
**Key Activities:** Assessing, auditing, and maintaining OS hardening is essential

## Cloud Infrastructure Hardening

### Secure Cloud Management
**Secure Workstation:** Use secure cloud management workstation
**Least Privilege:** Implement least privilege access principles
**EDR Configuration:** Configure Endpoint Detection and Response on all devices accessing cloud

**Requirements:**
- **All Devices Secure** - All devices accessing cloud should be secure
- **Access Control** - Implement proper access controls
- **Monitoring** - Monitor cloud access and activities
- **Compliance** - Ensure compliance with cloud security standards

## SCADA/ICS Hardening

### Industrial Control Systems
**Definition:** PC manages equipment for power generation and manufacturing

**Characteristics:**
- **Large Scale Systems** - Industrial-scale systems
- **Distributed Control** - Distributed control systems
- **Real-Time Information** - Real-time system information
- **System Control** - Direct system control capabilities

**Security Requirements:**
- **Extensive Segmentation** - Require extensive network segmentation
- **Air-Gapped Networks** - Isolate from internet-connected networks
- **Specialized Security** - Use specialized industrial security solutions
- **Regular Updates** - Regular security updates and patches

**Challenges:**
- **Legacy Systems** - Often use legacy operating systems
- **Update Limitations** - Limited ability to apply updates
- **Availability Requirements** - High availability requirements
- **Specialized Knowledge** - Require specialized security knowledge

## Best Practices
- **Comprehensive Approach** - Implement multiple hardening techniques
- **Regular Audits** - Regular security audits and assessments
- **Documentation** - Document all hardening activities
- **Testing** - Test hardening changes before deployment
- **Monitoring** - Continuous monitoring of hardened systems
- **Staff Training** - Train staff on hardening techniques
- **Standards Compliance** - Follow established security standards
- **Change Management** - Implement proper change management