
### What Is a Database?

- An organized collection of structured information (data)
    
- Easily accessible, manipulable, and analyzable
    
- Stores everything from user credentials to social-media posts and streaming-service histories
    

---

### Main Database Types

- **Relational (SQL)**
    
    - Structured: data fits predefined tables with rows & columns
        
    - Enforces schemas and data types
        
    - Ideal when input format is consistent (e.g., e-commerce transactions)
        
- **Non-Relational (NoSQL)**
    
    - Flexible, schema-less formats (key-value, document, column-family, graph)
        
    - Handles varying or unstructured data (e.g., user-generated content)
        
    - Scales horizontally for large, heterogeneous datasets
        

---

### Core Components of a Relational Database

- **Tables**: named collections of related records (e.g., `Books`)
    
- **Columns**: defined fields in each table, with specific data types (STRING, INTEGER, DATE, etc.)
    
- **Rows**: individual records in a table (one book per row)
    

---

### Keys & Relationships

- **Primary Key (PK)**
    
    - Uniquely identifies each record in its table
        
    - Example: `book_id` in the `Books` table
        
- **Foreign Key (FK)**
    
    - A column that references a PK in another table
        
    - Creates a link between tables (e.g., `author_id` in `Books` → `id` in `Authors`)
        

---

### Review Questions

|Question|Answer|
|---|---|
|What type of database should you consider if the data will **vary greatly** in its format?|Non-relational database|
|What type of database should you consider if the data will **reliably** be in the same structured format?|Relational database|
|In our example, once a record of a book is inserted into our “Books” table, it would be represented as a ___ in that table?|Row|
|Which type of key provides a link from one table to another?|Foreign key|
|Which type of key ensures a record is unique within a table?|Primary key|