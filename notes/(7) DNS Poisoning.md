
#### Possible Methods
-----
- **Modify the DNS server**
	- Requires some crafty hacking
- Cause a user to navigate to a place they did not usually intend to

- **Modify the client host file**
	- Host file takes precedent over DNS queries
	- Need access (elevated) to Client Computer
	- Client host file acts as a cache 

- **Send a fake response to a valid DNS request**
	- Requires `redirection` of the original request or the resulting response
	- Real-time redirection
	- `On-path` Attack



#### DNS Spoofing / Poisoning
-----
Modify DNS configuration to a different IP address.
- Subsequent requests made to the DNS server results in a malicious IP address returned.


#### Domain Hijacking
---
Get access to the domain registration and you have control where the traffic flows.
- Don't need to interact with the actual servers
- Determines the DNS names and DNS IP Addresses

*Ways to get in.*
- brute force
- social engineering
- gain access to the email address that manages accounts
- other...

*Example*
- Brazilian bank had 36 domain names changed in the DNS settings.
- Under hacker control for 6 hours


#### URL Hijacking / Typosquatting
---
Redirects users to a site with advertising.

*Potential Outcomes:*
- Could have a misspelled domain name to the actual owner
- Could potentially sell this domain name to the owner
- Phishing site, looks like the real thing (please login).
- Infect with a drive-by download (ransomware) (botnet)

`professormessor.com v professormesser.com...`





