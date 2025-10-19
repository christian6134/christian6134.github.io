
**Define**: Authentication Hashes
- Hashed versions of passwords stored by **operating systems**
- Possible to crack them using a brute force method.
- Usually need privilege to get your hands on these hashes


### NTHash / NTLM
-----
**NTHash**: Hash format of modern Windows Operating System machines
- Used to store user and service passwords

**Note**: Commonly reffered to as NTLM (interchangeably) 


**Recall:**
- Security Account Manager (SAM) is used to store **user account information including usernames and hashed passwords**

Could acquire NTHashes by dumping the SAM Database or using the **Active Directory Database** `NTDS.dit`


**Exercise**
---------------
What do we need to set the `--format` flag to in order to crack this hash? (ntlm.txt)
- **Find the type of Hash (ID)**
- Possible Hash ID -> MD5, MD4
- It was really **NT**
Cracked Value:
- **Mushroom**


