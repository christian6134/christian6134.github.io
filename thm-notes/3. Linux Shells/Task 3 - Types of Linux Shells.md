# Task 3 - Types of Linux Shells

## Learning Objectives
- Identify different types of Linux shells available
- Learn how to check current shell and available shells
- Understand shell switching and permanent changes
- Master BASH shell features and capabilities

## Overview
Linux systems support multiple shell types, each with unique features and capabilities. Understanding different shell types, how to identify them, and how to switch between them is essential for system administration and customization.

### Shell Identification

**Check Current Shell**
```bash
echo $SHELL
```
- Displays current shell path (e.g., `/bin/bash`)
- Shows which shell is currently active
- Essential for shell identification

**List Available Shells**
```bash
cat /etc/shells
```
- Shows all shells installed on the system
- Displays available shell options
- Lists shell paths and locations

### Shell Switching

**Temporary Shell Switch**
```bash
shell_name
```
- Type shell name to open it temporarily
- Creates new shell session
- Returns to previous shell when exiting

**Permanent Shell Change**
```bash
chsh -s /path/to/shell
```
- Changes default shell permanently
- Requires shell restart to take effect
- Updates user's default shell setting

### BASH Shell Features

**BASH (Bourne Again Shell)**
- Most common default shell in Linux distributions
- Enhanced version of original Bourne shell
- Provides advanced features and capabilities

**BASH Key Features**

**Tab Completion**
- Press Tab to auto-complete commands and filenames
- Saves time and reduces typing errors
- Essential for efficient command line usage

**Command History**
```bash
history
```
- Displays all previous commands
- Shows command history with line numbers
- Enables reuse of previous commands

**History Navigation**
- Use arrow keys to navigate command history
- `Ctrl+R` for reverse search through history
- `!!` to repeat last command

### Common Shell Types

**BASH (Bourne Again Shell)**
- Default shell for most Linux distributions
- Full-featured with scripting capabilities
- Compatible with POSIX standards

**SH (Bourne Shell)**
- Original Unix shell
- Basic shell functionality
- Minimal features compared to BASH

**ZSH (Z Shell)**
- Advanced shell with additional features
- Enhanced completion and customization
- Popular alternative to BASH

**FISH (Friendly Interactive Shell)**
- User-friendly shell with auto-suggestions
- Syntax highlighting and web-based configuration
- Modern shell with enhanced user experience

### Shell Customization

**Environment Variables**
- Shell-specific configuration settings
- Customizable prompt and behavior
- Environment-specific variables

**Configuration Files**
- `.bashrc` - BASH configuration file
- `.profile` - User profile settings
- `.bash_profile` - BASH login settings

### Practical Examples

**Shell Management**
```bash
# Check current shell
echo $SHELL

# List available shells
cat /etc/shells

# Switch to ZSH temporarily
zsh

# Change default shell to ZSH
chsh -s /bin/zsh

# View command history
history

# Search command history
history | grep "command_name"
```

**BASH Features**
```bash
# Use tab completion
ls /usr/bin/[TAB]

# Navigate command history
# Use up/down arrows

# Repeat last command
!!

# Execute command from history
!123  # Execute command number 123
```

## Best Practices
- Use appropriate shell for specific tasks
- Learn shell-specific features and capabilities
- Customize shell environment for efficiency
- Use command history effectively
- Practice tab completion for speed
- Document shell configurations and customizations