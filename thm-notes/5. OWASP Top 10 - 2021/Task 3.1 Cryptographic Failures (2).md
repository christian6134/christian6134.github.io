
**How do we store large amounts of data?**
- Format data to be easily accessible from any locations within a DATABASE
- Database engines usually follow the **Structured Query Language (SQL) Syntax**

Databases can be setup on dedicated servers using services such as :
- MySQL
- MariaDB

Databases can also be stored as files
- Referred to as `flat-file` databases
- Stored as a single file on a computer
- 
### Focus: Accessing a FLAT-FILE Database (Not a server)

------

#### Flat-File DBs and the RISK
----
These are typically not a problem especially for smaller web servers (applications)
- However, the problem arises if the FLAT-FILE DB is stored within the root of the web application
- This means a user can access the Flat-File DB directly from the web application (root directory)
- We will download and query it on our own machine, full access to the database


### Syntax to Query a Flat-File DB
-------
Most Common Format -> SQLite Database
Dedicated client for querying on the CLI
- `sqlite 3`

**Let's suppose we have successfully managed to download a database:**

Linux

```shell-session
user@linux$ ls -l 
-rw-r--r-- 1 user user 8192 Feb  2 20:33 example.db
                                                                                                                                                              
user@linux$ file example.db 
example.db: SQLite 3.x database, last written using SQLite version 3039002, file counter 1, database pages 2, cookie 0x1, schema 4, UTF-8, version-valid-for 1
```

**We can see that there is an SQLite database in the current folder.**

To access it, we use `sqlite3 <database-name>`:

Linux

```shell-session
user@linux$ sqlite3 example.db                     
SQLite version 3.39.2 2022-07-21 15:24:47
Enter ".help" for usage hints.
sqlite> 
```

**From here, we can see the tables in the database by using the `.tables` command:**

Linux

```shell-session
user@linux$ sqlite3 example.db                     
SQLite version 3.39.2 2022-07-21 15:24:47
Enter ".help" for usage hints.
sqlite> .tables
customers
```

At this point, we can dump all the data from the table, but we won't necessarily know what each column means unless we look at the table information. First, let's use `PRAGMA table_info(customers);` to see the table information. Then we'll use `SELECT * FROM customers;` to dump the information from the table:

Linux

```shell-session
sqlite> PRAGMA table_info(customers);
0|cudtID|INT|1||1
1|custName|TEXT|1||0
2|creditCard|TEXT|0||0
3|password|TEXT|1||0

sqlite> SELECT * FROM customers;
0|Joy Paulson|4916 9012 2231 7905|5f4dcc3b5aa765d61d8327deb882cf99
1|John Walters|4671 5376 3366 8125|fef08f333cc53594c8097eba1f35726a
2|Lena Abdul|4353 4722 6349 6685|b55ab2470f160c331a99b8d8a1946b19
3|Andrew Miller|4059 8824 0198 5596|bc7b657bd56e4386e3397ca86e378f70
4|Keith Wayman|4972 1604 3381 8885|12e7a36c0710571b3d827992f4cfe679
5|Annett Scholz|5400 1617 6508 1166|e2795fc96af3f4d6288906a90a52a47f
```

We can see from the table information that there are four columns: `custID`, `custName`, `creditCard` and `password`. You may notice that this matches up with the results. Take the first row:

`0|Joy Paulson|4916 9012 2231 7905|5f4dcc3b5aa765d61d8327deb882cf99   `   

We have the custID (0), the custName (Joy Paulson), the creditCard (4916 9012 2231 7905) and a password hash (5f4dcc3b5aa765d61d8327deb882cf99).

**In the next task, we'll look at cracking this hash.**
