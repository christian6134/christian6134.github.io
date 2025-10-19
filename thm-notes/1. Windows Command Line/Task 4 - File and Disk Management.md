# Task 4 - File and Disk Management

## Learning Objectives
- Master Windows CLI file and directory navigation commands
- Learn file and folder creation, deletion, and management techniques
- Understand file content viewing and manipulation commands
- Practice disk and directory structure navigation

## Overview
File and disk management through command line interfaces is essential for system administration and cybersecurity tasks. Understanding how to navigate directories, manage files, and perform disk operations efficiently is crucial for maintaining organized systems and conducting security assessments.

### Directory Navigation

**CD Command (Change Directory)**
```cmd
cd
```
- Changes to specified directory
- `cd ..` moves up one directory level
- `cd target_directory` navigates to specific folder
- Essential for directory traversal

**DIR Command (Directory Listing)**
```cmd
dir
```
- Lists files and directories in current location
- Shows file sizes, dates, and attributes

```cmd
dir /a
```
- Displays hidden and system files
- Shows all file attributes including hidden files

```cmd
dir /s
```
- Displays files in current directory and subdirectories
- Recursive directory listing

### Directory Structure Visualization

**TREE Command**
```cmd
tree
```
- Displays directory structure in tree format
- Visual representation of folder hierarchy
- Useful for understanding directory organization

### File and Directory Management

**MKDIR Command**
```cmd
mkdir test
```
- Creates new directory
- Essential for organizing files and folders

**RMDIR Command**
```cmd
rmdir test
```
- Removes empty directory
- Cannot delete directories with contents

### File Content Operations

**TYPE Command**
```cmd
type filename
```
- Displays file contents on screen
- Shows text file content directly in terminal
- Useful for quick file content review

**MORE Command**
```cmd
more filename
```
- Displays file content with pagination
- Use `space` to advance through pages
- Essential for viewing large files

### File Operations

**COPY Command**
```cmd
copy target new
```
- Copies files from source to destination
- Creates duplicate files with new names
- Preserves original file

**DEL/ERASE Command**
```cmd
del filename
erase filename
```
- Deletes specified files
- Both commands perform identical operations
- Use with caution - deleted files may be unrecoverable

## Practical Applications
- System file organization and cleanup
- Backup and file management operations
- Security assessment file analysis
- Directory structure documentation

## Best Practices
- Always verify file paths before deletion
- Use appropriate commands for file operations
- Practice in safe environments before production use
- Document frequently used file management procedures