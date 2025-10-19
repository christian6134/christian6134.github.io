
**Scenario:** Instead of storing the password, you store its hash value using a secure hashing function.
- Never have to store **the password**

**Problem:** What if two users have the same password
- Hash function will return the same input into the same output
- Store the same hash for each user
- Rainbow Table


**Rainbow Table**
------------------------------
**Define**: Lookup table of **hashes to plaintexts**.
- Quickly find out a password just from the hash
- Takes time to create, cuts time when cracking a password with a present HASH

**Resources**:
- Websites like [CrackStation](https://crackstation.net/) and [Hashes.com](https://hashes.com/en/decrypt/hash) internally use massive rainbow tables to provide fast password cracking for **hashes without salts**. Doing a lookup in a sorted list of hashes is quicker than trying to crack the hash
- ----------------------------------------





**Protecting against Rainbow Tables**:
-------------------------------------------------------
- Add a **salt** to the passwords

Define: **Salt**
- Randomly generated value stored in the database 
- Unique to every user
- Added to the start or end of the password **before it is hashed**
- Every user will have a **different password hash** even if they **have the same password**



### Example of Securely Storing Passwords
------------------------------------------------
1. We select a secure hashing function, such as Argon2, Scrypt, Bcrypt, or PBKDF2.
2. We add a unique salt to the password, such as `Y4UV*^(=go_!`
3. Concatenate the password with the unique salt. For example, if the password is `AL4RMc10k`, the result string would be `AL4RMc10kY4UV*^(=go_!`
4. Calculate the hash value of the combined password and salt. In this example, using the chosen algorithm, you need to calculate the hash value of `AL4RMc10kY4UV*^(=go_!`.
5. Store the hash value and the unique salt used (`Y4UV*^(=go_!`).



**Why don't we just encrypt passwords?**
- Secure hashing algorithm for passwords and storing the key
- If someone gets the key, they can decrypt all passwords

