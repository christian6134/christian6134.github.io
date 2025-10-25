# Task 1 - What is an IDS?

## Learning Objectives
- Understand the difference between IDS and firewalls
- Learn about types of IDS and their detection capabilities
- Master how Snort IDS works
- Understand default and custom rules in Snort IDS
- Practice making custom rules in Snort IDS

## Overview
An Intrusion Detection System (IDS) is a security solution that **detects malicious activity within a network** if an attacker has successfully **bypassed the firewall**. Think of it like a **surveillance camera inside a bank** - while firewalls guard the perimeter, IDS monitors activities inside to detect suspicious behavior that made it past the first line of defense.

### IDS vs Firewall

**Firewall Function**
- Deployed **on the boundary** of a network
- Protects **incoming and outgoing traffic**
- First line of defense
- Prevents unauthorized access

**IDS Function**
- **Detects activities of connections** that passed through the firewall
- Monitors internal network traffic
- Identifies malicious behavior
- Alerts on suspicious activities

**Key Difference**
- **Firewalls**: Preventive control at network boundary
- **IDS**: Detective control for internal monitoring
- **Complementary**: Work together for defense in depth

### What is an IDS?

**Core Definition**
- **Detects malicious activity** within a network
- **Monitors traffic** that has bypassed the firewall
- **Alerts security teams** to suspicious activities
- **Surveillance system** for internal network

**IDS Analogy**
- Like a **surveillance camera inside a bank**
- Firewall is the bank's locked doors
- IDS watches what happens inside
- Alerts guards to suspicious behavior

### IDS Detection Capabilities

**Signature-Based Detection**
- Matches traffic patterns against known attack signatures
- Fast and accurate for known threats
- Requires regular signature updates
- Limited against zero-day attacks

**Anomaly-Based Detection**
- Identifies deviations from normal behavior
- Can detect unknown threats
- May generate more false positives
- Requires baseline establishment

**Protocol Analysis**
- Validates protocol compliance
- Detects protocol anomalies and violations
- Identifies evasion techniques
- Deep packet inspection

### Types of IDS

**Network-Based IDS (NIDS)**
- Monitors network traffic
- Deployed at strategic network points
- Analyzes packets in real-time
- Provides network-wide visibility

**Host-Based IDS (HIDS)**
- Monitors individual hosts
- Analyzes system logs and file changes
- Detects local threats
- Provides per-host protection

**Hybrid IDS**
- Combines NIDS and HIDS capabilities
- Comprehensive detection coverage
- Correlates network and host events
- Enhanced threat detection

### Snort IDS

**Snort Overview**
- Open-source IDS/IPS solution
- Industry-standard detection system
- Rule-based detection engine
- Extensive community support

**Snort Capabilities**
- Real-time traffic analysis
- Packet logging
- Protocol analysis
- Content matching and searching

**Default Rules**
- Pre-configured detection signatures
- Cover common attack patterns
- Regularly updated by community
- Ready-to-use detection capabilities

**Custom Rules**
- Create organization-specific rules
- Tailor detection to environment
- Address unique security requirements
- Enhance detection capabilities

### Rule Creation

**Rule Components**
- Rule header (action, protocol, addresses, ports)
- Rule options (content, flags, metadata)
- Alert actions and logging
- Performance optimization

**Rule Syntax**
- Structured rule format
- Pattern matching capabilities
- Flexible detection logic
- Regular expression support

### Practical Applications

**Security Monitoring**
- Continuous network surveillance
- Real-time threat detection
- Incident identification
- Security event alerting

**Threat Hunting**
- Proactive threat detection
- Behavioral analysis
- Advanced persistent threat detection
- Custom rule development

**Compliance**
- Meet regulatory requirements
- Audit trail generation
- Security control validation
- Incident documentation

## Best Practices
- Deploy IDS strategically across network
- Regularly update detection signatures
- Tune rules to reduce false positives
- Monitor IDS alerts and respond promptly
- Create custom rules for environment-specific threats
- Integrate IDS with SIEM for centralized monitoring