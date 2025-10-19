
### Some Clarifications:
-------------------

**Hashing**
- Process that takes input data and produces a fixed-size hash value string (digest)
- Unique to the data and any changes will reflect significant changes to the hash (integrity)
- Hashing is **one-way** and cannot be reversed to get the original data


**Encoding**
- Converts data from one form to another to make it compatible with a specific system.
- Example: UTF-8, UTF-16 are valid encoding methods for English Language
- Reversible and anyone can change the data encoding with tools


**Encryption**
- Protects confidentiality using  a cipher and a key
- Encryption is reversible provided the cipher and key access



**Exercise**
(1) Use `base64` to decode `RU5jb2RlREVjb2RlCg==`, saved as `decode-this.txt` in `~/Hashing-Basics/Task-8`. What is the original word?****
- `base64 -d decode-this.txt`
- **Answer: ENcodeDEcode**
