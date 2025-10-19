
**Big Picture:** Once a web application is up and running, every action that takes place should be logged. In the `event of an incident, we can trace attacker's actions.`

### Security Logging
----
**What are some possibilities without Security Logging functions.**

- **Regulatory Damage:** if an attacker has gained access to personally identifiable user information and there is no record of this, final users are affected, and the application owners may be subject to fines or more severe actions depending on regulations.

- **Risk of further attacks:** an attacker's presence may be undetected without logging. This could allow an attacker to launch further attacks against web application owners by stealing credentials, attacking infrastructure and more.


**What might be some information that should be stored in Security Logs?**
- HTTP status codes
- Time stamps
- Usernames
- API endpoints/page locations
- IP addresses



### Monitoring
-----
Have monitoring in place to detect any suspicious activity.

**What is the goal of monitoring?:** `Either stop the attacker completely or reduce the affects after their presence has been detected.`

**What are some examples of suspicious activity?**
- Multiple unauthorised attempts for a particular action (usually authentication attempts or access to unauthorised resources, e.g. admin pages)
- Requests from anomalous IP addresses or locations: while this can indicate that someone else is trying to access a particular user's account, it can also have a false positive rate.
- Use of automated tools: particular automated tooling can be easily identifiable, e.g. using the value of User-Agent headers or the speed of requests. This can indicate that an attacker is using automated tooling.
- Common payloads: in web applications, it's common for attackers to use known payloads. Detecting the use of these payloads can indicate the presence of someone conducting unauthorized/malicious testing on applications.



### Exercise (Security Logs)
----
200 OK           12.55.22.88 jr22          2019-03-18T09:21:17 /login
200 OK           14.56.23.11 rand99        2019-03-18T10:19:22 /login
200 OK           17.33.10.38 afer11        2019-03-18T11:11:44 /login
200 OK           99.12.44.20 rad4          2019-03-18T11:55:51 /login
200 OK           67.34.22.10 bff1          2019-03-18T13:08:59 /login
200 OK           34.55.11.14 hax0r         2019-03-21T16:08:15 /login
401 Unauthorised 49.99.13.16 admin         2019-03-21T21:08:15 /login
401 Unauthorised 49.99.13.16 administrator 2019-03-21T21:08:20 /login
401 Unauthorised 49.99.13.16 anonymous     2019-03-21T21:08:25 /login
401 Unauthorised 49.99.13.16 root          2019-03-21T21:08:30 /login 

**What is the IP of the attacker?**
- `49.99.13.16`

**What type of attack is this?**
- `Brute Force`



