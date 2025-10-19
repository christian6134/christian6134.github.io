# Task 3 - URL (Uniform Resource Locator)

## Learning Objectives
- Understand the components and structure of URLs
- Learn about different URL schemes and their security implications
- Master URL parsing and analysis techniques
- Identify security risks associated with URL components
- Understand how URLs are used in web attacks

## Overview
A Uniform Resource Locator (URL) is the address used to access resources on the web. Understanding URL structure and components is essential for web development, security analysis, and penetration testing. URLs contain multiple components that can be exploited by attackers if not properly secured.

### URL Components

**Scheme**
- **Protocol used to access the website**
- Most common: **HTTP** (Hypertext Transfer Protocol) and **HTTPS** (Hypertext Transfer Protocol Secure)
- **HTTPS is more secure** because it encrypts the connection
- Browsers and cybersecurity experts recommend HTTPS
- Websites often enforce HTTPS for added protection

**User**
- Some URLs can include **user's login details** (usually username) for authentication
- Mostly used in URLs requiring credentials for resource access
- **Rare nowadays** because putting login details in URL isn't safe
- Can expose sensitive information, creating security risks
- Should be avoided in favor of secure authentication methods

**Host/Domain**
- **Most important part of the URL** - tells you which website you're accessing
- Every domain name must be unique and registered through domain registrars
- **Security concern**: Look for domain names that appear almost like real ones but have small differences
- **Typo squatting**: Practice of registering misspelled variations of popular websites
- Fake domains often used in **phishing attacks** to trick users

**Port**
- **Port number** helps direct browser to the right service on web server
- Like telling the server which doorway to use for communication
- Port numbers range from 1 to 65,535
- Most common: **80 for HTTP** and **443 for HTTPS**
- Custom ports may indicate non-standard services

**Path**
- **Points to specific file or page** on server you're trying to access
- Like a roadmap showing browser where to go
- Websites need to secure these paths
- Ensure only authorized users can access sensitive resources
- Path traversal attacks exploit insecure path handling

**Query String**
- **Part of URL starting with question mark (?)** 
- Often used for search terms or form inputs
- **Security risk**: Users can modify query strings
- Important to handle securely to prevent **injection attacks**
- Malicious code could be added through query parameters

**Fragment**
- **Starts with hash symbol (#)** and points to specific section of webpage
- Like jumping directly to particular heading or table
- **Security risk**: Users can modify fragments
- Like query strings, important to check and clean data
- Can be used in injection attacks if not properly handled

### Security Implications

**Protocol Security**
- Always prefer HTTPS over HTTP
- Implement HTTP Strict Transport Security (HSTS)
- Monitor for protocol downgrade attacks
- Use secure protocols for sensitive communications

**Domain Security**
- Implement Domain Name System Security Extensions (DNSSEC)
- Monitor for typosquatting and domain spoofing
- Use certificate pinning for critical applications
- Implement proper certificate validation

**Path Security**
- Implement proper access controls
- Validate and sanitize path components
- Prevent directory traversal attacks
- Use secure file serving mechanisms

**Parameter Security**
- Validate and sanitize all query parameters
- Implement proper input validation
- Use parameterized queries for database operations
- Monitor for injection attack patterns

### Exercise Answers

**Question 1**: Which protocol provides encrypted communication to ensure secure data transmission between a web browser and a web server?
- **Answer**: HTTPS

**Question 2**: What term describes the practice of registering domain names that are misspelt variations of popular websites to exploit user errors and potentially engage in fraudulent activities?
- **Answer**: typo squatting

**Question 3**: What part of a URL is used to pass additional information, such as search terms or form inputs, to the web server?
- **Answer**: query string

## Best Practices
- Always use HTTPS for sensitive communications
- Implement proper input validation for all URL components
- Monitor for suspicious domain names and typosquatting
- Use secure coding practices for URL handling
- Implement proper access controls for sensitive paths
- Regular security testing of URL-based functionality