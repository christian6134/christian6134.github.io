
**Focus**:
- Password Storage
- Data Integrity
Password Storage when used for **Authentication**

*Note*: Does not apply to password managers where you must retrieve a password in cleartext.
- **Authentication mechanisms only need to confirm that the user knows the password**
- Differ from password managers




**Three Insecure Practices**:
------------------------------------------------
- Storing passwords in plaintext (rockyou company breach)
- Storing passwords using a deprecated encryption
- Storing passwords using an insecure hashing algorithm


**Password Salting**: Adding a salt, i.e, a random value to the password before it is hashed.




**Questions**
---------
What is the 20th password in `rockyou.txt`?
`head -n 20 rockyou.txt`
- qwerty
