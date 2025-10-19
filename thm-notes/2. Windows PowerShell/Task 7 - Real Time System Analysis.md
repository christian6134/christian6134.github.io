# Task 7 - Real Time System Analysis

## Learning Objectives
- Master PowerShell commands for real-time system monitoring
- Learn process and service monitoring techniques
- Understand network connection analysis
- Practice file integrity verification methods

## Overview
Real-time system analysis involves monitoring dynamic aspects of a system including running processes, services, and network connections. PowerShell provides powerful cmdlets for live system monitoring, which is essential for system administration, security analysis, and incident response.

### Process Monitoring

**Get-Process**
```powershell
Get-Process
```
- Provides detailed view of all currently running processes
- Shows CPU and memory usage information
- Essential for monitoring and troubleshooting

**Process Information**
- Process Name and ID (PID)
- CPU Usage and Memory Consumption
- Process Start Time
- Parent Process Information

**Advanced Process Queries**
```powershell
# Get processes using most memory
Get-Process | Sort-Object WorkingSet -Descending | Select-Object -First 10

# Get processes by specific name
Get-Process -Name "notepad"

# Get processes with high CPU usage
Get-Process | Where-Object -Property "CPU" -gt 100
```

### Service Monitoring

**Get-Service**
```powershell
Get-Service
```
- Retrieves information about service status on the machine
- Shows running, stopped, or paused services
- Used extensively by system administrators

**Service Status Types**
- Running - Active and operational
- Stopped - Inactive and not running
- Paused - Temporarily suspended

**Service Analysis**
```powershell
# Get all running services
Get-Service | Where-Object -Property "Status" -eq "Running"

# Get services by specific status
Get-Service | Where-Object -Property "Status" -eq "Stopped"

# Get services starting with specific name
Get-Service -Name "Win*"
```

### Network Connection Analysis

**Get-NetTCPConnection**
```powershell
Get-NetTCPConnection
```
- Displays current TCP connections
- Shows local and remote endpoints
- Essential for network monitoring

**Connection Information**
- Local and Remote IP Addresses
- Port Numbers
- Connection State
- Process ID (PID) of owning process

**Network Analysis Examples**
```powershell
# Get all established connections
Get-NetTCPConnection | Where-Object -Property "State" -eq "Established"

# Get connections on specific port
Get-NetTCPConnection | Where-Object -Property "LocalPort" -eq 80

# Get connections by remote address
Get-NetTCPConnection | Where-Object -Property "RemoteAddress" -like "192.168.*"
```

### File Integrity Verification

**Get-FileHash**
```powershell
Get-FileHash -Path ".\path"
```
- Generates file hashes for integrity verification
- Used in incident response and forensics
- Detects potential file tampering

**Hash Types**
- SHA1, SHA256, SHA384, SHA512
- MD5 (less secure, legacy)
- Default is SHA256

**File Integrity Examples**
```powershell
# Get SHA256 hash of file
Get-FileHash -Path "./hiddentreasure.txt"

# Get MD5 hash
Get-FileHash -Path "./file.txt" -Algorithm MD5

# Hash multiple files
Get-ChildItem -Filter "*.exe" | Get-FileHash
```

### Security Applications

**Blue Team Operations**
- Log analysis and monitoring
- Anomaly detection
- Extracting indicators of compromise (IOCs)
- System integrity verification
- Automated scanning for intrusion signs

**Incident Response**
- Process analysis and monitoring
- Network connection investigation
- Service status verification
- File integrity checking
- Malware analysis support

**Real-Time Monitoring**
```powershell
# Monitor processes continuously
while ($true) { Get-Process | Sort-Object CPU -Descending | Select-Object -First 5; Start-Sleep 5 }

# Monitor network connections
Get-NetTCPConnection | Where-Object -Property "State" -eq "Established" | Select-Object LocalAddress, LocalPort, RemoteAddress, RemotePort
```

## Best Practices
- Use appropriate cmdlets for specific monitoring needs
- Combine commands for comprehensive system analysis
- Monitor system resources during analysis
- Document findings for incident response
- Use filtering to focus on relevant data
- Verify file hashes against known good values