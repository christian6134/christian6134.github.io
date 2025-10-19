# Task 4 - Navigating the File System and Working With Files

## Learning Objectives
- Master PowerShell file system navigation commands
- Learn file and directory creation, removal, and copying techniques
- Understand file content viewing and manipulation
- Practice working with file paths and locations

## Overview
PowerShell provides powerful file system management capabilities through object-oriented cmdlets. Understanding how to navigate directories, create and manage files, and manipulate file content is essential for system administration and automation tasks.

### File System Navigation

**Get-ChildItem**
```powershell
Get-ChildItem
dir  # Alias for Get-ChildItem
ls   # Another alias
```
- Lists files and directories in specified location
- Uses `-Path` parameter to specify directory
- Shows file properties and attributes

**Set-Location**
```powershell
Set-Location -Path "./Documents"
cd  # Alias for Set-Location
```
- Navigates to different working directory
- Changes current working directory
- Supports relative and absolute paths

### File and Directory Management

**Creating New Items**
```powershell
New-Item -Path ".\captain-cabin\captain-wardrobe" -ItemType "Directory"
```
- Creates new files or directories
- Must specify path and item type
- `-ItemType` can be "File" or "Directory"

**Removing Items**
```powershell
Remove-Item -Path "./path"
```
- Deletes files or directories
- Use with caution - deleted items may be unrecoverable
- Supports recursive deletion with `-Recurse`

**Copying Items**
```powershell
Copy-Item -Path "source" -Destination "destination"
```
- Copies files or directories
- Preserves original files
- Supports wildcard patterns

### File Content Operations

**Get-Content**
```powershell
Get-Content -Path ".\captain-hat.txt"
type  # Alias for Get-Content
```
- Displays file contents in console
- Reads text files line by line
- Supports encoding parameters

**Advanced Content Operations**
```powershell
Get-Content -Path "file.txt" -TotalCount 10  # First 10 lines
Get-Content -Path "file.txt" -Tail 5          # Last 5 lines
```

### Practical Examples

**Directory Listing**
```powershell
Get-ChildItem -Path C:\Users
```
- Displays contents of C:\Users directory
- Shows all user directories

**File Operations**
```powershell
# Create directory structure
New-Item -Path ".\project\src" -ItemType "Directory"

# Copy files
Copy-Item -Path ".\source.txt" -Destination ".\backup.txt"

# View file content
Get-Content -Path ".\config.txt"
```

### Path Management

**Working with Paths**
- Use `.\` for current directory
- Use `..\` for parent directory
- Use absolute paths for specific locations
- PowerShell handles path separators automatically

**Path Examples**
```powershell
Set-Location -Path "C:\Users\Username\Documents"
Set-Location -Path ".\Desktop"
Set-Location -Path "..\Downloads"
```

## File System Best Practices
- Always verify paths before operations
- Use appropriate item types for creation
- Test commands in safe environments
- Document file management procedures
- Use descriptive names for files and directories

## Security Considerations
- Be cautious with Remove-Item operations
- Verify file sources before copying
- Use appropriate permissions for file operations
- Monitor file system changes in production environments