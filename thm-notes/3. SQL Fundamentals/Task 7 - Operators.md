- **LIKE**
    
    - Filters text by pattern
        
    - Wildcards: `%` (any sequence), `_` (single character)
        
- **AND / OR / NOT**
    
    - `AND`: all conditions true
        
    - `OR`: at least one true
        
    - `NOT`: negates a condition
        
- **BETWEEN**
    
    - Tests if a value lies within an inclusive range
        
- **Comparison Operators**
    
    - `=` (equal)
        
    - `!=` (not equal)
        
    - `<` (less than)
        
    - `>` (greater than)
        
    - `<=` (less than or equal)
        
    - `>=` (greater than or equal)


## Exercises
------
`show DATABASES;`
`USE tools_db;`
`SHOW tables;`


**Using the `tools_db` database, which tool falls under the Multi-tool category and is useful for pentesters and geeks?**  
- `SELECT category FROM tools_db WHERE category="Multi-tool" AND description LIKE "pentesters"`
	- Flipper ZERO



**Using the `tools_db` database, what is the category of tools with an amount greater than or equal to 300?**  
- `SELECT category FROM tools_db WHERE amount >= 300;`
	- RFID Cloning



**Using the `tools_db` database, which tool falls under the Network intelligence category with an amount less than 100?**
- `SELECT * FROM tools_db WHERE category="Network intelligence" AND amount < 100;`