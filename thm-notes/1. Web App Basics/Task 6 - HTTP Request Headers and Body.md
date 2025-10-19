# Task 6 - HTTP Request Headers and Body

## Learning Objectives
- Understand common HTTP request headers and their purposes
- Learn about different request body formats and their use cases
- Master security implications of various header and body types
- Understand how headers guide web server request processing
- Learn to identify and analyze different content types

## Overview
HTTP request headers and body provide essential information that guides how web servers process requests. Understanding these components is crucial for web development, security analysis, and penetration testing, as they can contain sensitive information and be vectors for various attacks.

### Common Request Headers

**Host Header**
- **Example**: `Host: tryhackme.com`
- **Purpose**: Specifies the name of the web server the request is for
- **Security**: Essential for virtual hosting and can be manipulated for attacks
- **Use Case**: Required in HTTP/1.1 requests

**User-Agent Header**
- **Example**: `User-Agent: Mozilla/5.0`
- **Purpose**: Shares information about the web browser making the request
- **Security**: Can be spoofed for evasion or fingerprinting
- **Use Case**: Server-side browser detection and analytics

**Referer Header**
- **Example**: `Referer: https://www.google.com/`
- **Purpose**: Indicates the URL from which the request came from
- **Security**: Can be manipulated for CSRF attacks or privacy violations
- **Use Case**: Analytics, CSRF protection, and navigation tracking

**Cookie Header**
- **Example**: `Cookie: user_type=student; room=introtowebapplication; room_status=in_progress`
- **Purpose**: Contains information web server previously asked browser to store
- **Security**: Critical for session management and authentication
- **Risk**: Can be stolen or manipulated for session hijacking

**Content-Type Header**
- **Example**: `Content-Type: application/json`
- **Purpose**: Describes what type or format of data is in the request
- **Security**: Important for preventing MIME-type confusion attacks
- **Use Case**: Server-side content processing and validation

### Request Body Formats

**URL Encoded (application/x-www-form-urlencoded)**
- **Format**: Data structured in key=value pairs
- **Separator**: Multiple pairs separated by (&) symbol
- **Encoding**: Special characters are percent-encoded
- **Use Case**: Standard form submissions
- **Example**: `name=Aleksandra&age=27&country=US`

**Form Data (multipart/form-data)**
- **Format**: Multiple data blocks separated by boundary string
- **Boundary**: Defined in request header
- **Use Case**: File uploads and binary data transmission
- **Security**: Can be used for file upload attacks
- **Example**: File uploads with images and documents

**JSON (application/json)**
- **Format**: JavaScript Object Notation structure
- **Structure**: name: value pairs separated by commas in curly braces
- **Use Case**: Modern web APIs and AJAX requests
- **Security**: Vulnerable to JSON injection attacks
- **Example**: `{"name": "Aleksandra", "age": 27, "country": "US"}`

**XML (application/xml)**
- **Format**: Data structured in tags with opening and closing elements
- **Structure**: Nested tags for hierarchical data
- **Use Case**: Legacy systems and enterprise applications
- **Security**: Vulnerable to XML injection and XXE attacks
- **Example**: `<user><name>Aleksandra</name><age>27</age></user>`

### Security Implications

**Header Security**
- **Host Header Attacks**: Manipulation for cache poisoning and password reset attacks
- **User-Agent Spoofing**: Used for evasion and fingerprinting
- **Referer Manipulation**: CSRF attacks and privacy violations
- **Cookie Theft**: Session hijacking and unauthorized access

**Body Security**
- **Injection Attacks**: SQL injection, XSS, command injection through body content
- **File Upload Attacks**: Malicious file uploads through multipart/form-data
- **JSON Injection**: Manipulation of JSON data for attacks
- **XML Attacks**: XXE (XML External Entity) and XML injection

### Exercise Answers

**Question 1**: Which HTTP request header specifies the domain name of the web server to which the request is being sent?
- **Answer**: HOST

**Question 2**: What is the default content type for form submissions in an HTTP request where the data is encoded as key=value pairs in a query string format?
- **Answer**: URL Encoded (application/x-www-form-urlencoded)

**Question 3**: Which part of an HTTP request contains additional information like host, user agent, and content type, guiding how the web server should process the request?
- **Answer**: Request Headers

### Practical Applications

**Web Development**
- Implementing proper content type handling
- Building secure form processing
- Managing file uploads safely
- Implementing proper header validation

**Security Analysis**
- Analyzing HTTP requests for attack patterns
- Identifying malicious headers and body content
- Implementing security controls for different content types
- Monitoring for injection attacks

**Penetration Testing**
- Testing for header manipulation vulnerabilities
- Analyzing request body for injection points
- Testing file upload functionality
- Identifying information disclosure through headers

## Best Practices
- Validate and sanitize all request headers
- Implement proper content type validation
- Use secure file upload mechanisms
- Implement proper input validation for all body formats
- Monitor for suspicious header patterns
- Use HTTPS to protect sensitive header and body data