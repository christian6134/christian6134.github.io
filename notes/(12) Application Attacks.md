
#### Injection
-----
Code Injection
- Adding your own information into a data stream.

*How is this allowed?*
- Poor programming
- `Unsanitized Input`

Types:
- SQL, HTML, XML, LDAP



#### Buffer Overflow
-----
Overwriting a buffer of memory
- Spills over into other memory areas (extra data)

*How is this allowed?*
- No checks for `bound checking`
- Verify input

Not a simple exploit
- Takes time to avoid crashing things
- Takes time to make it do what you want
- Usually `repeatable`



#### Replay Attack
-----
Useful information is transmitted over the network
- Replay information over the server to gain access to the information

Need access to raw network data.
- Network tap, ARP poisoning, Malware on the victim computer
- Gathered information may help the attacker
- Not an on-path attack, doesn't require the original workstation.



#### Privilege Escalation
------
Gaining `higher-level access` to a system
- Exploit a vulnerability
- Might be a bug / design flaw
- More attacker capabilities

High Priority vulnerability
- Perform patches

Horizontal Privilege Escalation
- User A can access user B resources

*How can we mitigate this?*
- Close vulnerabilities by patching quickly
- Update anti-virus / anti-malware
- `Data execution prevention`
	- Only data in executable areas can run
- randomized address space



#### Cross-Site Requests
----------
Common and legitimate
- Information being loaded from different servers
- Normal process that occurs when you visit any website
- HTML directs requests from your browser



#### Client-Server
----
**Client Side**
- HTML, JavaScript
- Renders page on the screen

**Server Side**
- Performs requests from the client
- HTML, PHP
- Transferring money from one account to another
- Posting a youtube video



#### Cross-Site Request Forgery
-----
One-click attack, session riding
- XSRF, CSRF (sea surf)

 Takes advantage of the trust that a web application has for the user.
 - Web site trusts your browser
 - Requests are made without your consent or your knowledge
 - Attacker posts a Facebook status on your account

Significant application development oversight
*Mitigations:*
- Use a cryptographic token to prevent a forgery
- Web server knows (authentication) and presenting a correct token.

![[CSRF.png]]


#### Directory Traversal
---
- Read files from a web server that are outside of the website's file directory.
- Users should not be able to browse the Windows Folder (Out of Scope)

*WHY?*
- Web Server Software Vulnerability
- Web application code vulnerability

Look for `../../` showing a directory traversal