# Task 5 - The Locker Script

## Learning Objectives
- Apply shell scripting concepts to create a security authentication script
- Learn user input validation and conditional logic
- Practice script creation for access control systems
- Understand real-world application of shell scripting in security

## Overview
The Locker Script demonstrates practical application of shell scripting for security purposes. This script implements a simple authentication system that verifies user credentials before granting access to a secured resource. It showcases how scripting can be used for access control and security validation.

### Script Requirements

**Security Scenario**
A user has a locker in a bank that requires script-based verification before opening. The script must:
- Prompt user for authentication details
- Validate provided credentials
- Grant or deny access based on verification
- Implement basic security controls

**Required Credentials**
- **Username**: John
- **Company name**: Tryhackme
- **PIN**: 7385

### Script Implementation

**Authentication Logic**
```bash
#!/bin/bash
# Locker Access Control Script

echo "Welcome to the Bank Locker System"
echo "Please provide your credentials:"

# Get user input
read -p "Enter your username: " username
read -p "Enter your company name: " company
read -p "Enter your PIN: " pin

# Validate credentials
if [ "$username" = "John" ] && [ "$company" = "Tryhackme" ] && [ "$pin" = "7385" ]
then
    echo "Access granted! Welcome to your locker."
    echo "Locker opened successfully."
else
    echo "Access denied! Invalid credentials."
    echo "Please contact bank administration."
fi
```

### Script Components

**User Input Collection**
```bash
read -p "Enter your username: " username
read -p "Enter your company name: " company
read -p "Enter your PIN: " pin
```
- Prompts user for required information
- Stores input in variables
- Creates interactive authentication process

**Credential Validation**
```bash
if [ "$username" = "John" ] && [ "$company" = "Tryhackme" ] && [ "$pin" = "7385" ]
```
- Compares user input with stored credentials
- Uses logical AND (`&&`) for multiple conditions
- Implements strict validation requirements

**Access Control Logic**
```bash
then
    echo "Access granted! Welcome to your locker."
    echo "Locker opened successfully."
else
    echo "Access denied! Invalid credentials."
    echo "Please contact bank administration."
fi
```
- Provides appropriate feedback based on validation
- Implements access control decisions
- Offers clear user communication

### Security Features

**Multi-Factor Authentication**
- Requires three pieces of information
- Username, company, and PIN validation
- Increases security through multiple verification steps

**Input Validation**
- Checks all provided credentials
- Implements strict matching requirements
- Prevents unauthorized access attempts

**User Feedback**
- Clear success and failure messages
- Appropriate guidance for denied access
- Professional communication style

### Script Execution

**Setup Process**
```bash
# Create script file
nano locker_script.sh

# Add execute permissions
chmod +x locker_script.sh

# Execute script
./locker_script.sh
```

**Execution Flow**
1. Script prompts for username
2. User enters "John"
3. Script prompts for company name
4. User enters "Tryhackme"
5. Script prompts for PIN
6. User enters "7385"
7. Script validates all credentials
8. Access granted or denied based on validation

### Enhanced Security Features

**Additional Security Measures**
```bash
# Add attempt counter
attempts=0
max_attempts=3

while [ $attempts -lt $max_attempts ]
do
    # Authentication logic
    if [ "$username" = "John" ] && [ "$company" = "Tryhackme" ] && [ "$pin" = "7385" ]
    then
        echo "Access granted!"
        break
    else
        echo "Invalid credentials. Attempt $((attempts+1)) of $max_attempts"
        attempts=$((attempts+1))
    fi
done
```

**Security Considerations**
- Limit login attempts
- Log access attempts
- Implement timeout mechanisms
- Use secure credential storage
- Add audit trail functionality

## Practical Applications
- System access control
- Application authentication
- Service account management
- Security automation scripts
- Access logging and monitoring

## Best Practices
- Validate all user input
- Implement appropriate error handling
- Use secure credential storage methods
- Add logging and audit capabilities
- Test scripts thoroughly before deployment
- Document security requirements and procedures