# 3.2.2 Intrusion Prevention

## Learning Objectives
- Understand intrusion prevention systems (IPS) and their functions
- Explain the difference between IDS and IPS
- Describe failure modes and device connections
- Identify active vs passive monitoring configurations

## Overview
Intrusion Prevention Systems monitor network traffic to detect and block malicious activities, providing real-time protection against exploits and attacks.

## Intrusion Prevention Systems (IPS)

### Core Functionality
**Purpose:** Watch network traffic and prevent malicious activities

**Threat Detection:**
- **Operating System Exploits** - Buffer overflows, privilege escalation
- **Web Application Attacks** - Cross-site scripting (XSS), SQL injection
- **Network Attacks** - Port scans, denial of service attempts
- **Malware Communication** - Command and control traffic

### IDS vs IPS Comparison

#### Intrusion Detection System (IDS)
- **Detection Only** - Alerts and alarms when threats are detected
- **Passive Response** - Does not block traffic automatically
- **Network Impact** - Minimal impact on network performance
- **Use Case** - Monitoring and alerting

#### Intrusion Prevention System (IPS)
- **Detection and Prevention** - Stops threats before they enter the network
- **Active Response** - Automatically blocks malicious traffic
- **Network Impact** - May impact performance due to inline processing
- **Use Case** - Active protection and threat blocking

## Failure Modes

### System Failure Scenarios
**Question:** "Devices can fail! What happens to network traffic?"

#### Fail-Open Mode
- **Behavior** - When system fails, data continues to flow
- **Advantage** - Maintains network availability
- **Risk** - Security protection is lost during failure
- **Use Case** - When availability is more critical than security

#### Fail-Closed Mode
- **Behavior** - When system fails, data does not flow
- **Advantage** - Maintains security posture
- **Risk** - Network availability is lost during failure
- **Use Case** - When security is more critical than availability

## Device Connections

### Active Monitoring Configuration
**Implementation:** System is connected inline with network traffic

**Characteristics:**
- **Inline Processing** - All traffic passes through the IPS
- **Real-time Blocking** - Immediate threat prevention
- **Traffic Analysis** - Complete packet inspection
- **Performance Impact** - May introduce latency

**Example Configuration:**
```
Internet → Firewall → IPS → Core Switch
```

**Benefits:**
- **Immediate Protection** - Blocks threats in real-time
- **Complete Visibility** - Analyzes all network traffic
- **Automated Response** - No manual intervention required

### Passive Monitoring Configuration
**Implementation:** Copy of network traffic is examined using taps or ports

**Characteristics:**
- **Traffic Copying** - Switch sends copy to IPS
- **No Traffic Blocking** - Cannot stop threats in real-time
- **Detection Only** - Alerts and logging capabilities
- **Minimal Performance Impact** - Does not affect network flow

**Traffic Distribution:**
- **Primary Copy** - Sent to original destination
- **Secondary Copy** - Sent to IPS for analysis

**Use Cases:**
- **Monitoring** - Network visibility and threat detection
- **Forensics** - Post-incident analysis
- **Compliance** - Audit trail and logging requirements

## Best Practices
- **Regular Updates** - Keep threat signatures current
- **Tuning** - Adjust rules to reduce false positives
- **Monitoring** - Continuous system health monitoring
- **Backup Plans** - Implement failover procedures
- **Performance Testing** - Regular throughput validation
- **Staff Training** - Ensure proper system management