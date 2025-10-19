
### **John Basic Syntax**
-------
`john [options] [file path]`


**Automatic Cracking**
- Built in features to detect what type of hash it is being given and select appropriate rules and formats to follow
- Can be **unreliable**

`john --wordlist={path to word list} {path to  file hash}`
`john --wordlist=/usr/share/wordlists/rockyou hash_to_crack.txt`


**Some tools to identify hashes**
- Hashes.com
- Hash-Identifier (on GitHub) - Python Tool
- `wget / curl hash-id.py`


**Format-Specific Cracking**
- Once Hash identified, you can tell John to use it while cracking the provided hash using the following syntax

- `john --format=[format] --wordlist=[path to wordlist] [path to file]

- `john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash_to_crack.txt`

- **Note**: When dealing with a standard hash (e.g. md5), you must prefix it with `raw-` to tell John you're dealing with a **standard hash type.**

- To check if prefixes are needed, use `john --list=formats` or `john --list=formats | grep -iF "md5"`


**Exercise**
---------------
What type of hash is hash1.txt?
- run `hash-id.py <hash>`
- Returned **MD5**
Cracked value of hash1.txt?
- **biscuit**

Type Hash2.txt?
- run `hash-id.py <1A732667F3917C0F4AA98BB13011B9090C6F8065>`
- Returned SHA-1 --> Raw-SHA1-AxCrypt
Cracked value of Hash2.txt?
- **kangeroo**


Type Hash3.txt?
- run hash-id.py {hash}
- return **SHA-256**
- john --format=Raw-SHA256 --wordlist=... hash3.txt
Cracked value of hash3.txt
- **microphone**


Type Hash4.txt?
- SHA-512 / **Whirlpool**
Cracked value of Hash4.txt?
- colossal














