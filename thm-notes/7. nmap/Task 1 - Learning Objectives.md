**Scenario:** Connected to a network using various network resources (email and web browsing)
- How can we discover other **live devices** on this network or other networks
- How can we figure out the network services running (SSH and web servers)

We could use `ping or arp-scan` however limitations are set
- Ping wont give information on if the target system's firewalls and if it blocks ICMP traffic
- ARP-SCAN only works if your device is connected to the same network (via ethernet or WiFi)

**NMAP**
-------------
- Open-Source network scanner
- use with **SUDO**


**Learning Objectives**
-------------------------------------
<> Discover Live Hosts
<> Find running services on live host
<> Distinguish different types of **port scans**
<> Detect version of the running services
<> Control the timing
<> Format the output

"Who is listening on the network"


