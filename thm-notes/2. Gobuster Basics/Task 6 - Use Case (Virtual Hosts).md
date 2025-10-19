
### VHOST Mode
----------
`This mode allows gobuster to brute force virtual hosts.`

**What are virtual hosts?**
- `Different websites on the same machine`
- `May look like subdomains`

**Virtual Host v DNS**
- `Vhosts are IP-based and run on the same server`
- `Subdomains are set up in DNS`

**Scans**
- `Vhost navigates to the URl created by combining the host name with an entry of a wordlist (-u)`
- `DNS mode will do a DNS look up to the FQDN created by combinining configured domain name with an entry of a wordlist (-d)`


### VHOST Help
------
![[VHOST-help.png]]


### How to Use
---------
`gobuster vhost -u "http://example.thm" -w /path/to/wordlist`

`gobuster vhost -u "http://10.10.152.206" --domain example.thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt --append-domain --exclude-length 250-320`



### Exercise
-------
`gobuster vhost -u "http://10.10.152.206" --domain offensivetools.thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt --append-domain --exclude-length 250-350

**How many VHOSTS are returned with a 200 Status Code**
- 4