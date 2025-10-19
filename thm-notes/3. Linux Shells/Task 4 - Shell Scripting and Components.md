# Task 4 - Shell Scripting and Components

## Learning Objectives
- Understand shell scripting fundamentals and automation concepts
- Learn script creation, structure, and execution techniques
- Master variables, loops, and conditional statements
- Practice script permissions and execution methods

## Overview
Shell scripting involves creating executable text files containing a series of commands. Scripts automate repetitive tasks, enable complex operations, and provide powerful automation capabilities. Understanding script structure, components, and execution is essential for system administration and cybersecurity operations.

### Shell Scripting Fundamentals

**Script Definition**
- Set of commands combined into a single executable file
- Automates repetitive tasks requiring multiple commands
- Enables complex operations through simple execution
- Supports various programming languages and constructs

**Scripting Benefits**
- **Automation**: Reduces manual intervention
- **Efficiency**: Speeds up repetitive tasks
- **Consistency**: Ensures uniform execution
- **Complexity**: Enables sophisticated operations

### Script Creation Process

**Step-by-Step Creation**
1. Open terminal
2. Select appropriate shell
3. Create file using text editor
4. Use `.sh` extension for bash scripts
5. Add proper permissions for execution

**Text Editor Usage**
```bash
nano first_script.sh
```
- Creates new script file
- Opens text editor for script creation
- `.sh` extension indicates shell script

### Script Structure

**Shebang**
```bash
#!/bin/bash
```
- **Shebang**: `#!` followed by interpreter path
- Must be first line of script
- Specifies which shell to use for execution
- Essential for proper script execution

**Script Components**
1. **Shebang** - Interpreter specification
2. **Variables** - Data storage and manipulation
3. **Commands** - Actual operations to perform
4. **Control Structures** - Loops and conditionals

### Variables

**Variable Usage**
- Store values for use throughout script
- Can store URLs, file paths, user input, etc.
- Enable dynamic and flexible scripting
- Support various data types

**Variable Examples**
```bash
#!/bin/bash
NAME="John"
AGE=25
PATH="/home/user/documents"
```

### Script Execution

**Permission Setting**
```bash
chmod +x first_script.sh
```
- Gives execute permissions to script
- Required before script can be executed
- `+x` adds execute permission

**Script Execution**
```bash
./first_script.sh
```
- Executes script in current directory
- `./` tells shell to execute file in current directory
- Script runs with specified permissions

### Control Structures

**Loops**
```bash
for i in {1..5}
do
    echo $i
done
```
- **For Loop**: Repeats commands for specified range
- `do` and `done` enclose loop commands
- Enables repetitive operations

**Conditional Statements**
```bash
if [ "$user" = "Stewart" ]
then
    echo "Access granted"
else
    echo "Access denied"
fi
```
- **If Statement**: Executes commands based on conditions
- `if` starts condition, `fi` ends it
- Enables decision-making in scripts

### Advanced Script Features

**User Input**
```bash
read -p "Enter your name: " user
```
- Prompts user for input
- Stores input in variable
- Enables interactive scripts

**Error Handling**
```bash
if [ $? -eq 0 ]
then
    echo "Command succeeded"
else
    echo "Command failed"
fi
```
- Checks command exit status
- Handles errors appropriately
- Improves script reliability

### Practical Examples

**Basic Script Template**
```bash
#!/bin/bash
# Script: example.sh
# Purpose: Basic script example

# Variables
NAME="User"
PATH="/home/user"

# Commands
echo "Hello, $NAME"
echo "Current path: $PATH"

# Loop example
for i in {1..3}
do
    echo "Iteration: $i"
done
```

**Interactive Script**
```bash
#!/bin/bash
# Interactive script example

read -p "Enter your name: " name
if [ "$name" = "Admin" ]
then
    echo "Welcome, Administrator!"
else
    echo "Hello, $name"
fi
```

## Best Practices
- Always include shebang at script beginning
- Use descriptive variable names
- Add comments explaining script purpose
- Test scripts in safe environments
- Use proper error handling
- Set appropriate file permissions
- Document script functionality