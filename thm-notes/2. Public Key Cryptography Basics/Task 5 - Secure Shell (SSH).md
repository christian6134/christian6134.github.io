
**Authenticating the Server**
`ssh 10.10.244.173`
- SSH client confirms whether we recognize the server's public key fingerprint
- ED25519 is the public-key algorithm used for digital signature generation and verification 
- Mitigates Man in the Middle Attacks

Add Public Key Signature -> Now can connect silently unless the host replies with a different public key


**Authenticating the Client**
Now we have confirmed we are talking with the correct server.

Key Authentication: Uses public and private keys to prove the client is a valid and authorized user on the server
- By Default SSH keys are RSA Keys

`ssh-keygen` is used to generate key pairs


**SSH Private Keys**
*Note*: Passphrase used to decrypt the private key doesn't identify you to the server, it only decrypts the SSH private key.
- Passphrase is never transmitted and never leaves your system

Only the owner should be able to read / write the private key 
`ssh -i privateKeyFileName user@host`
- Specify a key for the standard Linux OpenSSH Client


`~/.ssh` - Default place to store keys for OpenSSH
`authorized_keys` directory holds public keys that are allowed access to the server if key authentication is enabled


**Exercise**
----------------
Check the SSH Private Key in `~/Public-Crypto-Basics/Task-5`. What algorithm does the key use?
- rsa




