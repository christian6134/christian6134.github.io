
### `Considerations
----

#### `Availability
---
- System uptime
- Access data, complete transactions

- A balancing act, it needs to be available to the `right people`
- A lot of money is spent on availability
	- Redundant systems
- An important Metric


#### `Resilience
---
Eventually, something will not be `available`
- "Can you maintain availability?"
- "Can you recover? How quickly"

Based on many different variables
- The root cause
- Replacement hardware installation
- Software patch availability
- Redundant Systems

`MTTR`
- Mean time to Repair



#### `Cost
---
How much money is required?
- Initial installation
	- Very different across various platforms
- Ongoing maintenance costs
	- Replacement or repair costs
	- Tax implications


#### `Responsiveness
---
`Request information`
- Get a response
- How quickly did that Happen?

Especially important for interactive applications
- Humans are sensitive to delays

Speed is another metric
- All parts of the application contribute
- There's always a `weakest link`


#### `Scalability
----
`How quickly and easily can we increase or decrease capacity?`
- This might happen many times a day
- Elasticity

Always a resource challenge
- Whats preventing scalability?
- Money...

Needs to include security monitoring
- Increases and decreases as the system scales


#### `Ease of deployment
----
`Many moving parts of an application`
- Web server, database, caching server, firewall, etc...

A very involved process
- Hardware resources, cloud budgets, change control

Could be very simple
- Orchestration / automation

Important to consider during the product engineering phase
- One missed detail can cause deployment issues


#### `RISK TRANSFERENCE`
----
`Many methods to minimize risk`
- Transfer the risk to a third-part

Cybersecurity Insurance
- Attacks and downtime can be covered
- Popular with the rise in ransomware.

`Recover Internal Losses`
- Outages and business (platform) downtime

`Protect against legal issues from customers`.
- Limit the costs associated with legal proceedings.


#### `Ease of recovery
----
`Something will eventually go wrong.`
- Time is money
- How easily can you recover?

*Example:*
- Malware infection
- Reload operating system from original media ~ 1 hour
- Reload from corporate `image` ~ 10 minutes

`Ease of recovery` is another important design criteria.
- This may be critical to the final product 



#### `Patch availability
----
`Software isn't usually static`
- Bug fixes, security updates, etc.

Patches are usually the first task after installation
- `Are you running the latest version?`

Most companies have regular updates.
- Microsoft monthly patch schedule

Some companies rarely patch
- This could be a significant concern.



#### `Inability to patch
----
`What if patching is not an option?`
- Systems not designed for end-user updates
- Additional security controls

*Examples:*
- Embedded Systems
- HVAC Controls
- Time clocks
- (purpose built systems) no connectivity or internet access
	- Hard to patch




#### `Power
---
`Foundational Element`
- Require extensive engineering.

Various requirements.
- Data center vs. Office Building

`What if power goes down?`
Backup services
- Uninterruptible Power Supply (UPS)
  Power Generators



#### `Compute
---
`An application's heavy lifting`
- More than just a CPU

`The Compute Engine`
- More options available in the cloud
- Could be limited to a single processor
- Easier to develop

`Use multiple CPUS across multiple clouds.`
- Additional complexity
- Enhanced Scalability