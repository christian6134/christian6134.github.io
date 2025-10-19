This room taught us about the offensive tool Gobuster. This tool enumerates directories, files, DNS subdomains, and virtual hosts.

We have covered three different modes of the Gobuster tool:

- `dns` mode: enumerates dns subdomains.
- `dir` mode: enumerates directories.
- `vhost` mode: enumerates virtual hosts.

For each mode, we covered the required flags to configure and additional optional flags that fine-tune the desired results.

We have highlighted the difference between virtual hosts and subdomains and the way Gobuster scans for these:

- `dns` mode uses the DNS services to scan for subdomains using the configured domain and wordlist.
- `vhost` mode sends web requests using the configured URL and wordlist.

At the end of each task, we directly applied the skills we had learned through hands-on exercises.