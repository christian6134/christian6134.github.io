
# 2.5.3 Hardening Techniques

#### System Hardening
------
- Varied Operating Systems (Windows, Linux, iOS, Android)
- Updates (Operating System updates/service packs, security patches)

 `USER ACCOUNTS
	- Minimum password length and complexity
	- Account limitations
	
`Network Access and Security
	- Limit Network Access

`Monitor and Secure`
- Anti-virus, Anti-malware


#### `ENCRYPTION
-----
`Prevent Access to Application Data Files
- file level
- windows encrypting file system (EFS)
`Full disk encryption (FDE)
- BitLocker, FileVault
`Encrypt all network communication
- VPN
- Application Encryption


#### `EDR` (Endpoint Detection and Response)
----
`A different method of threat protection`
- Scale to meet the increasing number of threats

Detect a threat
- Signatures aren't the only detection tool
- Behavioral analysis, Machine Learning, Process monitoring
- Lightweight agent on the endpoint

Investigate the Threat
- `Root cause analysis`

Respond to the threat
- Isolate the system, quarantine threat, rollback to a previous config
- API driven, no user intervention required



#### `HOST-BASED FIREWALL`
------
- Software based firewall
	- Personal, runs on every endpoint

- Allow or disallow incoming or outgoing traffic
	- Control by application process
	- View all Data

- Identify and block unknown processes
	- Stop malware before it can start



#### Finding Intrusions
-----
- Host Based Intrusion Prevention Systems
	- Recognize and block known attacks
	- Secure OS and configs
	- Validate incoming service requests
	- Often built into `endpoint protection software`

- HIPS Identification
	- Signatures, behavioral changes
	- Access to non-encrypted data



#### `PORTS AND SERVICES`
-----------------
Every open port is a possible entry point
- Close everything except required ports

Control access with a firewall
- Next Generation Firewall would be ideal

Unused or unknown services
- Installed with the OS or from other applications

`Nmap` or similar port scanner to verify
- Ongoing monitoring



#### Default Password Changes
----
Every network device has a management interface
- Critical Systems, other devices

Many applications also have management or maintenance interfaces
- These can contain sensitive data

Change default settings
- Passwords



#### `REMOVAL OF UNNECESSARY SOFTWARE`
-----
All software contains bugs!
- Some are security risks

Every application seems to have a different patching process
- Can be challenging to manage ongoing updates


Instead,
- Remove all unused software
- Get rid of the security concern 