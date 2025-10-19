
### **Linux Passwords**
----------------------
Password hashes are stored in `/etc/shadow`
- Normally readable by root
- `shadow` file contains password info
	- 9 fields separated by `:`
	- First two fields: Login name and Encrypted password
	- `man 5 shadow`

Encrypted password field contains **hashed passphrase** with **4 components.**
`$prefix$options$salt$hash`

![[Pasted image 20250702132632.png]]

**Example**
`root@TryHackMe# sudo cat /etc/shadow | grep strategos strategos:$y$j9T$76UzfgEM5PnymhQ7TlJey1$/OOSg64dhfF.TigVPdzqiFang6uZA4QA1pzzegKdVm4:19965:0:99999:7:::`

In the example above, we have four parts separated by `$`:
- `y` indicates the hash algorithm used, **yescrypt**
- `j9T` is a parameter passed to the algorithm
- `76UzfgEM5PnymhQ7TlJey1` is the salt used
- `/OOSg64dhfF.TigVPdzqiFang6uZA4QA1pzzegKdVm4` is the hash value


### MS Windows Passwords
---------------------------------------
Hashed using NLTM (Variant of MD4)
- Password hashes are stored in SAM (Security Accounts **Manager**)
- Prevents normal users from dumping
- Hashes are split into NT hashes and LM hashes