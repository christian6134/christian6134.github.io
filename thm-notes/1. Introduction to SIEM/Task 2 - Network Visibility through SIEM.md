
**Consider a topology consisting of**
- 1 Router
- 20 Workstations
- 1 Web Server
- 1 Data Server

All of these network components consist of one or more `log sources` ... generating different logs.


#### Types of Log Sources (2)
--------
**1. Host Centric Log Sources**
*Define:*
- Log sources that capture events that occurred within or related to the host
- Some examples are `Windows Event Logs, Sysmon, Osquery`

*Examples of Host-Centric Logs*
- User access
- User attempting to authenticate
- Process execution activity
- A process adding/editing/deleting a registry key or value
- Powershell Execution


**2. Network Centric Log Sources**
*Define:*
- Network related logs are generated when `hosts communicate with each other or access the internet to visit a website`
- SSH, VPN, HTTPs, FTP

*Examples of Network Centric events*
- SSH connection
- File access over FTP
- Web traffic
- User accessing resources through a VPN
- Network file sharing



#### Importance of SIEM
------
Takes logs from various sources in real-time but also provides the ability to `correlate between events, search through logs, investigate incidents and respond promptly`.

*Key Features of a SIEM*
[] Real-time log ingestion
[] Alerting against abnormal activities
[] 24/7 monitoring and visibility
[] Protection against the latest threats through early detection
[] Data insights and visualization
[] Ability to investigate past incidents.