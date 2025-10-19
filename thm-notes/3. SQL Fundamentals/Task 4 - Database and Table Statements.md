

### Database Statement
----
- **Creating a Database**
	- `CREATE DATABASE database_name;`

- **Showing Databases**
	- `SHOW DATABASES;`

- **Using a Database**
	- `USE DATABASE;`

- **Dropping a Database**
	- `DROP databse database_name;`


### Table Statements
----
- **Creating a Table**
	- `CREATE TABLE example_table_name (
		- `example_col1 data_type,
		- `example_col2 data_type`
		- `example_col3 data_type`
		- `example_col4 data_type`
		`);`


`mysql> CREATE TABLE book_inventory (
    **`book_id INT AUTO_INCREMENT PRIMARY KEY,`**
    **`book_name VARCHAR(255) NOT NULL,`**
    **`publication_date DATE`**
`);`

- ***book_id** (`INT`, `AUTO_INCREMENT`, `PRIMARY KEY`):*
    
    - *Integer-only*
        
    - *Automatically increments (1, 2, 3, …)*
        
    - *Uniquely identifies each book*
        
- ***book_name** (`VARCHAR(255)`, `NOT NULL`):*
    
    - *Variable-length text (up to 255 characters)*
        
    - *Cannot be empty*
        
- ***publication_date** (`DATE`):*
    
    - *Stores calendar date (`YYYY-MM-DD` format)*

- **Describing a Table**
	- Show what columns are contained within a table (and their datatype)
	- use `DESCRIBE table_name;`
	- Returns a **detailed** view of the table

- **Altering a Table**
	- Dataset changes
	- `ALTER TABLE book_inventory
	- `ADD page_count INT;
Added a new row to the table

- **Dropping a Table**
	- `DROP TABLE table_name;`

