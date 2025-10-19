
- Dynamic aspects -> Running processes, services and network connections
- Leverage cmdlets to go **beyond static machine details**


`Get-Process`
- Provides detailed view of all **currently running processes**
- CPU, Memory Usage, Monitoring and Troubleshooting


`Get-Service`
- Allows retrieval of information about **status of services** on the machine
- Running, Stopped or Paused
- Used extensively in troubleshooting by **system administrators**
- Analysis of anomalous services on a system


`Get-NetTCPConnection`
- Displays current TCP connections
- Local and Remote Endpoints
- Handy during **incident response** or **malware task analysis**

`Get-FileHash` 
- Generates file hashes
- Used in **incident response**
- Verifies file integrity and detects potential tampering
- `Get-FileHash -Path .\path`


**Questions**
-----------------
In the previous task, you found a marvellous treasure carefully hidden in the target machine. What is the hash of the file that contains it?
- `Get-FileHash -Path "./hiddentreasure.txt`




