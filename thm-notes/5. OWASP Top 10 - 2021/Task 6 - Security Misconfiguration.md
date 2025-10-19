
### Security Misconfigurations
-----------
**What is a security misconfiguration and what do they include?**: 

Occur when security could have been configured appropriately but was not.

- Poorly configured permissions on cloud services (S3 buckets)
- Unnecessary features
- Accounts with unchanged passwords
- Error messages that are **over-detailed**
- Not using HTTP security 

Can result in more vulnerabilities.
[OWASP top 10 entry for Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)


### Debugging Interfaces
----------------
This is a common security misconfiguration.

**What does Debugging Interfaces Consist of?**
- Exposure of debugging features in production software
- Attackers can abuse debug functionalities if not disabled

**Example of Debugging Interface Misconfiguration**:
- Patreon in 2015
- Console access given to users (from python scripting framework)
- `Werkzeug`


### Exercise
---------
**This VM showcases a `Security Misconfiguration` as part of the OWASP Top 10 Vulnerabilities list.**

**Navigate to [http://10.10.5.248:86](http://10.10.5.248:86/) and try to exploit the security misconfiguration to read the application's source code.**

Use the Werkzeug console to run the following Python code to execute the `ls -l` command on the server:

```python
import os; print(os.popen("ls -l").read())
```

Modify the code to read the contents of the `app.py` file, which contains the application's source code. What is the value of the `secret_flag` variable in the source code?
- `THM{Just_a_tiny_misconfiguration}`
- 
``