# Task 5 - HTTP Request Line and Methods

## Learning Objectives
- Understand the structure and components of HTTP request lines
- Learn about different HTTP methods and their purposes
- Master security implications of each HTTP method
- Understand URL path security considerations
- Learn about HTTP version differences and security implications

## Overview
HTTP requests are the primary means of communication between clients and web servers. Understanding request structure, methods, and security implications is crucial for both web development and cybersecurity professionals who need to analyze, secure, and test web applications.

### HTTP Request Structure

**Request Line Components**
- **HTTP Method**: Tells server what action user wants to perform
- **URL Path**: Identifies the resource being requested
- **HTTP Version**: Specifies protocol version for communication
- **Format**: `METHOD /path HTTP/version`

### HTTP Methods and Security

**GET**
- **Purpose**: Used to **fetch** data from server without making changes
- **Security Reminder**: Only expose data user is allowed to see
- **Risk**: Avoid putting sensitive info like tokens or passwords in GET requests
- **Issue**: Can show up as plaintext in logs and browser history

**POST**
- **Purpose**: **Sends** data to server, usually to create or update something
- **Security Reminder**: Always validate and clean input to avoid attacks
- **Risks**: SQL injection, XSS, and other injection attacks
- **Best Practice**: Implement proper input validation and sanitization

**PUT**
- **Purpose**: Replaces or **updates** something on the server
- **Security Reminder**: Ensure user is authorized to make changes
- **Risk**: Unauthorized modification of resources
- **Best Practice**: Implement proper authorization checks

**DELETE**
- **Purpose**: **Removes** something from the server
- **Security Reminder**: Ensure only authorized users can delete resources
- **Risk**: Unauthorized deletion of critical data
- **Best Practice**: Implement strong authorization and confirmation mechanisms

### Additional HTTP Methods

**PATCH**
- **Purpose**: Updates part of a resource without replacing the whole thing
- **Security Consideration**: Always validate data to avoid inconsistencies
- **Use Case**: Making small changes efficiently

**HEAD**
- **Purpose**: Works like GET but only retrieves headers, not full content
- **Use Case**: Checking metadata without downloading full response
- **Security**: Can be used for reconnaissance by attackers

**OPTIONS**
- **Purpose**: Tells you what methods are available for specific resource
- **Security Risk**: Can reveal server capabilities to attackers
- **Best Practice**: Disable if not needed to avoid security risks

**TRACE**
- **Purpose**: Shows which methods are allowed, often for debugging
- **Security Risk**: Can be used for cross-site tracing attacks
- **Best Practice**: Many servers disable it for security reasons

**CONNECT**
- **Purpose**: Used to create secure connection, like for HTTPS
- **Use Case**: Critical for encrypted communication
- **Security**: Essential for secure tunneling

### URL Path Security

**Path Manipulation**
- **Attack Vector**: Attackers often try to manipulate URL path to exploit vulnerabilities
- **Examples**: Directory traversal, path injection, unauthorized access

**Security Measures**
- **Validate URL path** to prevent unauthorized access
- **Sanitize path** to avoid injection attacks
- **Protect sensitive data** by conducting privacy and risk assessments
- **Implement proper access controls** for sensitive resources

### HTTP Versions

**HTTP/0.9 (1991)**
- First version, only supported GET requests
- Limited functionality and security features

**HTTP/1.0 (1996)**
- Added headers and better support for different content types
- Improved caching capabilities

**HTTP/1.1 (1997)**
- Brought persistent connections and chunked transfer encoding
- Better caching mechanisms
- **Still widely used today** due to broad support

**HTTP/2 (2015)**
- Introduced multiplexing, header compression, and prioritization
- Faster performance and better efficiency
- Enhanced security features

**HTTP/3 (2022)**
- Built on HTTP/2 but uses QUIC protocol
- Quicker and more secure connections
- Latest standard with improved performance

### Security Considerations

**Method Security**
- Each HTTP method has specific security rules
- PATCH requests should be validated to avoid inconsistencies
- OPTIONS and TRACE should be disabled if not needed
- Implement proper authorization for state-changing methods

**Version Security**
- HTTP/2 and HTTP/3 offer better speed and security
- Many systems still use HTTP/1.1 for compatibility
- Upgrading can provide significant performance and security improvements

## Best Practices
- Use appropriate HTTP methods for intended actions
- Implement proper input validation for all methods
- Disable unnecessary HTTP methods (OPTIONS, TRACE)
- Use HTTPS for all sensitive communications
- Implement proper authorization checks for state-changing methods
- Monitor and log HTTP requests for security analysis