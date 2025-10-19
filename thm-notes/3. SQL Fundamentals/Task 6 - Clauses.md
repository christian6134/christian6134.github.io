
### What is a Clause?
-------------
A part of a statement that specifies the criteria of the data being manipulated.
Help define the type of data and how it should be retrieved and sorted.

`FROM` and `WHERE` are examples of clauses from previous tasks.

Now,

`DISTINCT, GROUP BY, ORDER BY, HAVING
`


#### DISTINCT CLAUSE
-----------
Used to avoid duplicate records when doing a query, returns only **unique values**.
**Example:**
- `SELECT * from books;`
- `SELECT DISTINCT name FROM books;`
	- This will return the name columns present in the table that are (UNIQUE) no duplicates.


#### GROUP BY CLAUSE
------
Aggregates data from multiple records and groups the query results in columns.
**Example:**
- `SELECT name, COUNT(*) FROM books GROUP BY name;`
	- Records on the book table are grouped by the result of COUNT function, in this case ETHICAL_HACKING has 2 instances thus it is reflected.


### ORDER BY Clause
-----------------
Used to sort records returned by a query in ascending or descending order using **ASC and DESC**.
`SELECT * FROM books ORDER BY published_date ASC;`
`SELECT * FROM books ORDER BY published_date DESC;`


### HAVING Clause
------------------------
Filter groups and results of records based on a condition
`SELECT name, COUNT(*)
	`FROM books
	`GROUP BY name
	`HAVING name LIKE '...'`
	`
Returns books with the names that contain the word hack and the proper count.


## Exercises
-------
**Using the `tools_db` database, what is the total number of distinct categories in the `hacking_tools` table?**  
- `SELECT DISTINCT category FROM hacking_tools`
	- Returned 6



**Using the `tools_db` database, what is the first tool (by name) in ascending order from the `hacking_tools` table?**  
- `SELECT name FROM hacking_tools ORDER by name ASC;`
	- First returned -> Bash Buddy



**Using the `tools_db` database, what is the first tool (by name) in descending order from the `hacking_tools` table?**
- ``SELECT name FROM hacking_tools ORDER by name DESC;``
	- First Returned -> Wi-Fi Pineapple
