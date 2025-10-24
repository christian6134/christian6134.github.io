
![[SIEM(1).png]]
![[SIEM(2).png]]
### Scenario
---------
You are the Level 1 Analyst of your organization’s SOC team. You receive an alert that a port scanning activity has been observed on one of the hosts in the network. You have access to the SIEM solution, where you can see all the associated logs for this alert. You are tasked to view the logs individually and answer the question to the 5 Ws given below.

**Note**: The vulnerability assessment team notified the SOC team that they were running a port scan activity inside the network from the host: `10.0.0.8`

**What: Activity that triggered the alert?**
- `Port Scan`

**When: Time of the activity?** 
- `June 12, 2024 17:24`

**Where: Destination host IP?** 
- `10.0.0.3`

**Who: Source host name?**  
- `Nessus`

**Why: Reason for the activity? Intended/Malicious**
- `Intended`

**Additional Investigation Notes: Has any response been sent back to the port scanner IP? (yea/nay)**
- `yea`

**What is the flag found after closing the alert?**
`THM{000_INTRO_TO_SOC}`
