
**Functions:**
- Help streamline queries and operations and manipulate data.

**String Functions:**
- String functions perform operations on a string, returning a value associated with it.


### CONCAT() Function
------------
Used to add two or more strings together, useful to **combine text from different columns.**
- **Example:**
	- `SELECT CONCAT(name, " is a type of ", category "book.") AS book_info FROM books;`
- Concatenates the name and category columns from the books table into a single one named book_info.



### GROUP_CONCAT() Function
----
Concatenate data from multiple rows in one field.
- **Example:**
	- `SELECT from category, GROUP_CONCAT(name SEPARATOR ", ") AS books 
	- 'FROM books
	- 'GROUP BY category;`
- Groups books by category and concatenates titles of books within each category into a single string.


### SUBSTRING() Function
---------
Retrieve a substring from a string within a query, starting at a **determined position**.
Length of substring can be **specified**.
- **Example:**
	- `SELECT SUBSTRING(published_date, 1, 4) AS published_year FROM books;`
- Extracts the first four characters from the published_date column and stores them in the published_year column.


#### LENGTH() Function
----------
Returns the number of characters in a string. Includes **space and puncuation**.
- **Example:**
	- `SELECT LENGTH(name) AS name_length FROM books;`
- Calculates the length of the string within the name column and stores it in a new column named name_length.


## Aggregate Functions
---


### COUNT() Function
-----------
Returns the number of records within an expression.
- **Example**:
	- `SELECT COUNT(*) AS total_books FROM books;
- Counts the number of rows in the books table, the result is 5, as there are 5 books and its stored in the total_books column.


### SUM() Function
-----
This function sums all values (not NULL) of a determined column.
- `SELECT SUM(price) AS total_price FROM books;`



### MAX() Function
-----
This function calculates the maximum value within a provided column in an expression.
- `SELECT MAX(published_date) AS latest_book FROM books;`



### MIN() Function
---
This function calculates the minimum value within a provided column in an expression.
- `SELECT MIN(price) AS cheapest_book FROM books;`




### Exercises
-----
**Using the `tools_db` database, what is the tool with the longest name based on character length?**  
- `SELECT * from hacking_tools ORDER BY LENGTH(name) DESC;`
- USB Rubber Ducky



**Using the `tools_db` database, what is the total sum of all tools?**  
- `SELECT SUM(amount) AS total_tools FROM hacking_tools;`
- 1444



**Using the `tools_db` database, what are the tool names where the amount does not end in 0, and group the tool names concatenated by " & ".**
- `SELECT GROUP_CONCAT(name SEPARATOR "&") FROM hacking_tools WHERE SUBSTRING(-1, 1)!=0;`