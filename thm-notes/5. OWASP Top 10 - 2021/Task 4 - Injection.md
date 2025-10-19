
### What is Injection?
-------
Injection flaws are very **common** even today.

**How Do they Occur?**
- Application interprets user-controlled input as commands or parameters
- Injection attacks depend on what technologies are used and how they are used to **interpret input**

**Some Examples**:
- **SQL Injection**: Occurs when user-controlled input is `passed to SQL as a query`. 
- An attacker can pass in SQL queries to manipulate the outcome of such queries.
- Attacker could `modify, access, delete information` within a database (If the input of the user is passed to the database queries)
- Attack could steal sensitive information

- **Command Injections**: Occurs when user input is passed to system commands.
- Attacker can execute arbitrary system commands on application servers
- Allowing access to user' systems


### How do we Defend from this?
----------
Ensure that user controlled input is **NOT interpreted as Database Queries or System Commands**
- **Using an allow list**: 
	- When input is sent to the server:
	- Input is compared to a [list of safe inputs or characters] 
	- Input is marked [safe]?
	- It is processed -> Rejected if not and application will throw (error)

- **Stripping Input (Sanitization)**
	- If input contains dangerous characters, these are removed before processing

#### What is considered dangerous input?
-----
Input that can change how the underlying data is processed
- As opposed to manually constructing allow lists
- Libraries exist to perform these actions for you.