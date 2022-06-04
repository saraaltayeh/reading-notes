# Data Modeling

## SQL vs NoSQL

- SQL databases are primarily called as Relational Databases (RDBMS)

- SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores.

- SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.

## SQL Database Examples

1. MySQL Community Edition

MySQL database is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js.
2. MS-SQL Server Express Edition

It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft.
3. Oracle Express Edition

It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment.

## NoSQL Database Examples

1. MongoDB
Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents.
2. CouchDB
CouchDB is also a document based NoSQL database. It stores data in form of JSON documents.
3. Redis
Redis is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language.

## Data Modeling – Table Elements

- The Table Name, which is located at the top of the table.
- The Primary Keys.  Remember the primary keys uniquely identify each row in a table.  A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key.
- Table Columns – There can be one or more table columns.  To keep the diagrams simple, I don’t show the data types.  I may introduce those later when we focus on more comprehensive modeling.
- Foreign Key – This is a column or set of columns which match a primary key in another table.

## Data Modeling – Table Relationships

This is called a one-to-many relationship.
In our example there are many employees in on department; therefore, we show a many-to-one relationship.
