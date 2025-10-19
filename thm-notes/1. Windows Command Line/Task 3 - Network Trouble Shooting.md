# Task 3 - Network Troubleshooting

## Learning Objectives
- Master essential Windows CLI network troubleshooting commands
- Understand IP configuration and network connectivity testing
- Learn route tracing and DNS resolution techniques
- Identify network connections and listening ports

## Overview
Network troubleshooting is a critical skill for cybersecurity professionals. Understanding how to diagnose network issues, verify connectivity, and analyze network traffic through command line tools is essential for maintaining secure and functional network environments.

### Network Configuration Commands

**IPCONFIG Command**
```cmd
ipconfig
```
- Displays basic network configuration
- Shows IP address, subnet mask, and default gateway
- Quick network interface overview

```cmd
ipconfig /all
```
- Comprehensive network configuration details
- Shows all network adapters and their settings
- Displays DNS servers and DHCP information
- Essential for network troubleshooting

### Connectivity Testing

**PING Command**
```cmd
ping target_name
ping example.com
```
- Tests network connectivity to remote hosts
- Verifies if target server is reachable
- Measures round-trip time and packet loss
- Basic network health check

**TRACERT Command (Traceroute)**
```cmd
tracert destination
```
- Traces network route to destination
- Shows each hop in the network path
- Identifies where packets are dropped (TTL reached 0)
- Useful for diagnosing routing issues

### DNS Resolution

**NSLOOKUP Command**
```cmd
nslookup domain_name
```
- Performs DNS lookups
- Converts hostnames to IP addresses
- Resolves domain names to IP addresses
- Essential for DNS troubleshooting

### Network Connection Analysis

**NETSTAT Command**
```cmd
netstat
```
- Displays current network connections
- Shows listening ports and established connections
- No arguments shows established connections only
- Port 22 typically indicates SSH connections

**NETSTAT Advanced Options**
```cmd
netstat -a
```
- Displays all connections and listening ports
- Shows both active and passive connections

```cmd
netstat -b
```
- Shows program associated with each connection
- Identifies which application is using specific ports

```cmd
netstat -o
```
- Reveals Process ID (PID) for each connection
- Links network activity to specific processes

```cmd
netstat -n
```
- Shows numerical form for addresses and ports
- Faster output without DNS resolution

### Common Network Ports
- **Port 22**: SSH (Secure Shell)
- **Port 80**: HTTP
- **Port 443**: HTTPS
- **Port 21**: FTP
- **Port 25**: SMTP

## Practical Applications
- Network connectivity troubleshooting
- Security assessment and port scanning
- Monitoring network connections
- Identifying suspicious network activity

## Best Practices
- Use appropriate netstat flags for specific information needs
- Combine multiple commands for comprehensive network analysis
- Document network configurations for troubleshooting reference
- Monitor for unusual network connections or listening ports