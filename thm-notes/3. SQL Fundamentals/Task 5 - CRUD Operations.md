
### CRUD
----------
**Basic Operations** in any system that manages data. (Databases)
- Create
- Read
- Update
- Delete

#### Create (INSERT)
---------------
Use `INSERT INTO`
- Example:
	`INSERT INTO books (id, name, published_date, description) VALUES (1, "Android Security Internals", "2014-10-14", "An In-Depth Guide to Android's Security");`
- Inserting into the `books table`, the columns are the records within the table starting with Primary Key (1).


#### Read (SELECT)
----------
Use `SELECT`
- Example: 
	`SELECT * FROM books;`
	`*` Indicates that all columns should be retrieved `FROM` table_name

	`SELECT name, description FROM books;`
	Will retrieve `name and description` rows from the table.



#### UPDATE (UPDATE)
--------
Use `UPDATE`
- Example:
  `UPDATE books SET description = "An In-Depth Guide to Android's Security Architecture" WHERE id=1;

	`UPDATE` specifies the table name `books` and we can use `SET` followed by the `column name` we will update.
		`WHERE` specifies which row to update, in this case one with the ID = 1


#### DELETE (DELETE)
----
`DELETE FROM books WHERE id=1;`



## Exercises
----
Using the `tools_db` database, what is the name of the tool in the `hacking_tools` table that can be used to perform man-in-the-middle attacks on wireless networks?  
- `USE tools_db;`
- `DESCRIBE hacking_tools;
- `SELECT name, description FROM hacking_tools;`
	- `Wi-Fi Pineapple`



Using the `tools_db` database, what is the shared category for both **USB Rubber Ducky** and **Bash Bunny**?
- `SELECT name, category from hacking_tools;`
	- USB Attacks