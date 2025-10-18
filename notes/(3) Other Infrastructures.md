
- Two categories for IT security
	- `On-Premises`
	- `Cloud-based`

- `Cloud Based Security`
	- Centralized and costs less
	- No dedicated hardware, no data center to secure
	- A third-party handles everything

- `On-Premises`
	- Puts the burden on the client
	- Data center security and infrastructure costs

- Attackers want your data, they don't care where it is.


### `ON-PREMISES SECURITY`
----
Customize your security posture!
- Control when everything is in-house

- On site IT team can manage security better
	- Local team can ensure everything is seccure
	- Local team can be expensive and difficult to staff

- Local team maintains uptime and availability
	- System checks can occur at any time
	- No phone call for support

- Security changes take time...


#### `CENTRALIZED v DECENTRALIZED`
------
- Most organizations are `physically decentralized
	- Many locations, cloud providers, operating systems
- Difficult to manage and protect so many diverse systems
	- Centralize the security management
- A `centralized approach
	- Correlated alerts 
	- Consolidated log file analysis
	- Comprehensive system status and maintenance/patching

A centralized approach is not perfect ... it has a `single point of failure` and potential performance issues. 



#### `VIRTUALIZATION`
-----
- `Virtualization
	- Run many different operating systems on the same hardware.

*CHALLENGES:*
- each application instance has its own operating system
- adds overhead and complexity
- virtualization is relatively expensive

*The HyperVisor*:
- Manage all resources between the separate virtual machines



#### `APPLICATION CONTAINERIZATION`
----
`Container`
- Contains everything you need to run an application
- Code and dependencies
- A standardized unit of software

`Has everything you need` except the Operating System.

Containers are isolated processes within a sandbox.
- Self-contained
- Apps can't interact with each other

Container Image
- A standard for portability
- lightweight, uses the host kernel
- Secure separation between applications 


#### `VIRTUALIZATION v CONTAINERIZATION`
-----
![[virtual-container.png]]



#### `IoT (internet of things)`
-----
`Devices that are designed to be integrated in a network and support features and services.`

*Example:*
- Temperature Sensors
- Automatic lighting system
- Smart devices
	- Home automation, garage door openers
	- Ring doorbells
- Smart watches, health monitors
- Very convenient, but `Weak Defaults`
	- IOT manufacturers are `not security professionals.`



#### `SCADA / ICS
-----
- `Supervisory Control and Data Acquisition System`
	- Large scale, multi-site Industrial Control Systems (ICS)
- PC manages equipment
	- Power generation, refining, manufacturing
- Distributed control systems
	- real-time information
	- system control
- Requires `extensive segmentation`
	- No access from the outside




#### `RTOS (Real-Time Operating System`)
---
*What is a RTOS?*
- An operating system with a `deterministic processing schedule`
	- No time to wait for other processes
	- Industrial equipment, automobiles
	- Military Environments
- *Example:*
	- Driving a car, pressing the brakes requires full attention

- `Non-Deterministic Processing (Operating System)`
	- No process can take all the resources at a given time 
	- No priority
	- *Examples:*
		- Windows, Linux, IOS, Android

*Drawbacks?*
- Extremely sensitive to security issues
	- Non-trivial systems
	- Need to be available
	- Difficult to know security implementations in place




#### `Embedded Systems`
---
`Hardware and software are built and designed for a specific function.`
- Or to operate as a large system

Is built with only this task in mind
- Can be optimized for size and or cost

*Examples:*
- Traffic Light Controllers
- Digital watches
- Medical Imaging Systems



### `High Availability`
---
- Redundancy doesn't mean its always available
	- May need to be powered on manually

- HA (High Availability)
	- `Always on, always available`
- May include many different components working together
- Active / Active can provide scalability advantages

- Higher availability almost always means `higher costs`
	- *Example*
		- 2 separate firewalls to ensure availability