### What is Dir Mode?
- `dir` mode allows users to `enumerate website directories and files`

**When is this useful?**
- When performing pen testing
- When you need to see the directory structure of a website and what files they contain
- Most website directories `follow a specific convention`

**Example: WordPress Directory**
```shell-session
root@tryhackme:~# tree -L 3 -d
.
└── html
    └── wordpress
        ├── wp-admin
        ├── wp-content
        └── wp-includes
```

Gobuster allows scans of websites and `returns status codes`

**Why are status codes useful in this case?**
- `Status codes tell you immediately if you as an outside user can request that directory or not.`


### `gobuster dir --help`

| Flag | Long Flag                  | Description                                                                                                                                                                                                                   |
| ---- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-c` | `--cookies`                | This flag configures a cookie to pass along each request, such as a session ID.                                                                                                                                               |
| `-x` | `--extensions`             | This flag specifies which file extensions you want to scan for. E.g., .php, .js                                                                                                                                               |
| `-H` | `--headers`                | This flag configures an entire header to pass along with each request.                                                                                                                                                        |
| `-k` | `--no-tls-validation`      | This flag  skips the process that checks the certificate when https is used. It often happens for CTF events or test rooms like the ones on THM a self-signed certificate is used. This causes an error during the TLS check. |
| `-n` | `--no-status`              | You can set this flag when you don’t want to see status codes of each response received. This helps keep the output on the screen clear.                                                                                      |
| `-P` | `password`                 | You can set this flag together with the --username flag to execute authenticated requests. This is handy when you have obtained credentials from a user.                                                                      |
| `-s` | `--status-codes`           | With this flag, you can configure which status codes of the received responses you want to display, such as 200, or a range like 300-400.                                                                                     |
| `-b` | `--status-codes-blacklist` | This flag allows you to configure which status codes of the received responses you don’t want to display. Configuring this flag overrides the -s flag.                                                                        |
| `-U` | `--username`               | You can set this flag together with the `--password` flag to execute authenticated requests. This is handy when you have obtained credentials from a user.                                                                    |
| `-r` | `--followredirect`         | This flags configures Gobuster to follow the redirect that it received as a response to the sent request. A HTTP redirect status code (e.g., 301 or 302) is used to redirect the client to a different URL.                   |


### How to use `dir` mode
------
**Recall:** 
- ````gobuster dir -u "http://www.example.thm" -w /path/to/wordlist

#### Example
Let us look at a practical example of how to enumerate directories and files with Gobuster `dir` mode:

```
gobuster dir -u "http://www.example.thm" -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -r
```

  
This command scans all the directories located at _www.example.thm_ using the wordlist _directory-list-2.3-medium.txt_. Let’s look a bit closer at each part of the command:

- `gobuster dir`: Configures Gobuster to use the directory and file enumeration mode.
- `-u http://www.example.thm`:

- The URL will be the base path where Gobuster starts looking. So, the URL  above is using the root web directory. For example, in a typical Apache installation on Linux, this is `/var/www/html`. So if you have a “resources” directory and you want to enumerate that directory, you’d set the URL as `http://www.example.thm/resources`. You can also think of this like `http://www.example.thm/path/to/folder`.
- The URL must contain the protocol used, in this case, HTTP. This is important and required. If you pass the wrong protocol, the scan will fail.
- In the host part of the URL, you can either fill in the IP or the HOSTNAME. However, it is important to mention that when using the IP, you may target a different website than intended. A web server can host multiple websites using one IP (this technique is also called virtual hosting). Use the HOSTNAME if you want to be sure.
- Gobuster does not enumerate recursively. So, if the results show a directory path you are interested in, you will have to enumerate that specific directory.

- `-w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt` configures Gobuster to use the _directory-list-2.3-medium.txt_ wordlist to enumerate. Each entry of the wordlist is appended to the configured URL.
- `-r` configures Gobuster to follow the redirect responses received from the sent requests. If a status code 301 was received, Gobuster will navigate to the redirect URL that is included in the response.  
    

Let’s look at a second example where we use the `-x` flag to specify what type of files we want to enumerate:

```
gobuster dir -u "http://www.example.thm" -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x .php,.js
```


### Exercises
---------
(1) *Which flag do we have to add to our command to skip the TLS verification?*
- **-k or --no-tls-validation**

(2) *Enumerate the directories of www.offensivetools.thm. Which directory catch your attention?*
- `gobuster dir -u "www.offensivetools.thm" -w /usr/share/wordlists/dirbuster/directory...txt`

- **Answer:** `Secret`


(3) Continue enumerating the directory found in question 2. You will find an interesting file there with a .js extension. What is the flag found in this file?
- `gobuster dir -u "www.offensivetools.thm/secret/ -w /...txt -x .js`
- returned 301 FOR /CONTENT

What does this mean?
- `we must invoke -r to follow the redirect`
- `eventually we can see flag.js with a 200 return code meaning it can be retrieved
- **Answer** `wget "MACHINE_IP/secret/content/flag.js"`
- cat flag.js
- FLAG = `THM{ReconSuccess}`
