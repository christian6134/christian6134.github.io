
### Insecure Direct Object Reference
----------
(IDOR)
- Access Control Vulnerability
- Access resources you shouldn't be able to see

**How does this occur?**
- Programmers exposing Direct Object References

**What is Direct Object Reference?** 
- An Identifier that `refers to specific objects within the server`
- E.g. File, User, Bank Account, Anything.

### Example
----

 Let's say we're logging into our bank account, and after correctly authenticating ourselves, we get taken to a URL like this `https://bank.thm/account?id=111111`. On that page, we can see all our important bank details, and a user would do whatever they need to do and move along their way, thinking nothing is wrong.

![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/0ddb5676eebdb367bff750717268b82b.png)  

There is, however, a potentially huge problem here, anyone may be able to change the `id` parameter to something else like `222222`, and if the site is incorrectly configured, then he would have access to someone else's bank information.

![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/42a83d8c119295a79dfcab36b7e4d105.png)

The application exposes a direct object reference through the `id` parameter in the URL, which points to specific accounts. Since the application isn't checking if the logged-in user owns the referenced account, an attacker can get sensitive information from other users because of the IDOR vulnerability. Notice that direct object references aren't the problem, but rather that the application doesn't validate if the logged-in user should have access to the requested account.


#### Exercises
-----
**Deploy the machine and go to [http://10.10.215.157](http://machine_ip/)[](http://machine_ip/) - Login with the username `noot` and the password `test1234`.**

**Look at other users' notes. What is the flag?**
- Simply change the note_id reference
- IDOR Vulnerability does not verify if we have the correct permissions to the reference account (note_id=0)
- **Flag:** flag{fivefourthree}

