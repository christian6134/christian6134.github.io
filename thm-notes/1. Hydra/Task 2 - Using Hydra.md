# Task 2 - Using Hydra

## Learning Objectives
- Master Hydra command syntax and options
- Learn how to brute force SSH services
- Understand web form brute forcing techniques
- Practice with practical Hydra exercises
- Learn to interpret Hydra output and results

## Overview
This task provides hands-on experience with Hydra's command-line interface and practical examples of brute forcing different services. Understanding Hydra's syntax and options is essential for effective password attacks during penetration testing and security assessments.

### Hydra Command Syntax

**Basic Syntax Structure**
```bash
hydra [options] target service
```

**Common Options**
- `-l username`: Specify single username
- `-L userlist`: Use username list file
- `-p password`: Specify single password
- `-P passlist`: Use password list file
- `-t threads`: Set number of parallel threads
- `-V`: Verbose output for every attempt

### SSH Brute Forcing

**SSH Attack Command**
```bash
hydra -l <username> -P <full path to pass> 10.10.36.161 -t 4 ssh
```

**SSH Command Breakdown**
- `-l`: Specifies the SSH username for login
- `-P`: Indicates a list of passwords to try
- `-t`: Sets the number of threads to spawn
- `ssh`: Specifies the service to attack

**SSH Example**
```bash
hydra -l root -P passwords.txt 10.10.36.161 -t 4 ssh
```
- Uses `root` as the username for SSH
- Tries passwords from `passwords.txt` file
- Runs four threads in parallel
- Attacks SSH service on target IP

### Web Form Brute Forcing

**POST Web Form Command**
```bash
sudo hydra <username> <wordlist> 10.10.36.161 http-post-form "<path>:<login_credentials>:<invalid_response>"
```

**Web Form Parameters**
- `-l`: Username for web form login
- `-P`: Password list to use
- `http-post-form`: Specifies POST method form
- `<path>`: Login page URL (e.g., `login.php`)
- `<login_credentials>`: Form fields (e.g., `username=^USER^&password=^PASS^`)
- `<invalid_response>`: Response text indicating failed login
- `-V`: Verbose output for every attempt

**Web Form Example**
```bash
hydra -l <username> -P <wordlist> 10.10.36.161 http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V
```

**Web Form Breakdown**
- Login page is `/` (main IP address)
- `username` is the form field for username entry
- `^USER^` will be replaced with specified usernames
- `password` is the form field for password entry
- `^PASS^` will be replaced with provided passwords
- `F=incorrect` appears in server reply when login fails

### Practical Exercises

**Exercise 1: Web Password Brute Force**
```bash
hydra -l molly -P /usr/share/wordlist/rockyou.txt 10.10.36.161 http-post-form "/login:username=^USR^&password=^PASS^:F=incorrect" -v
```
- **Target**: Molly's web password
- **Method**: HTTP POST form brute force
- **Wordlist**: RockYou.txt
- **Flag**: `THM{2673a7dd116de68e85c48ec0b1f2612e}`

**Exercise 2: SSH Password Brute Force**
```bash
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.36.161 -t 4 ssh
```
- **Target**: Molly's SSH password
- **Method**: SSH brute force
- **Threads**: 4 parallel connections
- **Flag**: `THM{c8eeb0468febbadea859baeb33b2541b}`

### Command Options Reference

**Threading Options**
- `-t 4`: Use 4 parallel threads
- `-t 16`: Use 16 parallel threads (higher performance)
- Balance between speed and system impact

**Output Options**
- `-V`: Verbose output showing every attempt
- `-v`: Less verbose output
- `-q`: Quiet mode (minimal output)

**Service-Specific Options**
- `ssh`: SSH service brute forcing
- `ftp`: FTP service brute forcing
- `http-post-form`: Web form POST attacks
- `http-get-form`: Web form GET attacks

### Best Practices

**Performance Optimization**
- Use appropriate thread counts to avoid overwhelming target
- Monitor target system for signs of stress
- Implement delays between attempts if needed
- Use targeted word lists for better efficiency

**Stealth Considerations**
- Use lower thread counts for stealth
- Implement random delays between attempts
- Monitor for detection by security systems
- Consider time-based restrictions

**Legal and Ethical**
- Always obtain proper authorization
- Respect rate limiting and system resources
- Document all testing activities
- Follow responsible disclosure practices

## Best Practices
- Start with lower thread counts to avoid detection
- Use targeted word lists for better success rates
- Monitor target systems for signs of stress
- Implement appropriate delays between attempts
- Always obtain proper authorization before testing
- Document all testing activities and results