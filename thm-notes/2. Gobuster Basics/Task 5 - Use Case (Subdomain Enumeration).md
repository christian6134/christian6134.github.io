
### Focus
------
Next mode will be focusing on `DNS` mode.

`What does DNS mode do?`
- Allows gobuster to brute force subdomains.

`Why is subdomain enumeration important?`
- Patching in a regular domain does not guarantee it is patched in a subdomain
- We may be able to exploit these vulnerabilities by scanning various subdomains.


### `gobuster dns --help`
--------
![[gobuster-dns-help.png]]


### How to use
---------
Example:
- `gobuster dns -d example.thm -w /path/to/wordlist`
