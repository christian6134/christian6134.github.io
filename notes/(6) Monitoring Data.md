# 4.5.6 Monitoring Data

## Learning Objectives
- Understand file integrity monitoring and critical file protection
- Explain Windows SFC and Linux Tripwire implementations
- Describe Data Loss Prevention (DLP) systems and data protection
- Identify USB blocking, cloud-based DLP, and email DLP capabilities

## Overview
Data monitoring involves comprehensive protection of data through file integrity monitoring, data loss prevention systems, and various DLP implementations to protect data at rest, in transit, and in use across different environments.

## File Integrity Monitoring

### Critical File Protection
**Core Concept:** Some files should NEVER change

**File Categories:**
- **Operating System Files** - Critical OS files that shouldn't change
- **Application Files** - Important application files
- **Configuration Files** - System configuration files
- **Security Files** - Security-related files

**Monitoring Requirements:**
- **Change Detection** - Detect unauthorized file changes
- **Baseline Establishment** - Establish file baselines
- **Real-Time Monitoring** - Real-time change detection
- **Alert Generation** - Generate alerts for changes

**Benefits:**
- **Integrity Protection** - Protect file integrity
- **Malware Detection** - Detect malware modifications
- **Compliance** - Meet regulatory compliance
- **Incident Detection** - Detect security incidents

## Windows SFC (System File Checker)

### Windows File Protection
**Purpose:** Scans all critical operating system files

**SFC Functions:**
- **File Scanning** - Scan critical OS files
- **Integrity Verification** - Verify file integrity
- **File Replacement** - Replace modified files with good versions
- **System Repair** - Repair system file issues

**SFC Benefits:**
- **System Integrity** - Maintain system integrity
- **Malware Recovery** - Recover from malware damage
- **System Stability** - Maintain system stability
- **Automated Repair** - Automated system repair

**Implementation:**
- **Scheduled Scans** - Schedule regular scans
- **Manual Scans** - Perform manual scans
- **Integration** - Integrate with monitoring systems
- **Reporting** - Generate scan reports

## Linux Tripwire

### Linux File Integrity
**Purpose:** Real-time monitoring of critical files

**Tripwire Features:**
- **Real-Time Monitoring** - Real-time file monitoring
- **Change Detection** - Detect file changes immediately
- **Alert Generation** - Generate immediate alerts
- **Baseline Management** - Manage file baselines

**Tripwire Benefits:**
- **Immediate Detection** - Immediate change detection
- **Comprehensive Coverage** - Comprehensive file coverage
- **Customizable** - Customizable monitoring rules
- **Integration** - Integration with security systems

**Implementation:**
- **Configuration** - Configure monitoring rules
- **Baseline Creation** - Create file baselines
- **Alert Setup** - Set up alert mechanisms
- **Integration** - Integrate with SIEM systems

## Host-Based IPS

### File Verification Capabilities
**Definition:** Host-based Intrusion Prevention System

**Key Difference:** Different than network-based intrusion system

**File Verification:** This IPS can verify FILES

**IPS Capabilities:**
- **File Monitoring** - Monitor file changes
- **Behavior Analysis** - Analyze file behavior
- **Threat Detection** - Detect file-based threats
- **Response Actions** - Take response actions

**Benefits:**
- **File Protection** - Protect critical files
- **Threat Prevention** - Prevent file-based threats
- **Real-Time Response** - Real-time threat response
- **Comprehensive Protection** - Comprehensive file protection

## Data Loss Prevention (DLP)

### Data Protection Strategy
**Core Principle:** Stop the data before attackers get it

**Data "Leakage" Prevention:** Prevent sensitive information leakage

**Implementation Requirement:** Requires various solutions in different places

**DLP Objectives:**
- **Data Discovery** - Discover sensitive data
- **Data Classification** - Classify data by sensitivity
- **Data Monitoring** - Monitor data access and usage
- **Data Protection** - Protect data from unauthorized access

## DLP Systems

### Endpoint DLP
**Location:** On your computer (endpoint)

**Data State:** Data in Use

**Endpoint Capabilities:**
- **File Monitoring** - Monitor file access
- **Application Control** - Control application access
- **Print Prevention** - Prevent unauthorized printing
- **Copy Prevention** - Prevent unauthorized copying

**USB Blocking:**
- **Removable Media Control** - Control removable media
- **Flash Drive Blocking** - Block flash drives
- **Storage Device Control** - Control storage devices
- **Data Transfer Prevention** - Prevent unauthorized data transfer

### Network DLP
**Location:** On your network

**Data State:** Data in motion

**Network Capabilities:**
- **Traffic Analysis** - Analyze network traffic
- **Content Inspection** - Inspect data content
- **Policy Enforcement** - Enforce data policies
- **Blocking Actions** - Block unauthorized transfers

### Server DLP
**Location:** On your server

**Data State:** Data at rest

**Server Capabilities:**
- **Data Discovery** - Discover sensitive data
- **Access Control** - Control data access
- **Encryption** - Encrypt sensitive data
- **Audit Logging** - Log data access

## Cloud-Based DLP

### Cloud DLP Features
**Location:** Between users and internet

**Architecture:** NO hardware, NO software required

**Monitoring Capabilities:**
- **Traffic Monitoring** - Watch network traffic
- **Content Analysis** - Analyze data content
- **Policy Enforcement** - Enforce data policies
- **Threat Detection** - Detect data threats

**Custom Data Protection:**
- **Custom Data Strings** - Block custom defined data strings
- **Unique Data** - Unique data for your organization
- **Pattern Matching** - Match data patterns
- **Content Filtering** - Filter sensitive content

**Access Control:**
- **URL Management** - Manage access to URLs
- **Cloud Storage Prevention** - Prevent file transfers to cloud storage
- **Application Control** - Control application access
- **User Management** - Manage user access

**Security Features:**
- **Malware Blocking** - Block viruses and malware
- **Threat Prevention** - Prevent various threats
- **Content Filtering** - Filter malicious content
- **Policy Enforcement** - Enforce security policies

## DLP Email

### Email Security Focus
**Critical Risk:** Email is the most critical risk vector

**Email Inspection:** Check every email inbound and outbound

**Implementation Options:**
- **Internal System** - Internal email DLP system
- **Cloud-Based** - Cloud-based email DLP
- **Hybrid Approach** - Hybrid implementation

**Email DLP Capabilities:**
- **Keyword Detection** - Look for keywords
- **Impostor Identification** - Identify impostors (spoofed)
- **Message Quarantine** - Quarantine suspicious messages
- **Content Analysis** - Analyze email content

**Email Protection:**
- **Phishing Prevention** - Prevent phishing attacks
- **Data Leakage Prevention** - Prevent data leakage
- **Malware Protection** - Protect against malware
- **Compliance** - Meet email compliance requirements

## Best Practices
- **Comprehensive Coverage** - Cover all data states
- **Multi-Layer Protection** - Implement multiple DLP layers
- **Regular Monitoring** - Monitor data continuously
- **Policy Enforcement** - Enforce data policies strictly
- **User Training** - Train users on data protection
- **Incident Response** - Have incident response procedures
- **Compliance** - Ensure regulatory compliance
- **Continuous Improvement** - Continuously improve DLP