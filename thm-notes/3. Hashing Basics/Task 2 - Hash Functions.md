
**Hash Functions** are different that Encryption.
- There is **no key**
- Impossible to go from the output back to the input

**Procedure**
<> Takes input data of any size
<> Creates summary or **digest** of the data
<> Output has a fixed size
<> Hard to predict output for any input and vice versa


**Good Hashing Functions**
- Relatively fast to compute
- Slow to reverse (Go from output and determine the input)
- Any slight change in the input data results in a significant change in the output

![[Pasted image 20250702123642.png]]

*Note*:
- Very similar input in terms of hex and binary values
- However, hashes differ by a significant amount
- Outputs of hash functions are raw bytes --> Encoded by (`md5sum, sha1sum, sha256sum, sha512sum`)
-  Hexadecimal format prints each raw byte as two hex digits


**Why Hashing?**
-----------------------------
- Invisible to the user
- Protects data's integrity and ensure password confidentiality
------------------------------------------

**Hash Collisions**
------------------------------
*Define*:  When **two different inputs** result in the **same output**

Note: Hash functions are designed to avoid collisions as best as possible
- Designed to prevent an attacker from being able to create a collision
- Inputs are unlimited, Outputs are finite -> **Pigeonhole** **effect**

**Recall:**
The **pigeonhole effect** states that the number of items (_pigeons_) is more than the number of containers (_pigeonholes_); some containers must hold more than one item. In other words, in this context, there are a fixed number of different output values for the hash function, but you can give it any size input. As there are more inputs than outputs, some inputs must inevitably give the same output. If you have 21 pigeons and 16 pigeonholes, some of the pigeons are going to share the pigeonholes. Consequently, collisions are unavoidable. However, a good hash function ensures that the probability of a collision is negligible.


**Questions**
-------------------
What is the SHA256 hash of the `passport.jpg` file in `~/Hashing-Basics/Task-2`?
- `sha256sum passport.jpg`


If you have an 8-bit hash output, how many possible hash values are there?
- 2^8 = 256 hash values




