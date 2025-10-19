
**Recall**:
`/etc/shadow` file on Linux machines contains password hashes.
- Stores extraneous information
	- Date of last password change
	- Password expiration information
	- One entry per line for each user on system
	- Only accessible by **root**

### Unshadowing
---------
**Note**: John is very picky with his formats in order to work.
- To crack `/etc/shadow` passwords you must combine it with `/etc/passwd` file for John to understand the data being given.

We use a tool built into the John suite called `unshadow`.

**Procedure:**
- `unshadow`
- [path to passwd] -> File that contains the copy of the /etc/passwd file you've taken from the target machines
- [path to shadow] -> File that contains the copy of the /etc/shadow file from the target machine


**Cracking**
- Feed the output from `unshadow` to `a .txt file`. 
- May need to specify format as `--format=sha512crypt`

ex: `john --wordlist=/usr/share/wordlists/rockyou.txt --format=sha512crypt unshadowed.txt`


**Exercise**
----------
What is the roots password?
`unshadow local_pw locaL_shadow > unshadowed.txt`
- `john --format=sha512crypt --wordlist=/usr/share/wordlists/rockyou.txt etc-hashes.txt`
- Password: 1234

