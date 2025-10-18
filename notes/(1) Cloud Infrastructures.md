
#### Cloud Responsibility Matrix
---
- IaaS, PaaS, SaaS, etc
	- Infrastructure, Software, Platform ... as a Service 
	- On Premises
- `Who is responsible for security?

![[responsibility-matrix.png]]

`Security should be well documented
- Most cloud providers provide a matrix of responsibilities
- Every knows up front
- Contractual Agreement


`HYBRID CONSIDERATIONS
- Hybrid cloud
- More than 1 public or private cloud
- Adds additional complexity

`Network Protection Mismatches`
- Authentication across platforms
- Firewall configurations
- Server Settings

`Different security monitoring`
- Logs are diverse and cloud-specific

`Data Leakage`
- Data is shared across the public internet


#### Third-Party Vendors in the Cloud
----
- You, cloud provider, third parties
	- Infrastructure technologies
	- Cloud-based appliances

- Ongoing vendor `risk assessment`
	- Part of `risk management policy`

- Include third-party impact for incident response
	- Everyone is part of the process

- Constant Monitoring
	- Watch for changes / unusual activity



#### Infrastructure as Code
---
- Describe an infrastructure
	- Define servers, network, and applications `as code`, not hardware
	- Modify the infrastructure and create versions

- Use the description (code) to build other application instances
	- Build the same instance every time
	- `Significant Benefit` : you can create an infrastructure based on 1 single infrastructure (code)



#### Serverless Architecture
----
Function as a Service (FaaS)
- Applications are separated into individual, autonomous functions
- Remove the Operating System from the equation

Developer still creates server-side logic
- Runs in a stateless compute container
- May be event triggered or ephemeral

Managed by a third-party
- All OS security concerns are at the third party



#### Microservices and APIs
---
- `Monolithic applications
	- One big application that does everything
	- Handles all functions you need

- Application contains all decision making process
	- User interface
	- Business logic
	- Data input and Output

- Code challenges
	- Large codebase
	- Large change control challenges


#### APIs
----
![[microservice-architecture.png]]

API is the glue for the microservices
- Work together to act as the application
- Scalable
- Scale just the micro-services you need

Resilient
- Outages are contained
- Division of labor

Security and Compliance
- Containment is built-in

