# Database Normalization

Database normalization is a process used to organize a database into tables and columns. The main idea with this is that a table should be about a specific topic and only supporting topics included.

# Reasons for Database Normalization

There are three main reasons to normalize a database. The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries.

# Insert Anomaly

There are facts we cannot record until we know information for the entire row. In our example we cannot record a new sales office until we also know the sales person. Why? Because in order to create the record, we need provide a primary key. In our case this is the EmployeeID.

# Update Anomaly

In this case we have the same information in several rows. For instance if the office number changes, then there are multiple updates that need to be made. If we don’t update all rows, then inconsistencies appear.

Deletion Anomaly
Deletion of a row causes removal of more than one set of facts. For instance, if John Hunt retires, then deleting that row cause us to lose information about the New York office.

# Definition of Database Normalization

There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. There are several additional forms, such as BCNF, but I consider those advanced, and not too necessary to learn in the beginning.

The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form. Before we discuss the various forms and rules in detail, let’s summarize the various forms:

1. First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
2. Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
3. Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key