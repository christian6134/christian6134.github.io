
**Domain Name Service (DNS)**
--------------
- Operates at the **application** **layer**
- Uses **UDP Traffic by default** or **TCP Port 53 as fallback**

**DNS Records**
- **A RECORD**: Address record maps a **hostname to one or more IPv4 addresses**
- example.com --> 172.17.2.172

**AAAA Record** 
- Similar to A record, but for IPv6

**CNAME** **Record**
- Cannonical Name -> Maps a domain name to another domain name
- www.example.com mapped to example.com or example.org

**MX Record**
- MX (Mail Exchange) record specifies 
- Specifies the mail server responsible for handling emails for a domain


**Looking up the IP address of a Domain from CLI**
- `nslookup` www.example.com


