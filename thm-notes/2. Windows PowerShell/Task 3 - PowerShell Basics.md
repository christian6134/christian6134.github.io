# Task 3 - PowerShell Basics

## Learning Objectives
- Learn different methods to launch PowerShell
- Understand PowerShell cmdlet naming conventions
- Master essential PowerShell commands and help system
- Practice using aliases and module management

## Overview
PowerShell basics cover the fundamental concepts needed to effectively use PowerShell. Understanding cmdlet structure, help systems, and basic navigation commands is essential for building proficiency in PowerShell scripting and automation.

### Launching PowerShell

**Multiple Launch Methods**
- **Start Menu**: Type `powershell` in search
- **Search**: Search for "Windows PowerShell"
- **Run Dialog**: `Win + R` → Run → `powershell`
- **File Explorer**: Navigate to folder → type `powershell` in address bar
- **Task Manager**: File → Run New Task → `powershell`

### PowerShell Cmdlets

**Cmdlet Naming Convention**
PowerShell cmdlets follow the `Verb-Noun` pattern:
- **Verb**: Describes the action to be performed
- **Noun**: Specifies what the action applies to

**Common Examples**
```powershell
Get-Content    # Gets the content of a file
Set-Location   # Changes the current working directory
New-Item       # Creates new files or directories
Remove-Item    # Deletes files or directories
```

### Essential Commands

**Get-Command**
```powershell
Get-Command
```
- Lists all available cmdlets
- Shows installed PowerShell commands

```powershell
Get-Command -CommandType Function
```
- Filters commands by type (Function, Cmdlet, Alias)
- Useful for finding specific command types

**Get-Help**
```powershell
Get-Help cmdlet-name
```
- Provides detailed information about cmdlets
- Shows usage, parameters, and examples
- Essential for learning new commands

```powershell
Get-Help New-LocalUser -examples
```
- Shows example usage for specific cmdlets
- Practical demonstrations of command usage

**Get-Alias**
```powershell
Get-Alias
```
- Lists all available aliases
- Shows shortcuts for common commands

**Common Aliases**
- `dir` → `Get-ChildItem`
- `cd` → `Set-Location`
- `type` → `Get-Content`
- `echo` → `Write-Output`

### Module Management

**Find-Module**
```powershell
Find-Module -Name "ModuleName"
```
- Searches for modules in online repositories
- Discovers available PowerShell modules

**Install-Module**
```powershell
Install-Module ModuleName
```
- Installs PowerShell modules
- Expands PowerShell functionality

### Practical Examples

**Finding Commands**
```powershell
Get-Command -Name Remove*
```
- Retrieves all commands starting with "Remove"
- Useful for discovering related commands

**Getting Help**
```powershell
Get-Help New-LocalUser -examples
```
- Shows example usage for New-LocalUser cmdlet
- Demonstrates practical command usage

## Best Practices
- Use Get-Help to understand new commands
- Leverage aliases for common operations
- Explore modules to extend functionality
- Practice with safe commands before production use
- Document frequently used command patterns