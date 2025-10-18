
# 2.5.1 Segmentation and Access Control

#### Segmenting the Network
------
*Why?*
- Limit the scope of a security event.

*How?*
- Physical, logical, virtual
- Devices, VLAN, Virtual Network

`Performance
- High-bandwidth application get its own network
- So it runs efficiently as possible
- Throughput is not effected by other users

`Security
- Users should not be directly communicating with a database server
- Could be implemented through a Firewall

`Compliance
- Mandated Segmentation (PCI Compliance)
- Makes change control much easier



#### Access Control Lists
----
- `Allow or disallow traffic
	- Grouping of categories
	- Source IP, Dest IP, port numbers, time of day, etc...

- `Restrict access to network devices
	- Limit by IP addresses
	- Prevent regular user / non-admin access

- `Take all networks into account`

*Example*
- Bob can read files
- Fred can access the network
- James can access 192.168.1.0/24 using only ports 80, 433, 8088
- `Very granular control`



#### Application Allow / Deny
---
- `Any application can be dangerous
	- Vulnerabilities, trojan horses, malware

- `Security Policy can control app execution`
	- Allow list, deny/block list
	- Either a Whitelist or a Blacklist
	- `Nothing is allowed, allow manually
	- `Everything is allowed, block manually

*WHERE are decisions made?*
- Within the Operating System
- Use Application Hash
	- Prevent changed Applications
	- Some provide Digital Certificates (Trusted by a CA)

- `Path`
	- Only run applications in these folders

- `Network Zone`
	- App can only run from this network zone