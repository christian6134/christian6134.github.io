
# 2.5.2 Mitigation Techniques

`Process of reducing the impact of a security or potential security event.`

**`PATCHING`**
- System stability, security fixes.
- Monthly updates.
- Third-party updates
	- Application developers, device drivers
	- Auto-update
- Emergency out-of-band updates



****`ENCRYPTION`
- Prevent access to application data files
	- File system encryption
- **File level encryption**
	- Windows EFS
- **Full Disk Encryption (FDE)**
	- Encrypt everything on the drive
	- BitLocker, FileVault
- **Application Data Encryption**
	- Managed by Application
	- Always protected



****`MONITORING`
- Aggregate information from devices
	- Built-in sensors, separate devices
	- Integrated into servers, switches, routers, firewalls
- **Sensors**
	- Intrusion prevention systems, firewall logs, authentication logs, web server access logs, database transaction logs, email logs
- **Collectors**
	- SIEM console
	- Correlation engine to compare diverse sensor data



****`LEAST PRIVILEGE`
- Rights and permissions should be set to the bare minimum
- You only get exactly what is needed to complete your objective

- All users account must be limited
- Don't allow users to run with administrative privileges
	- Limits the scope of malicious behavior



****`CONFIGURATION ENFORCEMENT`
- Perform a `posture assessment`
	- Each time a device connects
- **Extensive Check**
	- OS PATCH
	- EDR Version
	- Status of Firewall and EDR
	- Certificate Status
- **Systems out of Compliance**
	- Private VLAN with limited access
	- Quarantined, recheck after making corrections.



****`DECOMMISSIONING`
- Should be a formal policy
	- Don't throw your data into the trash
	- Someone will find it later
- Most associated with `storage devices
	- HDD
	- SDD
	- USB
- Many options for physical devices
	- Recycle device for use in another system
	- Destroy the device

