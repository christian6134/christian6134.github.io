# Task 1 and 2 - Introduction and What is PowerShell?

## Learning Objectives
- Understand what PowerShell is and its core capabilities
- Learn the basic structure of PowerShell's scripting language
- Practice running basic PowerShell commands
- Recognize PowerShell's applications in cybersecurity industry

## Overview
PowerShell is Microsoft's advanced task automation and configuration management framework. It combines a powerful command-line shell with a comprehensive scripting language built on the .NET framework, making it an essential tool for system administrators and cybersecurity professionals.

### What is PowerShell?

**Core Definition**
PowerShell is a task automation and configuration management program consisting of:
- Command-line shell interface
- Associated scripting language
- Built on .NET framework foundation

**Key Characteristics**
- Designed for task automation and configuration management
- Combines CLI functionality with scripting capabilities
- Object-oriented programming approach
- Handles complex data types and system component interactions

### The Power of PowerShell

**Object-Oriented Approach**
PowerShell treats everything as objects, which provides significant advantages over traditional text-based command-line tools.

**Understanding Objects**
- **Objects** represent items with properties and methods
- **Properties** are characteristics or attributes
- **Methods** are actions or functions that can be performed

**Real-World Example**
A car object might have:
- **Properties**: Color, Model, Year, Mileage
- **Methods**: Drive(), Honk(), Refuel(), Start()

### PowerShell Cmdlets

**Cmdlet Definition**
- **Cmdlet** = Command-let
- Native PowerShell commands
- Run within PowerShell environment
- Return objects that retain their properties and methods

**Cmdlet Structure**
- Verb-Noun naming convention
- Examples: Get-Process, Set-Location, New-Item
- Consistent and predictable command structure

### Advantages Over Traditional CLI

**Object Retention**
- Commands return structured objects
- Properties and methods remain accessible
- Enables complex data manipulation
- Supports pipeline operations

**Rich Data Types**
- Handles complex data structures
- Supports arrays, hashtables, and custom objects
- Type-aware operations and validation

**System Integration**
- Direct access to .NET framework
- Integration with Windows Management Instrumentation (WMI)
- COM object support for legacy applications

### Cybersecurity Applications

**System Administration**
- Automated system configuration
- Bulk user and group management
- Service and process monitoring
- Registry and file system operations

**Security Analysis**
- Log analysis and parsing
- Network configuration auditing
- Malware detection and analysis
- Incident response automation

**Compliance and Reporting**
- Automated compliance checking
- Security policy enforcement
- Audit trail generation
- Custom reporting solutions

## Getting Started
- PowerShell is pre-installed on modern Windows systems
- Available as PowerShell Core for cross-platform use
- Integrated with Windows Terminal for enhanced experience
- Extensive help system with Get-Help command

## Best Practices
- Use consistent naming conventions
- Leverage object properties for data manipulation
- Practice with safe commands before production use
- Utilize PowerShell's extensive help system
- Document scripts for future reference