
*Note:*
- Firewalls (different types) work on different `layers of the OSI model`.

#### Some common types of Firewalls and their Roles in the `OSI Model`.
----------------------
**1. Stateless Firewall** (Slow Learner)
Operates on layers 3 and 4 of the OSI Model

*How does it work?*
- Works solely by `filtering data based on predetermined rules` without taking note of the state of the previous connections
- Matches every packet with the rules whether it is part of a legitimate connection

Maintains `no information`, allows for `faster processing of packets`.
- Cannot apply `complex policies` to the data based on relationships.
- I.E. This firewall does not make intelligent decisions (checks every packet)
- Cannot establish relationships.



**2. Stateful Firewall** (Quick Learner)
Operates on layers 3 and 4 of the OSI Model

*How does it work*?
- It does what `Stateless Firewalls DO NOT`
- Keeps track of previous connections and is able to allow further traffic from a trusted source
- Can also deny traffic based off a deny table (keeping tabs for the future)


**3. Proxy Firewall**
- Unlike the (2) previous firewalls, this firewall can `inspect the contents of a packet`. 
- Also known as application-level gateways
	- Act as an `intermediary between private networks and the internet`
	- Operate on the OSI model's layer 7
- Inspects the contents of a packet and masks the IP Address
- Can also apply content filtering policies (allow/deny)

**4. Next-Generation Firewall (NGFW)**
- Operates from `layer 3 to layer 7`
- Offers deep packet inspection
- Includes an intrusion prevention system that `blocks malicious activities in real time`

Other Capabilities
- SSL/TLS decryption
- Identifies anomalies based on attack pattern


![[firewall-types.png]]

