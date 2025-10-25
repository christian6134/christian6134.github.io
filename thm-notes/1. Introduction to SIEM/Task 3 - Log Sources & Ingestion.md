
#### Windows Machines
---
**Recall:**
- Windows Event Viewer
- Assigns unique IDs to each type of log activity (events)

These logs from all windows endpoints are forwarded to the SIEM solution for monitoring and better visibility.



#### Linux Workstation
-----
`Common locations where Linux logs are stored...`
- `/var/log/httpd`: Contains HTTP requests / Response and error logs
- `/var/log/cron`: Events related to cron jobs
- `/var/log/auth.log` and `/var/log/secure`: Stores authentication relate logs
- `/var/log/kern`: Stores kernel-related events



#### Web Servers
---------
Apache related logs
- `/var/log/apache` or `var/log/httpd`



#### Log Ingestion
----
Some common methods used by SIEM solutions to ingest logs.

**1. Agent / Forwarder**
- SIEM solutions provides a lightweight tool called `an agent (forwarder by Splunk)`
- Gets installed in the endpoint
- Configured to `capture all important logs and forward them to the SIEM server`

**2. Syslog**
- Widely used protocol to `collect data from various systems`
- Sent real time to the centralized destination

**3. Manual Upload**
- Allow users to ingest offline data for quick analysis
- Once data is ingested it is normalized and made available 

**4. Port Forwarding**
- Configure SIEM solutions to listen on a certain port
- Endpoints forward the data on the listening port


#### What is Splunk?
------
A platform for collecting, storing and analyzing machine data

Provides tools for
- Analyzing data
- Including Search
- Correlation
- Visualization


