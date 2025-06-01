## What is Database Management System(DBMS)?
It is a software that is used to manage and organize databases. Example includes MySQL, PostgresSQL, Oracle, and SQL Server.

advantages of dbms:
- fast rate of data retrieval
- automatic backup & recovery mechanism
- allows concurrent access(multiple user can access db without conflict)
- data integrity: ensures data is consistent and accurate
- reduced redundancy: avoid data duplication by enforcing normalization

## What is the difference between DBMS and RDBMS?
### DBMS (Database Management System)
A system that allows the user to perform crud operation like create, store, modify, delete etc. It does not require a relational structure for data organization e.g: XML databases.
### RDBMS (Relational Database Management System)
A subset of dbms that stores the data in a structured format using tables(relations), and supports the relational operations like `joins`.

## What is a relation in DBMS?
A `relation` in dbms is a table that consist of rows and columns. Rows represent the record while column represents the features/attributes or property of the entity being described. `Schema` is used to define the relations.

## What is a primary key? Explain with an example.
Primary key is the unique identifier for each record in the table. It can not be null. 

For example in the `student` table the `roll_number` could be the primary key as all students have unique roll numbers.

## What is a foreign key? Explain with an example.
Foreign key is an attribute in a table that links to the primary key of another table. It establishes a relationship between 2 tables allowing to link data between them. 

For example in the `order` table the `customer_id` can be the foreign key that references the `customer_id` primary key in the `customer` table.

##  What is a candidate key in DBMS?
A candidate key is the set of one or more attributes that can be uniquely identify a tuple in a relation(table). A relation(table) can have a multiple candidate keys, and one of them is chosen as the primary key.


## What is normalization? Why it is important in DBMS?
It is the process of organizing data in such a way that there should be reduced dependency and redundancy.
### Normalization Goals
- eliminates redundancy : avoid storing duplicate data 
- improve data integrity: ensure data consistent and accurate
- reduce data anomalies : prevent inconsistencies when performing CRUD operations
### Normalization Rules
- 1NF: Each table and cell contains a single value.
- 2NF: All non-key attributes depends entirely upon the primary key.
- 3NF: If a table is in 2NF and a non-key attribute depends upon another non-key attribute than it should be moved to a separate table.

## What is a view in DBMS? How does it differ from a table?
View is a virtual table created by querying one or more base tables. It does not stores data instead retrieves it dynamically. Unlike table, view does not store its own data but presents data from other tables.

## What are the different types of relationships in DBMS?
There are 3 main types of relationships in DBMS. 
### One-to-One (1:1) Relationship
A record(row) in one table is associated with a single record in another table. 
<br> For example a `person` has only one `passport` and similarly a passport is assigned to only one person.
### One-to-Many (1:N) Relationship
A record in one table is associated with multiple records in another tables. <br>
For example a `customer` can place multiple `orders`, but each order is associated with only one customer.
### Many-to-Many (M:N) Relationship
Multiple records in one table are associated with multiple records in another table.<br>
For example a `student` can enroll in multiple courses, and a `course` can have multiple students.

## What is the difference between DELETE and TRUNCATE in SQL?
### DELETE
- deletes specific row or all rows from a table depends upon the condition.
- logs each row deletion, making it a slower operation.
- can be rolled back if it is a part of transaction. 
### TRUNCATE
- removes all the rows from the table without logging individual row deletion.
- faster than deletes (because it does not log each row deletion).
- can not be rolled back.

## What is a join in SQL? Name and explain different types of joins.
### Join
A join in sql is used to combine rows from two or more tables based on the related column between them. <br>
There are 6 different types of joins.
1. ### Inner Join
- Returns only the matching rows form both tables.<br>
`SELECT *
FROM employees e`<br>
`INNER JOIN departments d ON e.department_id = d.id;`

2. ### Left Join (Left Outer Join)
- Returns all rows from the left table and matching rows from right table.
- No match return null from right side <br>
`SELECT *
  FROM employees e
  LEFT JOIN departments d ON e.department_id = d.id;
  `
- All employees shown even if no dept
3. ### Right Join (Right Outer Join)
- Return all rows from the right table and matching rows from the left table.
- No match returns null from left table.<br> 
`SELECT *
FROM employees e
RIGHT JOIN departments d ON e.department_id = d.id;
  `
- All departments are shown even if no employee is assigned.
4. ### Full Join (Full Outer Join)
- Returns all rows when there is match either in left or right table.
- non matching rows returns null.<br>
`SELECT *
  FROM employees e
  FULL OUTER JOIN departments d ON e.department_id = d.id;
  `
- combines `left` and `right` joins.
5. ### Cross Join
- Returns the cartesian product.
- every row from first table is joined with every row in second table.<br>
`SELECT *
  FROM employees
  CROSS JOIN departments;
  `
- very large result sets!
6. ### Self Join
- a table is joined with itself.
- used when the rows with in the same tables are related (employees & their managers etc)
- to compare rows in the same table.<br>
`SELECT a.name, b.name
  FROM employees a
  JOIN employees b ON a.manager_id = b.id;
  `

## What is a transaction in DBMS? What are the properties of a transaction?
A `transaction` in DBMS is a sequence of one or more sql operations executed or performed as a single unit of work.
- it is executed as a whole either completely or not at all, to ensure data integrity.
- guarantees the valid state of database even error or system failures occurred.
### Properties of transaction (ACID Properties)
1. #### Atomicity
- All operations with in transactions are completed successfully or none are applied.
- No partial updates.
2. #### Consistency
- Transaction takes the database from one valid state to another valid state.
- Maintaining integrity
3. #### Isolation
- Transactions are **independent**.
- Not interfere other transactions when running simultaneously.
- Intermediate results are not visible to other transactions.
4. #### Durability 
- Once the transaction is **commited**, the changes are **permanent**, even if the system crashes.




#### References
1. [geeksforgeeks](https://www.geeksforgeeks.org/commonly-asked-dbms-interview-questions/)