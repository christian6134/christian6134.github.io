
### Physical Isolation
-----
`Devices are physically separate`
- Air gap between Switch A and Switch B
- No way to gain access Switch B from Switch A

Must be connected to provide communication.
- Direct connect, or another switch / router

Web servers in one rack
- Database servers on another

Customer A on one switch, Customer B on another
- No opportunity for mixing data



#### Physical Segmentation
---
- Separate Devices
	- Multiple Devices (units), separate infrastructure
- No connectivity between customer A and customer B



#### Logical Segmentation with VLANs
----
- `Virtual Local Area Networks (VLAN)`
	- Separate logically instead of physically.
	- Cannot communicate between VLANs without a Layer 3 device / router.



#### Software Defined Networking
----
- Networking devices have different `functional planes of operation`
	- `Data, control, management planes.`

*WHY?*
- Separate the functions into separate logical units
	- Extend the functionality and management of a single device
	- Can be easily reproduced


**Infrastructure Layer / Data Plane**
- `Process the network frames and packets
- Forwarding, trunking, encrypting, NAT
- What sends information!


**Control Layer / Control Plane**
- `Manage the actions of the data plane
- Routing tables, session tables, NAT tables
- Dynamic routing protocol updates


**Application Layer / Management Plane**
- Configure and manage the device
- SSH, browser, API


#### SDN Data Flows
-----
![[SDN Flow.png]]