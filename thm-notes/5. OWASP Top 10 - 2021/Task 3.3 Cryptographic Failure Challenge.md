
##### **Have a look around the web app. The developer has left themselves a note indicating that there is sensitive data in a specific directory.**   
----------------
**What is the name of the mentioned directory?**
- `View the page source on the login page
- There is a comment referencing the database stored within `/assets`
- This is a INSECURE DIRECT OBJECT REFERENCE as the user can view the page from root directory and is not checked for authorization when viewing the page (reference)


**Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data?**  
- `assets.db`



**Use the supporting material to access the sensitive data. What is the password hash of the admin user?**  
- `Open terminal
- `sqlite3 <db_name.db>`
- `.tables`
- `PRAGMA table_info(.table_name)`
- `SELECT * FROM table`
- **Hash:** `6eea9b7ef19179a06954edd0f6c05ceb`



**Crack the hash.**  
**What is the admin's plaintext password?**  
- Using `cracksation`
- **Password**: `qwertyuiop`



**Log in as the admin. What is the flag?**
- Go back to the login page
- Use the credentials from the flat file database
- Login
- **Flag:** `THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}`