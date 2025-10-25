
#### Dashboard
--------
*What are Dashboards*
- Present data for analysis after being `normalized and ingested.`
- Summary of these analyses is presented in the form of actionable insights with the help of multiple dashboards.
- Each SIEM solution comes with default dashboards and provides creation.

Components:
- Alert highlights
- System notifications
- Health Alert
- List of failed login attempts
- Events ingested Count
- Rules triggered
- Top Domains Visited



#### Correlation Rules
--------
*What role do Correlation Rules play?*
- Timely detection of threats, allowing analysts to take action on time
- Logical expressions set to be `triggered`

*Examples of Correlation Rules*
- If a User gets 5 failed login attempts in 10 seconds - Raise
- If login is successful after multiple failed login attempts - Raise
- A rule is set to alert every time a user plugs in a USB 
- Outbound traffic > 25MB - Raise an alert for potential Data exfiltration



#### Correlation Rule Creation
-----
**Use-Case 1:**
Adversaries tend to remove the logs during the post-exploitation phase to remove their tracks. A unique Event ID **104** is logged every time a user tries to remove or clear event logs. To create a rule based on this activity, we can set the condition as follows:

**Rule:** If the Log source is WinEventLog **AND** EventID is **104** - Trigger an alert `Event Log Cleared`



**Use-Case 2:** Adversaries use commands like **whoami** after the exploitation/privilege escalation phase. The following Fields will be helpful to include in the rule.

- Log source: Identify the log source capturing the event logs  
    
- Event ID: which Event ID is associated with Process Execution activity? In this case, event id 4688 will be helpful.  
    
- NewProcessName: which process name will be helpful to include in the rule?  
    

**Rule:** If Log Source is WinEventLog **AND** EventCode is **4688,** and NewProcessName contains **whoami,** then Trigger an ALERT `WHOAMI command Execution DETECTED`



#### ALERT Investigation
----
When monitoring SIEM, analysts spend most of their time on dashboards as it displays various key details about the network in a very summarized way. Once an alert is triggered, the events/flows associated with the alert are examined, and the rule is checked to see which conditions are met. Based on the investigation, the analyst determines if it's a True or False positive. Some of the actions that are performed after the analysis are:

- Alert is False Alarm. It may require tuning the rule to avoid similar False positives from occurring again.  
- Alert is True Positive. Perform further investigation.  
- Contact the asset owner to inquire about the activity.
- Suspicious activity is confirmed. Isolate the infected host.
- Block the suspicious IP.