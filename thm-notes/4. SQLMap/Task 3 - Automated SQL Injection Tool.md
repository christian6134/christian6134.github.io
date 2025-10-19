
### SQLMap
------
**Define:**
- `SQLMap is a free and open-source penetration testing tool that automates finding and exploiting SQL injection vulnerabilities on web applications. It can extract data from databases, execute commands on the underlying operating system, and even take control of the target server.`

*What is SQL Map?*
- `CLI tool, open with `sqlmap --help
- Use `--wizard` flag to have the tool guide you through each step and ask questions to complete the scan

`DBS Flag`
- `--dbs`
- Extracts all database names
- `-D database_name -- tables` to extract information about the tables within the DB


**EXERCISE**
- `What would be the full command of SQLMap for extracting all tables from the "members" database? (Vulnerable URL: http://sqlmaptesting.thm/search/cat=1)`

`sqlmap -u http://sqlmaptesting.thm/search/cat=1 -D members --tables`