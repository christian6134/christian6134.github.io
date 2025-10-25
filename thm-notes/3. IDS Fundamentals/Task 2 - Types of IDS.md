
*Note:*
- An IDS's main categorization lies on its `deployment and detection modes.`

#### Deployment Modes 
-------
**1. Host Intrusion Detection System (HIDS)**
- Installed individually on the hosts
- Responsible for `detecting potentional security threats associated with a particular host.`
- Provide `detailed visibility of a host's activities.`
- Challenging to manage in `large networks` as they are `resource-intensive.`

**2. Network Intrusion Detection System (NIDS)**
- Detect malicious activities `within the whole network.`
- Monitor network traffic of `all hosts involved`
- Provides a `centralized view of all detections` inside a network.



#### Detection Modes
-------
**1. Signature-based IDS** "We seen you before bro"
- Each attack has a `unique pattern` also known as a `signature.`
- These signatures are `preserved by the IDS` so if the same attack happens, it gets detected `by the signature`.

*Cons:*
- Cannot detect `zero-day attacks` as they do not 'exist' or have not happened yet (not in the signature database.)
- Can only detect `attacks` that have happened `previously`


**2. Anomaly-Based IDS** "Something is Off"
- Learns `normal behavior (Baseline)` of the network / system.
- Performs detections if there is `any deviation` from normal behavior.
- Able to detect `zero-day attacks`

*Cons:*
- Generates a larger amount of `false positives.`
- Able to `fine-tune` by manually defining normal behavior in IDS


**3. Hybrid IDS**
- Combines both of above

