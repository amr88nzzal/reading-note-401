# Data Modeling  

### 1. Name 3 advantages to Test Driven Development.
 * Better program design, and higher code quality.
 * Reduces the time required for project development.
 * Code flexibility and easier maintenance.
***

### 2. In what case would you need to use beforeEach() or afterEach() in a test suite?
  * beforeEach() method needed to be called before the test running.
  * afterEach()  method needed to be called to rest the variables after the test running.

***

### 3. What is one downside of Test Driven Development. 
 * slow process (you need an extra time for straight forward implementations).
 * Not running frequently tests enough.
 * writing too large tests.


***

### 4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
* Inheritance, is that classes define a type which can be instantiated at runtime, while the prototype itself is an object instance.
* The inheritance is more efficient and simple with ES6 classes.

***

### 5. Why REST?

* Good for caching a lot of requests.
* Can be used well where network bandwidth is a constraint.
* Flexible
* Much easier to code/implement for web services than SOAP.
* Easy to Understand and Implement
* Don't need to maintain a state of information from one request to another.
* Caching is Easier with REST


***

## Vocabulary Terms:
|             Term          |                                                                                                   Definition                                                                                                   |
| :-------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      Functional programming       |                           is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects.                 |
| object-oriented programming (OOP) |      is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior.       |
|              Classes              | template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics. |
|              `super`              |                                                                     The super keyword is used to access and call functions on an object's parent.                                                                     |
|              `this`               |                        A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.                        |
|   Test Driven Development (TDD)   |                           Test-driven development (TDD) is a software development process relying on software requirements being converted to test cases before software is fully developed                           |
|               Jest                |                                                           Jest is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase.                                                           |
|    Continuous Integration (CI)    |                                                          is the practice of merging all developers' working copies to a shared mainline several times a day                                                           |
|               REST                |                                                         Representational state transfer (REST) is a software architectural style which uses a subset of HTTP.                                                         |
|            Data Model             |                     A data model (or datamodel) is an abstract model that organizes elements of data and standardizes how they relate to one another 

***
## Preparation Materials

### SQL 
* SQL stands for Structured Query Language
* SQL lets you access and manipulate databases
* SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International 
* Organization for Standardization (ISO) in 1987

 
### noSQL
NoSQL databases are purpose built for specific data models and have flexible schemas for building modern applications. NoSQL databases are widely recognized for their ease of development, functionality, and performance at scale.

 
### SQL vs noSQL
 #### The main differences between SQL and NoSQL databases.

||SQL Databases|NoSQL Databases|
|--|--|--|
|Data Storage Model|Tables with fixed rows and columns|Document: JSON documents, Key-value: key-value pairs, Wide-column: tables with rows and dynamic columns, Graph: nodes and edges|
|Development History|Developed in the 1970s with a focus on reducing data duplication|Developed in the late 2000s with a focus on scaling and allowing for rapid application change driven by agile and DevOps practices.|
|Examples|Oracle, MySQL, Microsoft SQL Server, and PostgreSQL|Document: MongoDB and CouchDB, Key-value: Redis and DynamoDB, Wide-column: Cassandra and HBase, Graph: Neo4j and Amazon Neptune|
|Primary Purpose|General purpose|Document: general purpose, Key-value: large amounts of data with simple lookup queries, Wide-column: large amounts of data with predictable query patterns, Graph: analyzing and traversing relationships between connected data|
|Schemas|Rigid|Flexible|
|Scaling|Vertical (scale-up with a larger server)|Horizontal (scale-out across commodity servers)|
|Multi-Record ACID Transactions|Supported|Most do not support multi-record ACID transactions. However, some—like MongoDB—do.|
|Joins|Typically required|Typically not required|
|Data to Object Mapping|Requires ORM (object-relational mapping)|Many do not require ORMs. MongoDB documents map directly to data structures in most popular programming languages.|
