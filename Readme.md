<!-- Problem 1 Answer -->
What is PostgreSQL?
- Answer: PostgreSQL is an advanced, powerful, open-source relational database management system that uses Structured Query Language. It is known for its reliability, support for custom data types, robust data storage and management, and ability to handle complex queries, advanced analytics, functions, triggers, and views. As an open-source solution, it offers significant cost savings compared to other databases. PostgreSQL provides comprehensive tools for data manipulation and analysis, including support for window functions, common table expressions, and advanced aggregations, enabling users to perform complex analyses efficiently.

<!-- Problem 3 Answer -->
Explain the Primary Key and Foreign Key concepts in PostgreSQL.
- Answer:  A Primary Key in PostgreSQL is a column or a set of columns that uniquely identifies each row in a table. It ensures that no duplicate or NULL values exist in the primary key column(s). Each table can have only one primary key.
A Foreign Key is a column or a set of columns in one table that refers to the primary key of another table. It is used to establish and enforce a link between the data in the two tables, maintaining referential integrity by ensuring that the value in the foreign key column matches a value in the referenced primary key column.
Example:
    -- Primary Key in rangers table
    ranger_id SERIAL PRIMARY KEY
    -- Foreign Key in sightings table
    ranger_id INT REFERENCES rangers(ranger_id)


<!-- Problem 4 Answer -->
What is the difference between the VARCHAR and CHAR data types?
- Answer:  The CHAR data type is a fixed-length character type. When in database a column define as CHAR(n), it always stores exactly 'n' characters, padding with spaces if the input is shorter.  
The VARCHAR data type is a variable-length character type. When in database a column define as VARCHAR(n), it can store up to 'n' characters, using only as much space as needed for the actual data.  

<!-- Problem 5 Answer -->
Explain the purpose of the WHERE clause in a SELECT statement.
- Answer: The WHERE clause in a SELECT statement is used to filter records and return only those rows that meet specific conditions. It allows to specify criteria that each row must satisfy to be included in the query results, making data retrieval more precise and efficient.
Example:
    SELECT * FROM sightings WHERE location ILIKE '%Pass%';


<!-- Problem 10 Answer -->
How can you calculate aggregate functions like COUNT(), SUM(), and AVG() in PostgreSQL?
- Answer: In PostgreSQL, we can calculate aggregate functions like COUNT(), SUM(), and AVG() by using them in a SELECT statement. These functions operate on a set of rows and return a single value. For example:

    1) COUNT(*) returns the number of rows in a table.
    2) SUM(column_name) returns the total sum of values in a numeric column.
    3) AVG(column_name) returns the average value of a numeric column.

Example usage:
    SELECT COUNT(*) FROM employees;
    SELECT SUM(salary) FROM employees;
    SELECT AVG(age) FROM employees;
