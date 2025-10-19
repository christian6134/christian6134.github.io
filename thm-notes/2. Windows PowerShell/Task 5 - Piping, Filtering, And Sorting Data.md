# Task 5 - Piping, Filtering, And Sorting Data

## Learning Objectives
- Master PowerShell piping techniques for data flow
- Learn filtering and sorting operations on objects
- Understand comparison operators and their usage
- Practice advanced data manipulation and analysis

## Overview
PowerShell's piping capabilities are one of its most powerful features. Unlike traditional command-line tools that pass text, PowerShell passes objects through pipelines, enabling sophisticated data manipulation and analysis. This object-oriented approach makes PowerShell exceptionally powerful for complex operations.

### Understanding Piping

**Piping Concept**
- Technique that allows output of one command to be used as input for another
- Enables sequence of operations
- Data flows from one command to the next
- Uses `|` (pipe) symbol

**PowerShell Piping Advantage**
- Passes **objects** rather than just text
- Objects retain properties and methods
- Enables advanced data manipulation
- Supports complex analysis operations

### Basic Piping Examples

**Sorting Files by Size**
```powershell
Get-ChildItem | Sort-Object Length
```
- Lists files sorted by size (ascending)
- `Sort-Object` operates on Length property

**Sorting in Descending Order**
```powershell
Get-ChildItem | Sort-Object Length -Descending
```
- Sorts files by size (largest first)
- `-Descending` parameter reverses sort order

### Filtering Operations

**Where-Object Filtering**
```powershell
Get-ChildItem | Where-Object -Property "Extension" -eq ".txt"
```
- Displays only files with .txt extension
- Filters based on object properties

**Pattern Matching**
```powershell
Get-ChildItem | Where-Object -Property "Name" -like "ship*"
```
- Shows files with names starting with "ship"
- Uses wildcard pattern matching

### Comparison Operators

**Common Comparison Operators**
- `-eq` - equal to
- `-ne` - not equal to
- `-gt` - greater than
- `-ge` - greater than or equal to
- `-lt` - less than
- `-le` - less than or equal to
- `-like` - pattern matching
- `-notlike` - not matching pattern

**Filtering Examples**
```powershell
# Files larger than 100 bytes
Get-ChildItem | Where-Object -Property "Length" -gt 100

# Files not equal to specific name
Get-ChildItem | Where-Object -Property "Name" -ne "readme.txt"
```

### Object Selection

**Select-Object**
```powershell
Select-Object -Property "Name", "Length"
```
- Selects specific properties from objects
- Limits output to needed details
- Reduces information overload

**Selecting First/Last Items**
```powershell
Get-ChildItem | Sort-Object Length -Descending | Select-Object -First 1
```
- Gets the largest file in directory
- Combines sorting and selection

### Text Searching

**Select-String**
```powershell
Select-String -Path ".\captain-hat.txt" -Pattern "hat"
```
- Searches for text patterns within files
- Similar to `grep` in Linux
- Supports regular expressions

**Searching Multiple Files**
```powershell
Get-ChildItem -Filter "*.txt" | Select-String -Pattern "searchterm"
```

### Advanced Pipeline Examples

**Complex Data Analysis**
```powershell
# Find largest file in specific directory
Get-ChildItem -Path "C:\Users\captain\Documents\captain-cabin" | 
    Sort-Object Length -Descending | 
    Select-Object -First 1
```

**Multi-Step Filtering**
```powershell
# Get all .txt files larger than 100 bytes
Get-ChildItem | 
    Where-Object -Property "Extension" -eq ".txt" | 
    Where-Object -Property "Length" -gt 100 |
    Sort-Object Length -Descending
```

### Practical Applications

**System Administration**
- Process monitoring and filtering
- Log file analysis
- System resource analysis
- Configuration file processing

**Security Analysis**
- Log parsing and analysis
- File system auditing
- Process monitoring
- Network connection analysis

## Best Practices
- Start with simple pipelines and build complexity
- Use appropriate comparison operators
- Test pipelines with small datasets first
- Document complex pipeline operations
- Leverage object properties for precise filtering
- Use Select-Object to focus on relevant data