# Task 2 - Basic System Information

## Learning Objectives
- Learn essential Windows CLI commands for system information gathering
- Understand how to display OS version and system details
- Master command output pagination techniques
- Identify system configuration through command line

## Overview
System information gathering is a fundamental skill for cybersecurity professionals. Understanding how to quickly retrieve system details through command line interfaces is essential for system administration, troubleshooting, and security assessments.

### Essential System Information Commands

**SET Command**
```cmd
set
```
- Displays all environment variables
- Search for `Path=` to view Windows PATH configuration
- Shows system and user-specific environment settings
- Useful for understanding system configuration

**VER Command**
```cmd
ver
```
- Displays the Windows operating system version
- Shows build number and version information
- Quick way to identify OS version without GUI
- Essential for compatibility and security assessments

**SYSTEMINFO Command**
```cmd
systeminfo
```
- Comprehensive system information display
- Shows OS details, processor information, and memory statistics
- Displays network configuration and installed software
- Critical for system documentation and analysis

### Command Output Management

**Pagination with MORE**
```cmd
systeminfo | more
```
- Controls output display when information is extensive
- Use `space` to advance to next page
- Prevents information overflow in terminal
- Essential for reading long command outputs

### Information Categories

**Operating System Details**
- Version and build information
- Installation date and system uptime
- Service pack and update information

**Hardware Information**
- Processor details and architecture
- Physical and virtual memory statistics
- System model and manufacturer information

**Network Configuration**
- Network adapter details
- IP configuration and routing tables
- Domain and workgroup membership

## Practical Applications
- System documentation and inventory
- Troubleshooting system issues
- Security assessment and compliance checking
- Remote system administration

## Best Practices
- Use pagination for long outputs
- Document system information for reference
- Combine commands for comprehensive system profiles
- Verify information accuracy for critical decisions