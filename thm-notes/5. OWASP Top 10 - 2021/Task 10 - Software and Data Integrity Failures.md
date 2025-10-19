
### Integrity
----
**What is Integrity?**: `Refers to the capacity to be able to keep data unmodified.`
- Maintaining important data from unwanted or malicious modifications/

**How can we ensure integrity**? :`Hashing`
- Hash sent alongside a file to prove the file downloaded kept its integrity and wasn't modified in transit.
- MD5, SHA1, SHA256



### WinSCP
-----
- Download some files with corresponding hashes
- Once downloaded -> Recalculate and compare against the ones published in Source Forge

**Calculating Hashes**
- `md5sum WinSCP-5.21.5-Setup.exe`
- Compare.


### Software and Data Integrity Failures
--------
**How does this arise?** `From code that uses software or data without integrity checks`.

- No verification is being done, an attacker might modify the software or data passed to the application.

**What are the two main types of vulnerabilities**
- Software Integrity Failures
- Data Integrity Failures


### Software Integrity Failures
--------
**Example:** `A third party website that uses third-party libraries that are stored in external servers (out of your control)`

- **jQuery**, a commonly used javascript library. If you want, you can include jQuery in your website directly from their servers without actually downloading it by including the following line in the HTML code of your website:

```html
<script src="https://code.jquery.com/jquery-3.6.1.min.js"></script>
```

**What if the attacker gains access to the repository?** - `The attacker can inject malicious code by replacing the external script line.`

**Why is this considered Software Integrity Failures**
- Website makes no checks against third-party libraries to check for a change (NO INTEGRITY)


**How can we mitigate this?**
- Specify a hash along library URL so that the library code is executed only if the hash of the downloaded files matches expected.

**What is SRI?** 
- Sending Route Information: Send along a hash with the source file

```html
<script src="https://code.jquery.com/jquery-3.6.1.min.js" integrity="sha256-o88AwQnZB+VDvE9tvIXrMQaPlFFSUTR+nldQm1LuPXQ=" crossorigin="anonymous"></script>
```

You can go to [https://www.srihash.org/](https://www.srihash.org/) to generate hashes for any library if needed.


### Exercise (1)

### Data Integrity Failures
-----
**Big Picture**: How Web Applications maintain sessions
- User logs in to an application
- Assigned session token that is saved on the browser for as long as the session
- Repeated each subsequent request so that web application `knows who we are`
- Usually assigned as **Cookies**
	- **Key-Value Pairs**

**How does a web application store work with cookies?**
- Stores cookie into the user's browser and those will be automatically repeated on each request to the website that issued them.

**What constitutes data integrity failures**
- Trusting data that an attacker can possibly tamper with

**What is the solution?**
- Implement an integrity mechanism to guarantee the cookie hasn't been altered by the user `INTEGRITY`
- Utilize existing token implementations
- Cryptography provides proof of integrity 
- **JSON Web Tokens (JWT)**


### JSON Web Tokens
----
**What is JSON?**
- *JavaScript Object Notation is an open standard file and data interchange format that uses human-readable text to store and transmit data objects consisting of attribute–value pairs and arrays.*


**How do JWT's work?**
- Store key-value pars on a taken **while providing integrity**
- Generate tokens that the user cannot possibly modify (integrity check)
![JSON Web Tokens](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/11c86acaea05f98045cec5634e03e997.png)

Notice that each of the 3 parts of the token is simply plaintext encoded with base64. You can use [this online tool](https://appdevtools.com/base64-encoder-decoder) to encode/decode base64. Try decoding the header and payload of the following token:


**How is it different than a simple hash?**
- Involves the use of a secret key held by the server only
- Change the payload? Mismatching signature unless the secret key is known.




### JWT and NONE Algorithm
----------
Recall: `JWT implements a signature to validate the integrity of the payload data.`
- Vulnerable libraries allow attackers to bypass signature validation by changing 
	- Modifying the header section of the token so that `alg` header would contain `none`
	- Remove the signature part

### Exercise (2)
------
It sounds pretty simple! Let's walk through the process an attacker would have to follow in an example scenario. Navigate to [http://10.10.5.248:8089/](http://10.10.5.248:8089/) and follow the instructions in the questions below.

**`Try logging into the application as guest. What is guest's account password?**
- `guest`

`If your login was successful, you should now have a JWT stored as a cookie in your browser. Press F12 to bring out the Developer Tools.`

Depending on your browser, you will be able to edit cookies from the following tabs:

**Firefox**
![Firefox Developer Tools](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/17765aa7418c977b2d07aa67305e04ad.png)  

**Chrome**
![Chrome Developer Tools](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/cd52fcfd91df145fb31d7bad9b56ebdc.png)

**What is the name of the website's cookie containing a JWT token?**
`jwt-session`

**Use the knowledge gained in this task to modify the JWT token so that the application thinks you are the user "admin".**

- Login to the website using guest credentials
- Once logged in, press `f12` to view `storage` and cookie information
- Decode the "value" and strip the `signature` ... keep the `.`
- encode the values with `alg="none" and user="admin"`
- Update the value parameter with the correct base 64 encodings
- Retrieve the flag
`
**What is the flag presented to the admin user?**
- `THM{Dont_take_cookies_from_strangers}`
