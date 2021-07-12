# Mongo and Mongoose

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## Fill in the chart below with five differences between SQL and NoSQL databases

|---------------|-------------|
|SQL|NoSQL|
| called as Relational Databases (RDBMS)| called as non-relational or distributed database.|
| table based databases | document based, key-value pairs, graph databases or wide-column stores|
|have predefined schema for unstructured data | have dynamic schema for unstructured data |
|vertically scalable |horizontally scalable |
|good fit for the complex query intensive environment |  not good fit for complex queries|

## What kind of data is a good fit for an SQL database?

**When your data is highly structured and associations among the program entities are clearly defined.**

## Give a real world example

**Online stores, health care providers, clubs, libraries and video stores.**

## What kind of data is a good fit a NoSQL database?

1. Semi-structured or Unstructured data / flexible schema
2. Limited pre-defined access paths and query patterns
3. No complex queries, stored procedures, or views
4. High velocity transactions
5. Large volume of data (in Terabyte range) requiring quick and cheap scalability
6. Requires distributed computing and storage
7. No Data Warehouse, Analytics or BI use cases

## Give a real world example

**Twitter,Facebook.**

## Which type of database is best for hierarchical data storage?

**NoSQL databases.**

## Which type of database is best for scalability?

**SQL based databases.**

## What does SQL stand for?

**Structured Query Language.**

## What is a relational database?

**A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables.**

## What type of structure does a relational database work with?

 **Logical Data Structure.**
 
## What is a ‘schema’?

**The database schema is its structure described in a formal language supported by the database management system. The term "schema" refers to the organization of data as a blueprint of how the database is constructed.**

## What is a NoSQL database?

**NoSQL is a type of database that stores and retrieves data without needing to define its structure first.**

## How does it work?

**NoSQL databases use a variety of data models for accessing and managing data. These types of databases are optimized specifically for applications that require large data volume, low latency, and flexible data models, which are achieved by relaxing some of the data consistency restrictions of other databases.**

## What is inside of a Mongo database?

**Records as documents (specifically BSON documents).**

## Which is more flexible - SQL or MongoDB? and why?

**MongoDB because of non-relational database but this cost some safety.**

## What is the disadvantage of a NoSQL database?

**The non-relational database greatly increases access time and scalability, it may lead to data loss.**
