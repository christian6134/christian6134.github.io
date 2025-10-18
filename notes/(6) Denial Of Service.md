# 2.4.6 Denial of Service

## Learning Objectives
- Understand DoS and DDoS attack mechanisms
- Explain botnets and their role in attacks
- Describe amplification and reflection attacks

## Overview
Denial of Service (DoS) attacks prevent legitimate users from accessing services by overwhelming systems with malicious traffic or exploiting vulnerabilities.

## Denial of Service (DoS)
**Definition:** Attack that forces a service to fail, making it unavailable to legitimate users

**Attack Methods:**
- Exploit design failures or vulnerabilities
- Overwhelm system resources
- Cause system crashes or slowdowns
- Serve as distraction for other attacks

**Protection:**
- Keep systems updated with patches
- Implement rate limiting and traffic filtering
- Use load balancing and redundancy
- Monitor for unusual traffic patterns

## Distributed Denial of Service (DDoS)
**Definition:** Coordinated attack using multiple devices worldwide to overwhelm a target

**Characteristics:**
- Uses multiple compromised devices
- Generates massive traffic spikes
- Consumes all available bandwidth
- Difficult to mitigate due to scale

### Botnets
**Definition:** Networks of compromised devices (robots) under attacker control

**Botnet Capabilities:**
- Coordinated attacks on specific targets
- Distributed processing power
- Geographic distribution
- Difficult to trace and shut down

**Common Botnet Types:**
- **HIVE** - Coordinated attack networks
- **Mirai** - IoT device botnets
- **Zeus** - Banking trojan botnets

## Amplification and Reflection Attacks
**Principle:** Turn small attacks into large attacks using legitimate services

### DNS Amplification
**Process:**
1. Attacker sends small DNS queries with spoofed victim IP
2. DNS servers respond with large responses to victim
3. Small attack becomes massive traffic flood

**Why Effective:**
- DNS responses are much larger than queries
- DNS servers don't verify request authenticity
- Amplification ratios can be 50:1 or higher

![DDoS Amplification](Photos/DDoS-Amplification.png)

### Other Amplification Vectors
- **NTP Amplification** - Network Time Protocol
- **SSDP Amplification** - Simple Service Discovery Protocol
- **Memcached Amplification** - Database caching protocol

## Friendly DoS
**Definition:** Unintentional DoS caused by misconfigurations or legitimate activities

**Examples:**
- Layer 2 loops without Spanning Tree Protocol
- Large downloads over limited bandwidth connections
- Misconfigured network equipment
- Resource-intensive legitimate applications

**Prevention:**
- Proper network configuration
- Bandwidth management
- Resource monitoring
- Capacity planning