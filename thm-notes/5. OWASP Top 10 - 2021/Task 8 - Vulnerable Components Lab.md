
### Prompt
----
**Navigate to [http://10.10.5.248:84](http://10.10.5.248:84/) where you'll find a vulnerable application. All the information you need to exploit it can be found online.** 
- **What is the content of the /opt/flag.txt file?**


### Steps
----
1. go to the victim website
2. notice that they use PHP and MySQL
3. Look up "CSE Bookstore" on ExploitDB
4. Find my SQL injection script
5. Parse for the correct injection site (in this case isbn)
6. run `sqlmap -u "injection_site" `
	1. verify that injection is possible
7. run `sqlmap -u "injection_site" --file-read "file_path"`
8. `cd to file path`
9. Dump contents of flag_txt

**Answer**: 
THM{But_1ts_n0t_my_f4ult!}


### Tools Used
----
`sqlmap`
`ExploitDB`
