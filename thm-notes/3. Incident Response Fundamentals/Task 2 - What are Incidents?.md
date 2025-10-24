
**Context**: 
- There are many different processes running on a system at a given time (Laptop, Phone)
- Some processes are **interactive** (require input e.g Gaming, videos) ... some processes are **not interactive** (simply background processes required for a device to run)

*What are events?*
- Both processes generate several events
- Anything that is **done, is logged as an event**

*Why are events logged?*
- Point to something destructive occurring in a device
- Use security solutions (logs) to find harmful activity


#### Example Workflow
----
**A security solution** detects various events that can be possibly **harmful** to a system.
- An alert is triggered
- Security team analyzes events and deems them as **False or True** positives.

*What is a false positive?*
- Security solution raised an alert due to ...
- Security team analyzes the alert and found that the system was undergoing a standard backup procedure
- **Discard false positives**

*True positive?*
- A security solution raises a phishing alert.
- Upon analysis the security team realizes it is really a phishing alert, this is known as a true positive.



**True positives** are also **Incidents**
- Assign incident severity to decide which alert should be handled first (prioritized).