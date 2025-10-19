# Task 2 - Interacting with a Shell

## Learning Objectives
- Master basic shell interaction and navigation commands
- Learn essential Linux commands for file and directory operations
- Understand text searching and manipulation techniques
- Practice working with shell environments and SSH connections

## Overview
Effective shell interaction requires understanding basic commands for navigation, file operations, and text manipulation. These fundamental skills form the foundation for advanced shell usage, scripting, and system administration tasks.

### Shell Connection

**SSH Connection**
```bash
ssh user@10.10.214.225
```
- Establishes secure shell connection to remote system
- Format: `ssh username@ip_address`
- Provides command-line access to remote machines
- Essential for remote system administration

### BASH Shell

**BASH (Bourne Again Shell)**
- Most Linux distributions use BASH as default shell
- Enhanced version of the original Bourne shell
- Provides advanced features and capabilities
- Standard shell for most Linux systems

### Essential Navigation Commands

**PWD Command**
```bash
pwd
```
- **Print Working Directory**
- Shows current directory location
- Essential for orientation in file system
- Default location is typically home directory

**CD Command**
```bash
cd
```
- **Change Directory**
- Navigates to specified directory
- Changes current working directory
- Essential for file system navigation

**LS Command**
```bash
ls
```
- **List Directory Contents**
- Shows files and directories in current location
- Displays file information and permissions
- Basic file system exploration

### File Content Operations

**CAT Command**
```bash
cat filename
```
- **Concatenate and Display**
- Shows file contents on screen
- Displays entire file content
- Useful for viewing text files

### Text Searching

**GREP Command**
```bash
grep POOP dictionary.txt
```
- **Global Regular Expression Print**
- Searches for patterns in files
- Allows search for words or patterns
- Powerful text searching tool

**GREP Examples**
```bash
grep "pattern" filename          # Search for pattern in file
grep -i "pattern" filename      # Case-insensitive search
grep -r "pattern" directory     # Recursive search in directory
grep -n "pattern" filename      # Show line numbers
```

### Working Directory Concepts

**Directory Operations**
- Must be in correct directory to perform operations
- Default location is home directory (`~`)
- Use `pwd` to verify current location
- Use `cd` to navigate to desired directory

**Common Directory Operations**
```bash
cd /home/user          # Navigate to specific directory
cd ..                  # Move up one directory level
cd ~                   # Return to home directory
cd -                   # Return to previous directory
```

### Practical Examples

**Basic File Operations**
```bash
# Check current location
pwd

# List directory contents
ls

# Navigate to specific directory
cd /var/log

# View file contents
cat filename.txt

# Search for text in file
grep "search_term" filename.txt
```

**File System Navigation**
```bash
# Navigate to home directory
cd ~

# List all files (including hidden)
ls -la

# Navigate to parent directory
cd ..

# Return to previous directory
cd -
```

## Best Practices
- Always verify current directory with `pwd`
- Use `ls` to explore directory contents
- Practice safe navigation commands
- Learn grep patterns for efficient searching
- Use appropriate commands for specific tasks
- Document frequently used command combinations