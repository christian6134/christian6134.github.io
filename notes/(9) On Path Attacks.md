
*What is an On Path Attack?*
- Allows an attacker to `sit between 2 devices`
- Watch all the traffic back and forth 
- Also known as a `Man In The Middle Attack`

Redirects traffic
- Then passes it on to the destination
- Some cases, can modify the information before redirecting
- Under the nose of the involved parties (invisible to see)

*Example:*
- ARP Poisoning
- On-path attack on the local IP Subnet
- ARP has no security


#### ARP Poisoning (Spoofing)
-----
1. ARP Request asks for a MAC address corresponding to a certain IP Address
2. Router replies with an ARP reply with its corresponding MAC Address
3. Translation gets cached in the ARP Cache (times out after a certain amount of time)

*Next ARP Request*
1. Attacker sends a falsified ARP request (ARP has no security)
2. Correct ARP Mac ADDRESS has been overwritten with an incorrect MAC Address



#### On Path browser Attack
--------
- What if the middleman was on the same computer as the victim?
	- Malware/Trojan does all of the proxy work?
	- `Man-in-the-browser`

- Huge advantage for attackers
	- Easy to proxy encrypted traffic
	- Everything remains to be normal

- Malware in your browser waits for you to login to your bank



