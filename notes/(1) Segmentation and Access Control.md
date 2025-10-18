# 2.5.1 Segmentation and Access Control

## Learning Objectives
- Understand network segmentation benefits and methods
- Explain access control list implementation
- Describe application allow/deny policies

## Overview
Network segmentation and access control are fundamental security practices that limit the scope of security incidents and control access to resources.

## Network Segmentation
**Purpose:** Limit the scope of security events by dividing networks into smaller, controlled segments

### Segmentation Methods
- **Physical Segmentation** - Separate physical networks
- **Logical Segmentation** - VLANs and virtual networks
- **Virtual Segmentation** - Software-defined networking

### Benefits

#### Performance
- High-bandwidth applications get dedicated networks
- Optimized throughput without interference
- Reduced network congestion

#### Security
- Users cannot directly communicate with database servers
- Implemented through firewalls and access controls
- Reduced attack surface

#### Compliance
- Mandated segmentation (PCI DSS compliance)
- Easier change control and auditing
- Regulatory requirement fulfillment

## Access Control Lists (ACLs)
**Function:** Allow or disallow traffic based on defined criteria

### ACL Criteria
- Source and destination IP addresses
- Port numbers and protocols
- Time of day restrictions
- User and group memberships

### Implementation Examples
- **Bob:** Can read files
- **Fred:** Can access the network
- **James:** Can access 192.168.1.0/24 using only ports 80, 443, 8088

**Result:** Very granular control over network access

## Application Allow/Deny Policies
**Principle:** Any application can be dangerous due to vulnerabilities or malware

### Policy Types
- **Whitelist (Allow List)** - Nothing allowed except explicitly permitted
- **Blacklist (Deny List)** - Everything allowed except explicitly blocked

### Decision Points
**Operating System Level:**
- Application hash verification
- Digital certificate validation
- Path-based restrictions
- Network zone limitations

### Implementation Methods
- **Application Hash** - Prevent modified applications
- **Digital Certificates** - Trusted by Certificate Authority
- **Path Restrictions** - Only run applications from specific folders
- **Network Zone** - Applications can only run from designated network zones

## Best Practices
- Implement defense in depth
- Regular review and updates of access controls
- Monitor and log all access attempts
- Use principle of least privilege
- Regular security assessments