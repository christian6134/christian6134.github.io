# Task 5 - Task and Process Management

## Learning Objectives
- Master Windows CLI process monitoring and management commands
- Learn how to list, filter, and terminate running processes
- Understand Process ID (PID) identification and usage
- Practice process filtering and termination techniques

## Overview
Process management is a critical skill for system administrators and cybersecurity professionals. Understanding how to monitor running processes, identify suspicious activities, and manage system resources through command line tools is essential for maintaining system security and performance.

### Process Listing

**TASKLIST Command**
```cmd
tasklist
```
- Lists all running processes on the system
- Shows process names, PIDs, and memory usage
- Displays session information and status
- Essential for system monitoring

### Process Filtering

**TASKLIST with Filter**
```cmd
tasklist /FI "imagename eq sshd.exe"
```
- Filters processes by specific criteria
- `/FI` specifies filter image (process name)
- Useful for finding specific running processes
- Essential for security monitoring

**Common Filter Examples**
```cmd
tasklist /FI "status eq running"
tasklist /FI "memusage gt 100000"
tasklist /FI "username eq administrator"
```

### Process Termination

**TASKKILL Command**
```cmd
taskkill /PID target_pid
taskkill /PID 4567
```
- Terminates processes by Process ID
- `/PID` specifies the process to kill
- Use with caution - can cause data loss
- Essential for stopping unresponsive processes

**TASKKILL by Process Name**
```cmd
taskkill /IM process_name.exe
taskkill /IM notepad.exe
```
- Terminates processes by image name
- `/IM` specifies image (process) name
- Can terminate multiple instances

### Process Management Options

**Force Termination**
```cmd
taskkill /PID 4567 /F
```
- `/F` forces process termination
- Use when normal termination fails
- Can cause immediate data loss

**Tree Termination**
```cmd
taskkill /PID 1234 /T
```
- `/T` terminates process tree
- Kills child processes as well
- Use carefully to avoid system instability

## Process Information Categories

**System Processes**
- Critical system services
- Operating system components
- Hardware drivers

**User Processes**
- Applications and programs
- User-initiated tasks
- Background services

**Network Processes**
- Network services and daemons
- SSH servers and clients
- Web servers and applications

## Security Applications
- Monitoring for suspicious processes
- Identifying unauthorized software
- Terminating malicious processes
- System resource management

## Best Practices
- Always verify process identity before termination
- Use filtering to locate specific processes
- Document process management procedures
- Monitor system stability after process termination
- Use force termination only when necessary