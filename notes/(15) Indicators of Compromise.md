# 2.4.15 Indicators of Compromise

## Learning Objectives
- Identify common indicators of system compromise
- Understand behavioral analysis techniques
- Explain log analysis for threat detection

## Overview
Indicators of Compromise (IOC) are evidence that suggests unauthorized access or malicious activity has occurred on a system or network.

## Definition
**Indicators of Compromise:** Any evidence that someone has breached or gained access to your systems

## Common Indicators
- Unusual network activity patterns
- Changes to file hash values
- Irregular international traffic
- DNS data modifications
- Uncommon login patterns
- Spikes in read requests to specific files

## Specific Attack Indicators

### Account Lockout
**Indicators:**
- Credentials not working despite being correct
- Exceeded login attempt limits
- Accounts administratively disabled
- Part of larger attack campaign

**Analysis:** Determine if lockouts are legitimate or attack-related

### Concurrent Session Usage
**Principle:** Users cannot be in multiple locations simultaneously

**Indicators:**
- Multiple account logins from different geographic locations
- Simultaneous sessions from different IP addresses
- Impossible travel patterns in authentication logs

### Blocked Content
**Attacker Behavior:** Keep compromised systems accessible

**Blocked Resources:**
- Auto-update connections
- Security patch downloads
- Third-party anti-malware sites
- Malware removal tools

### Impossible Travel
**Analysis:** Authentication logs reveal impossible geographic patterns

**Example:**
- Login from Omaha, Nebraska
- Second login from Victoria, Australia (minutes later)
- Physically impossible travel time

### Resource Consumption
**Principle:** Every attacker action consumes system resources

**Indicators:**
- Unusual bandwidth spikes (especially during off-hours)
- File transfer activity at unusual times
- Firewall logs showing outgoing data transfers
- CPU/memory usage anomalies

### Resource Inaccessibility
**Types:**
- **Server Outages** - Systems not responding
- **Network Disruption** - May be cover for actual exploit
- **Encrypted Data** - Ransomware indicators
- **Account Lockouts** - Brute force attack results

### Out of Cycle Logging
**Definition:** Logging activity occurring at unexpected times

**Examples:**
- Security patches applied outside scheduled maintenance
- Firewall activity during off-hours
- Unusual timestamp patterns in logs

### Missing Logs
**Significance:** Logs provide evidence of system activity

**Types of Logs:**
- Authentication logs
- File access logs
- Firewall logs
- Proxy logs
- Server logs

**Red Flags:**
- Missing log entries
- Logs deleted or modified
- Unsecured log storage

### Published/Documented Attacks
**Indicators:**
- Company data published online
- Data posted on dark web forums
- Ransomware groups publishing victim data
- Raw data released without context

**Response:** Investigate source and scope of published data