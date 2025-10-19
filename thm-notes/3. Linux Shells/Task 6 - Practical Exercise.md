# Task 6 - Practical Exercise

## Learning Objectives
- Apply shell scripting skills to solve real-world problems
- Practice directory navigation and file searching techniques
- Learn log file analysis and pattern searching
- Master script debugging and troubleshooting methods

## Overview
This practical exercise demonstrates the application of shell scripting skills to solve a real-world problem. The exercise involves creating a script to search through log files in a specific directory to find a hidden flag, showcasing practical cybersecurity and system administration skills.

### Exercise Scenario

**Problem Statement**
Create a script that searches through log files in a specific directory to find a hidden flag. The script must:
- Navigate to the correct directory
- Search through log files for the flag
- Use appropriate search patterns
- Handle directory and file operations efficiently

### Script Implementation

**Basic Search Script**
```bash
#!/bin/bash
# Log File Search Script

# Set target directory
directory="/var/log"

# Set search pattern
flag="desired_flag"

# Navigate to directory
cd $directory

# Search for flag in log files
for file in *.log
do
    if [ -f "$file" ]
    then
        echo "Searching in $file..."
        if grep -q "$flag" "$file"
        then
            echo "Flag found in $file!"
            cat "$file"
            break
        fi
    fi
done
```

### Script Components

**Directory Navigation**
```bash
directory="/var/log"
cd $directory
```
- Sets target directory variable
- Uses variable for flexible directory specification
- Navigates to log directory for searching

**File Iteration**
```bash
for file in *.log
do
    if [ -f "$file" ]
    then
        # Process file
    fi
done
```
- Iterates through all .log files
- Checks if file exists before processing
- Handles file operations safely

**Pattern Searching**
```bash
if grep -q "$flag" "$file"
then
    echo "Flag found in $file!"
    cat "$file"
    break
fi
```
- Uses grep to search for pattern
- `-q` flag for quiet operation
- Displays file contents when flag found
- Breaks loop when flag is located

### Exercise Solution

**Target Directory**
```bash
cd /var/log
```
- Navigate to system log directory
- Contains various system log files
- Standard location for log files

**Flag Discovery**
```bash
cat authentication.log
```
- Search in authentication log file
- Flag found: "the cat is sleeping under the table"
- Demonstrates log file analysis skills

### Advanced Script Features

**Enhanced Search Script**
```bash
#!/bin/bash
# Enhanced Log Search Script

# Configuration
LOG_DIR="/var/log"
SEARCH_PATTERNS=("flag" "secret" "password" "key")
LOG_EXTENSIONS=("*.log" "*.txt" "*.out")

# Function to search in file
search_file() {
    local file="$1"
    local pattern="$2"
    
    if grep -i "$pattern" "$file" > /dev/null 2>&1
    then
        echo "Match found in $file:"
        grep -i "$pattern" "$file"
        return 0
    fi
    return 1
}

# Main search logic
cd "$LOG_DIR"

for ext in "${LOG_EXTENSIONS[@]}"
do
    for file in $ext
    do
        if [ -f "$file" ]
        then
            echo "Searching $file..."
            for pattern in "${SEARCH_PATTERNS[@]}"
            do
                if search_file "$file" "$pattern"
                then
                    echo "Pattern '$pattern' found in $file"
                fi
            done
        fi
    done
done
```

### Script Debugging

**Common Issues and Fixes**
- **Directory Path**: Ensure correct directory path
- **File Permissions**: Check read permissions for log files
- **Pattern Matching**: Verify search pattern accuracy
- **File Existence**: Check if files exist before processing

**Debugging Techniques**
```bash
# Add debug output
echo "Current directory: $(pwd)"
echo "Files in directory: $(ls -la)"
echo "Searching for pattern: $flag"

# Test individual components
ls -la /var/log
grep -n "pattern" /var/log/authentication.log
```

### Practical Applications

**Security Analysis**
- Log file analysis for security incidents
- Pattern searching for indicators of compromise
- Automated log monitoring and alerting
- Forensic analysis of system logs

**System Administration**
- Automated log file processing
- System monitoring and alerting
- Log file cleanup and management
- Performance analysis and reporting

## Best Practices
- Use descriptive variable names
- Implement proper error handling
- Test scripts with sample data
- Document script functionality
- Use appropriate file permissions
- Validate input parameters
- Implement logging and debugging features