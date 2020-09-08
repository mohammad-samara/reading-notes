# Data Modeling & NoSQL Databases

- 1. Why would a developer choose to make data models?
  - helps design the database at the conceptual, physical and logical levels. Data Model structure helps to define the relational tables, primary and foreign keys and stored procedures.
- 2. What purpose do CRUD operations serve?
  - In computer programming, create, read, update, and delete (CRUD) are the four basic functions of persistent storage. Alternate words are sometimes used when defining the four basic functions of CRUD, such as retrieve instead of read, modify instead of update, or destroy instead of delete.
  - Explaining Crud Operations. CRUD is an acronym that comes from the world of computer programming and refers to the four functions that are considered necessary to implement a persistent storage application: create, read, update and delete.
- 3. What kind of database is Postgres? What kind of database is MongoDB?
  - MongoDB is an open source, non- relational database management system. PostgreSQL is a relational database management system. MongoDB has mainly programmed in C and C++ programming language and JavaScript language.
- 4. What is Mongoose and why do we need it?
  - Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node. js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.
- 5. Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.
  - 1. Batch Processing
  - 2. Real-Time Processing
  - 3. Data Mining
  - A department store is a large store, divided into departments which sell such products as furnishings, electronics, clothing, footwear, toys, cosmetics, and sometimes also groceries. ... A department store has several departments housed under the same roof to facilitate buying, customer service, and merchandising.
  - Constraints are the rules that force DBMSs to check that data satisfies the semantics. ... constraints. There are several kinds of integrity constraints, described below. ... Neither the PK nor any part of it can contain null values. This is ... It means the reference from a row in one table to another table must be valid.

## Document the following Vocabulary Terms:

Vocabulary | Definition
-----------------------------|-------------------------------------
database | is an organized collection of structured information, or data, typically stored electronically in a computer system.
data model | define how data is connected to each other and how they are processed and stored inside the system.
CRUD | represents an acronym for the database operations Create, Read, Update, and Delete.
schema | is a collection of database objects including tables, views, triggers, stored procedures, indexes, etc.
sanitize | means that you remove all dangerous characters from an input string before passing it to the SQL engine.
Structured Query Language (SQL) | is a programming nomenclature used to do set operations (like union, intersect, and minus) to organize and retrieve information in relational databases, based on “set theory and relational algebra.
Non SQL (NoSQL) | database provides a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases.
MongoDB | is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema.
Mongoose | is an Object Data Modeling (ODM) library for MongoDB and Node. ... MongoDB is a schema-less NoSQL document database. It means you can store JSON documents in it, and the structure of these documents can vary as it is not enforced like SQL databases.
record | is a group of related data held within the same structure.
document | is a type of nonrelational database that is designed to store and query data as JSON-like documents.
Object Relation Mapping (ORM) | in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages. |  
<hr>
<br>
## nosql vs sql
- **CouchDB:** is also a document based NoSQL database. It stores data in form of JSON documents.
- **Redis:** is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language.
## nosql modeling techniques
- NoSQL databases are often compared by various non-functional criteria, such as scalability, performance, and consistency.
- This aspect of NoSQL is well-studied both in practice and theory because specific non-functional properties are often the main justification for NoSQL usage and fundamental results on distributed systems like the CAP theorem apply well to NoSQL systems.