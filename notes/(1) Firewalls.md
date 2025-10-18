# 4.5.1 Firewalls

## Learning Objectives
- Understand network-based firewalls and their inline operation
- Explain NGFW capabilities and application layer recognition
- Describe firewall rules, access control lists, and implicit deny
- Identify screened subnets, IPS integration, and traffic analysis methods

## Overview
Firewalls provide essential network security by filtering traffic, managing access control, and protecting network boundaries through various technologies including traditional firewalls, next-generation firewalls, and integrated security features.

## Network-Based Firewalls

### Inline Operation
**Positioning:** In-line with your network for traffic filtering

**Core Functions:**
- **Traffic Filtering** - Filter traffic by port number or application (NGFW)
- **Traffic Encryption** - Encrypt traffic for secure communications
- **VPN Capabilities** - Provide VPN between sites
- **Layer 3 Functionality** - Most firewalls can be layer 3 devices (routers)

**Network Positioning:**
- **Boundary Placement** - Sits on boundary between external and internal networks
- **NAT Implementation** - Network Address Translation
- **Dynamic Routing** - Support for dynamic routing protocols
- **Traffic Control** - Control traffic flow between networks

## NGFW (Next-Generation Firewall)

### Application Layer Recognition
**Operating Layer:** OSI Application Layer 7

**Alternative Names:**
- **Application Layer Gateway** - Application-aware gateway
- **Deep Packet Inspection** - Deep packet inspection capability
- **Application Firewall** - Application-specific firewall

**Advanced Capabilities:**
- **Application Recognition** - CAN RECOGNIZE Applications
- **Advanced Decodes** - Requires advanced decodes
- **Packet Analysis** - Analyzes all packet captures
- **Security Decisions** - Make security decisions based on analysis

**Benefits:**
- **Application Awareness** - Understand application protocols
- **Granular Control** - Granular application control
- **Threat Detection** - Detect application-layer threats
- **Policy Enforcement** - Enforce application-specific policies

## Ports and Protocols

### Traditional Firewall Functionality
**Decision Making:** Make forwarding decisions based on protocol (TCP/UDP) and port number

**Traditional Firewall:**
- **Protocol-Based** - Based on destination protocol and port
- **Port-Based Rules** - Rules based on port numbers
- **Protocol Filtering** - Filter by transport protocol
- **Basic Security** - Basic security functionality

**NGFW Enhancement:** Add to NGFW for additional security

**Implementation:**
- **Rule-Based** - Implement port and protocol rules
- **Traffic Classification** - Classify traffic by port/protocol
- **Access Control** - Control access based on ports
- **Security Policies** - Implement security policies

## Firewall Rules

### Logical Path Management
**Rule Structure:** Logical path for traffic processing

**Rule Specificity:**
- **General Rules** - Can be very general
- **Specific Rules** - Can be very specific
- **Rule Order** - Specific rules are at the top
- **Rule Processing** - Process rules in order

### Implicit Deny
**Default Behavior:** Most firewalls include deny at bottom

**Security Principle:** Everything that does not have a match will be denied

**Implementation:**
- **Default Deny** - Deny by default
- **Explicit Allow** - Allow only explicitly permitted traffic
- **Security Posture** - Maintain secure default posture
- **Rule Management** - Manage allow rules carefully

### Access Control Lists (ACLs)
**Traffic Control:** Allow or disallow traffic

**ACL Parameters:**
- **Source IP** - Source IP address
- **Destination IP** - Destination IP address
- **Port Number** - Port number specification
- **Time of Day** - Time-based access control

**ACL Benefits:**
- **Granular Control** - Granular traffic control
- **Flexible Rules** - Flexible rule configuration
- **Time-Based** - Time-based access control
- **Audit Trail** - Maintain audit trail

## Screened Subnet

### Network Segmentation
**Definition:** Ingress/Egress separation between internal network and internet

**Architecture:**
- **Firewall Connection** - Firewall connects to internal network
- **Subnet Connection** - Firewall also connects to screened subnet
- **Traffic Segmentation** - Segment internet traffic into another subnet
- **Security Isolation** - Isolate different network segments

**Benefits:**
- **Traffic Control** - Control traffic between segments
- **Security Isolation** - Isolate network segments
- **DMZ Functionality** - Provide DMZ functionality
- **Attack Containment** - Contain attacks within segments

## IPS Integration

### Intrusion Prevention System
**Integration:** Usually integrated into NGFW

**Malicious Traffic Detection:** Different ways to find malicious traffic

**Detection Methods:**
- **Traffic Analysis** - Look at traffic as it passes by
- **Signature-Based Detection** - Look for perfect match
- **Anomaly-Based Detection** - Build baseline of normal traffic

### Signature-Based Detection
**Method:** Look for perfect match with known attack signatures

**Characteristics:**
- **Known Attacks** - Detect known attack patterns
- **Signature Database** - Maintain signature database
- **Pattern Matching** - Match traffic patterns
- **False Positives** - May generate false positives

### Anomaly-Based Detection
**Method:** Build baseline of what is normal

**Process:**
- **Baseline Establishment** - Establish normal traffic baseline
- **Pattern Analysis** - Analyze traffic patterns
- **Anomaly Detection** - Flag unusual traffic patterns
- **Behavioral Analysis** - Analyze traffic behavior

**Benefits:**
- **Unknown Threats** - Detect unknown threats
- **Behavioral Analysis** - Analyze traffic behavior
- **Adaptive** - Adapt to changing traffic patterns
- **Zero-Day Protection** - Protect against zero-day attacks

## Firewall Management

### Configuration Management
- **Rule Management** - Manage firewall rules
- **Policy Updates** - Update security policies
- **Monitoring** - Monitor firewall performance
- **Maintenance** - Regular maintenance and updates

### Security Best Practices
- **Least Privilege** - Implement least privilege access
- **Regular Updates** - Keep firewall firmware updated
- **Rule Review** - Regularly review firewall rules
- **Monitoring** - Monitor firewall logs and alerts

## Best Practices
- **Defense in Depth** - Implement multiple security layers
- **Regular Updates** - Keep firewalls updated
- **Rule Management** - Manage firewall rules effectively
- **Monitoring** - Monitor firewall performance and logs
- **Documentation** - Document firewall configurations
- **Testing** - Test firewall rules and policies
- **Staff Training** - Train staff on firewall management
- **Incident Response** - Integrate with incident response procedures