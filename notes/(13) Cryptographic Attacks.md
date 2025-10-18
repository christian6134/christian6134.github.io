
`You've encrypted data and sent it to another person .... is it secure? How do we know?`

*What makes the difference?*
- The attacker does not have the combination (the key)
- So they break the safe (cryptography)
- Finding other means...
- Find ways to `undo the security`



#### Birthday Attack (Hash Collision)
----
`In a classroom of 23 students, what is the chance of 2 students sharing a birthday.`
- About 50%
- For a class of 30, the chance is about 70%

In the digital world, this is a `hash collision`
- Two different plaintexts with the same hash value
- Usually found through brute force
- Generating multiple versions of plaintext to match the hashes
	- Protect yourself with a `large hash output size`


##### Collision
------
- Hash digests are supposed to be unique
	- Different input data should not create the same hash

*Example*
- Collisions in MD5 hash
- Researches created a CA certificate that was NEVER digitally signed by the CA



#### Downgrade Attack
-------
`Instead of using perfectly good encryption, use something that's not so great.
- Force the systems to downgrade their security
- Attack the implementation


**SSL Stripping**
- Combines an on-path and a downgrade attack
- Difficult to implement, big returns
- Attacker must sit in the middle of the conversation
- Victims browser page is not encrypted
- Strips the `S away from HTTPS`

![[SSL-Stripping.png]]