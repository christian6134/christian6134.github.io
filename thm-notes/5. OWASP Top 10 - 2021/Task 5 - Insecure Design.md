
### Insecure Design
-----
**What is insecure design?**: 
- Refers to the vulnerabilties which are **inherent** to the applications architecture
- Not a result of bad implementation / configuration
- The `whole application is flawed from the start`


**How can we Combat Insecure Design?:** 
- Rebuild vulnerable parts of the application from the ground up
- Take care of the early stages of the development cycle.

**Examples:**
- Improper threat modelling during planning phases
- Introduced "shortcuts" around code to make testing easier


### Insecure Password Resets
------
**Example**: 
- Instagram allowed users to reset their passwords by sending them a `6 digit code` to SMS for validation.
- Attackers want to be able to **BRUTE FORCE** the 6 digit code
- Not possible as Instagram implemented **Rate Limiting**

**What is Rate Limiting?**: `Example: 250 attempts, after that the attacker would be blocked from trying further.`

**However**: 
- The rate limit applied only to the same IP
- More IP addresses? 250 attempts per IP.
- Feasible Attack

**Distributed Brute-Forcing**
![Distributed bruteforcing](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/6e557475b0db7c4be710f75c24889808.png)


### Exercise
----
Navigate to [http://10.10.5.248:85](http://10.10.5.248:85/) and get into joseph's account. This application also has a design flaw in its password reset mechanism. Can you figure out the weakness in the proposed design and how to abuse it?

`Try to reset Joseph's password. Keep in mind the method used by the site.`
`What is the value of the flag in Joseph's Account`

**Your Steps:**
1. Go to the site
2. Click Around
3. Reset password
4. select `What is your favorite color` Security Question
5. Brute force attempts
6. Login using 1-time token


**Answer:**
`THM{Not_3ven_c4tz_c0uld_sav3_U!}`

