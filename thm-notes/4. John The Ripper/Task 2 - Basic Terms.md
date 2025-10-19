
### Hashes Cont.
--------------
Define: Taking a piece of data of **any length** and representing it in another **fixed**-length form.
- Process **masks the** original value of the data
- **Hash Value** is obtained through running original data through the **hashing algorithm / hashing function**
- Some popular hashing algorithms
	- MD4
	- MD5
	- SHA1
	- NTLM

**Example:**
Take the string "polo" and run it through an **MD5** hashing algorithm. It results with an output of `b53759f3ce692de7aff1b5779d3964da` which is a standard 32-character MD5 HASH.

Take the string "polomints" which contains 9 characters and run it through the same MD5 hashing algorithm ---> End up with another output of 32-character standard MD5
`584b6e4f4586e136bc280f27f9c64f3b`


---------

### Why is Hashing so Secure?
--------
* Designed as a **one-way** function.
* Easy to calculate hash value of a given input
* **Infeasible** to compute the original input given the hash value.
* Computational problem has its roots in mathematics as **P v NP**


- **P (Polynomial Time)**: 
	- Covers the problems whose solution can be found in **polynomial time**
	- Example: Sorting a list in increasing order
	- Longer the list --> Longer it takes for time to sort.
	- Increase in time ie **not exponential.**

- **NP (Non-deterministic Polynomial Time)**
	- Covers a given solution that can be checked quickly, even though the solution itself may be **hard to find**
	- We don't know if there is a fast algorithm to find the solution in the first place


**Putting it together** (Abstractly):
- The algorithm to hash will be the value "P" and can therefore be calculated reasonably
- An "un-hashing" algorithm would be "NP" and intractable to solve --> It cannot be computed in a reasonable time using standard computers


------------





### Where John Comes in
----------------
The hashing algorithm is not reversible, however that does not mean cracking the hashes is impossible.
- If you have the hashed version of a password and you know the hashing algorithm, you can use that hashing algorithm to hash a large number of word ---> **Dictionary**
- Then, compare these hashes to the one you are trying to crack and see if they match.

This is called a **dictionary attack**, and **John the Ripper** is a tool for conducting **fast brute force attacks** on various hash types. 

- "Jumbo John"


