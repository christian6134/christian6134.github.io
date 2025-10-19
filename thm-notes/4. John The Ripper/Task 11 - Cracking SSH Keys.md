
**Scenario:** 
- Using John to crack the SSH private key password of `id_rsa` files.
- Configure SSH login through a password
- **OR** Configure SSH login through a key-based authentication
	- Utilize private key `id_rsa` as an authentication key to login to a remote machine over **SSH**


### SSH2John
----
- `ssh2john` converts the `id_rsa` private key which is used to login to a SSH session ----> into **Hash Format**
- `ssh2john.py` located in `/opt/john/ssh2john.py`
- on Attack box -> python3 /opt/john/ssh2john.py
- kali -> python /usr/share/john/ssh2john.py

**Example usage**
- `ssh2john [id_rsa private key file] > [output file]`
- [id_rsa private key file] -> Path to the `id_rsa` you wish to get the hash of


**Exercise**
(1) Convert the id_rsa file to a .txt using:
	`python3 /opt/john/ssh2john.py > rsa.txt`
(2) Invoke john against the rockyou.txt wordlist
	`john --wordlist=/usr/share/wordlists/rockyou.txt rsa.txt`
(3) Password
	`mango`

**More resources**
https://www.openwall.com/john/


