
**Scenario:** How do we crack passwords with Salts?

**Problem:** You can't "decrypt" password hashes because they are not encrypted
- You must crack the hashes by hashing many different inputs
- Potentially adding salt if there is one and comparing it to the target hash
- Tools like [Hashcat](https://hashcat.net/hashcat/) and [John the Ripper](https://www.openwall.com/john/)


**Cracking Passwords with GPUs**
- Modern GPUs have thousand of cores
	- Specialized in digital image processing and accelerating computer graphics
	- Can perform mathematical calculations involved in **hash functions**



### **Exercise: Crack Hashes**
---------------
(1) Use `hashcat` to crack the hash, `$2a$06$7yoU3Ng8dHTXphAg913cyO6Bjs3K5lBnwq5FJyA6d01pMSrddr1ZG`, saved in `~/Hashing-Basics/Task-6/hash1.txt`.
- `hashcat -m 3200 -a 0 hash1.txt rockyou.txt`
- Run hashcat in Bcrypt mode (3200) 
- -a 0 indicates a standard dictionary attack
- Wordlist being used = rockyou.txt
**Answer: 85208520**



(2) Use `hashcat` to crack the SHA2-256 hash, `9eb7ee7f551d2f0ac684981bd1f1e2fa4a37590199636753efe614d4db30e8e1`, saved in saved in `~/Hashing-Basics/Task-6/hash2.txt`.
- `hashcat -m 1400 -a 0 hash2.txt rockyou.txt`
- SHA 2 256 ---> Mode 1400
**Answer: halloween**


(3) Use `hashcat` to crack the hash, `$6$GQXVvW4EuM$ehD6jWiMsfNorxy5SINsgdlxmAEl3.yif0/c3NqzGLa0P.S7KRDYjycw5bnYkF5ZtB8wQy8KnskuWQS3Yr1wQ0`, saved in `~/Hashing-Basics/Task-6/hash3.txt`.
- Mode sha512crypt ----> 1800
- `hashcat -m 1800 -a 0 hash3.txt rockyou.txt`
**Answer: spaceman**




