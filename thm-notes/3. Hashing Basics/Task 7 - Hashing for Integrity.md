
### **Integrity Checking**

Hashing can be used to check that files have not been changed
Data in ---> Same Data out?
- Even if a single bit changes, the hash will change significantly
- Check if file downloaded is identical to the file on the web server
- Can be used to detect duplicate files (same hash -> same document)
	- Convenient for finding and deleting duplicate files


### HMAC (Keyed-Hash Message Authentication Code)
--------------------------------
Type of message authentication code (MAC) that uses a hash function in combination with a secret key to **verify the authenticity and integrity of data**

Can be used to ensure:
- Person who created the HMAC is who they say they are (Authenticity is confirmed)
- Proves the message hasn't been modified or corrupted (Integrity is maintained)
- Achieved through the use of a secret key to prove authenticity and a hashing algorithm to produce a hash and prove integrity

**Procedure**
- Secret key is padded to the block size of the hash function (same size) 
- Padded Key is XORed with a constant (usually a block of zeros)
- Message is hashed using the hash function with the XORed key
- Result from previous step is hashed again with the same hashed function but uses the padded key XORed with another constant
- Final output ---> HMAC Value, fixed size string

![[Pasted image 20250702142818.png]]