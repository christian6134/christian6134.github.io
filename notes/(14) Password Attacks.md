
`Plaintext / Unencrypted Passwords`
- "In the clear"
- No encryption, you can read the stored password
- **DO NOT** store passwords as plaintext


`Hashing a PASSWORD`
- Hashes represent data as a fixed-length string of text
- Message digest or "Fingerprint"
- No collision! (Hopefully)

One way trip
- Impossible to recover from the original digest
- Cannot reconstruct a password from a hash


### Attacks
----
##### Spraying Attack
---
- Try to login with an incorrect password
	- Eventually you are locked out

Attack an account with the top three (or more) passwords
- If they don't work, move to the next account
- No lockouts, alarms, alerts


#### Brute Force
---
Trying many different iterations of passwords until the hash is matched.

Can be done online.