## Code 301 Reading Assignment Notes - Class 14

_May 21, 2020_

### Database Normalization

[Database Normalization (Explained in Simple Englist)](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

Database normalization is a process to organize a database into tables and columns. The main idea is that a table should be about a specific topic and only supporting topics included. 

By limiting a table to one purpose you reduce the number of duplicate data contained within your database. 

Three main reasons to normalize a database:

1. Minimize duplicate data
2. Minimize or avoid data modification issues
3. Simplify queries

**Three Common Forms of Database Normalization**

There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. 

The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form.

* [First Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-8-database-first-normal-form-explained-in-simple-english/) – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.

* [Second Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-10-database-second-normal-form-explained-in-simple-english/) – The table is in first normal form and all the columns depend on the table’s primary key.

* [Third Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-11-database-third-normal-form-explained-in-simple-english/) – The table is in second normal form and all of its columns are not transitively dependent on the primary key.


---
[Home page](https://marlene-rinker.github.io/reading-notes/)
