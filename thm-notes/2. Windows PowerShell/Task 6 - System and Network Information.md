# Task 6 - System and Network Information

## Learning Objectives
- Master PowerShell commands for comprehensive system information gathering
- Learn local user account management and monitoring
- Understand network configuration and IP address management
- Practice system information retrieval techniques

## Overview
PowerShell provides powerful cmdlets for gathering comprehensive system and network information. These commands are essential for system administration, security analysis, and troubleshooting. Understanding how to retrieve detailed system information through PowerShell is crucial for cybersecurity professionals.

### System Information Commands

**Get-ComputerInfo**
```powershell
Get-ComputerInfo
```
- Retrieves comprehensive system information
- PowerShell counterpart to `systeminfo` command
- Provides detailed system specifications

**Information Categories**
- Operating System Information
- Hardware Specifications
- BIOS Details
- System Configuration
- Performance Metrics

### User Account Management

**Get-LocalUser**
```powershell
Get-LocalUser
```
- Lists all local user accounts on the system
- Shows detailed account information

**User Account Details**
- Username
- Account Status (Enabled/Disabled)
- Description
- Last Logon Information
- Account Creation Date

**Advanced User Queries**
```powershell
Get-LocalUser | Where-Object -Property "Enabled" -eq $true
Get-LocalUser | Select-Object Name, Enabled, Description
```

### Network Configuration

**Get-NetIPConfiguration**
```powershell
Get-NetIPConfiguration
ipconfig  # Alias
```
- Provides detailed network interface information
- Shows IP addresses, DNS servers, and gateway configurations
- Essential for network troubleshooting

**Get-NetIPAddress**
```powershell
Get-NetIPAddress
```
- Shows details about IP addresses assigned to network interfaces
- Displays IP address types (IPv4/IPv6)
- Shows interface indexes and prefixes

**Network Information Examples**
```powershell
# Get all IPv4 addresses
Get-NetIPAddress -AddressFamily IPv4

# Get network configuration for specific interface
Get-NetIPConfiguration -InterfaceIndex 1
```

### Advanced System Queries

**Combining Commands**
```powershell
# Get system info with specific properties
Get-ComputerInfo | Select-Object WindowsProductName, TotalPhysicalMemory, CsProcessors

# Get enabled users with descriptions
Get-LocalUser | Where-Object Enabled -eq $true | Select-Object Name, Description
```

**Filtering and Sorting**
```powershell
# Sort network interfaces by IP address
Get-NetIPAddress | Sort-Object IPAddress

# Get largest network interfaces
Get-NetIPConfiguration | Sort-Object InterfaceMetric
```

### Security Applications

**System Auditing**
- User account enumeration
- Network configuration verification
- System specification documentation
- Compliance checking

**Incident Response**
- System information gathering
- Network connection analysis
- User account status verification
- System configuration documentation

## Best Practices
- Use appropriate cmdlets for specific information needs
- Combine commands for comprehensive system profiles
- Document system information for reference
- Verify information accuracy for critical decisions
- Use filtering to focus on relevant data