
**Recall: What does Gobuster do?**
- `Enumerates (lists) web directiories, DNS subdomains, Virtual Hosts, Amazon s3 buckets` all by BRUTE force.
- Utilizes specific wordlists and handles incoming responses.
- Resides between `reconnaissance and scanning phases`

**What is enumeration?**
- `The act of listing all the available resources, accessible or not`.
- E.g. Web Directories.

**What is Brute Force?**
- `Act of trying every possibility until a match is found. Having 10 keys and trying them all until the lock unlocks.`
- `Used in the form of Wordlists`

### Gobuster Overview
----------
- Included within Kali Linux.
- `gobuster --help` 
#### Gobuster Help
------
![[Gobuster --help.png]]

| Short Flag | Long Flag    | Description                                                                                                                                                                                                                                                                                                            |
| ---------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-t`       | `--threads`  | This flag configures the number of threads to use for the scan. Each of these threads sends out requests with a slight delay. The default number of threads is 10. This number may be slow when using large wordlists. You can increase or decrease the number of threads depending on the available system resources. |
| `-w`       | `--wordlist` | The flag configures a wordlist to use for iterating. Each wordlist entry is attached to the URL you included in the command.                                                                                                                                                                                           |
|            | `--delay`    | This flag defines the amount of time to wait between sending requests. Some web servers include mechanisms to detect enumeration by looking at how many requests are received in a certain period of time. We can increase the delay between subsequent requests to make it look like normal web traffic.              |
|            | `--debug`    | This flag helps us to troubleshoot when our command gives unexpected errors.                                                                                                                                                                                                                                           |
| `-o`       | `--output`   | This flag writes the enumeration results to a file we choose.                                                                                                                                                                                                                                                          |

### Example
--------------
Let us look at an example of how we would use these commands and flags together to enumerate a web directory:

```
gobuster dir -u "http://www.example.thm/" -w /usr/share/wordlists/dirb/small.txt -t 64
```

- `gobuster dir` indicates that we will use the directory and file enumeration mode.
- `-u "http://www.example.thm/"` tells Gobuster that the target URL is [http://example.thm/](http://example.thm/).
- `-w /usr/share/wordlists/dirb/small.txt` directs Gobuster to use the _small.txt_ wordlist to brute force the web directories. Gobuster will use each entry in the wordlist to form a new URL and send a GET request to that URL. If the first entry of the wordlist were images, Gobuster would send a GET request to [http://example.thm/images/.](http://example.thm/images/)
- `-t 64` sets the number of threads Gobuster will use to 64. This improves the performance drastically.