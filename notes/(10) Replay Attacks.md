


*What is needed for a Replay Attack?*
- Attacker needs access to `raw network data`
- Network tap, ARP poisoning, Malware on the victim computer

Not an actual on-path attack
- The actual replay doesn't require the original workstation


#### Pass the Hash
--------
Form of a replay attack.

1. Client sends a normal authentication request to the server
2. Attacker captures authentication (Username and hashed password)
3. Attacker sends his own authentication request 
	1. Poses as the original client
4. Server receives proper username and password
5. Attacker has access to the server posing as the victim server

*Fixes*
- Use encryption
- Salting of passwords
- Do not access the same hash more than once (prevent replay)


#### Browser Cookies and Session IDS
----
Files that store information about your visited sites.

Used for tracking, personalization and session management.

Considered a privacy risk.
- Lots of personal data.

Session IDS are often stored in the cookie
- Maintain sessions


#### Session Hijacking (SideJacking)
------------
Attacker gains access to the session ID.
- Used for subsequent sessions to the web server
- Attacker has access to victim machine information on the web server



#### Header Manipulation
---------
- Information gathering
	- Wireshark, Kismet
- Exploits
	- Cross site scripting
- Modify headers
	- tamper, firesheep, scapy
- Modify cookies
	- Cookies Manager


#### Preventing Session Hijacking
----
ENCRYPT ANYTHING AND EVERYTHING.
- End-to-End 
- Not able to capture Session ID's (HTTPs)

Encrypt for parts of the journey if possible.