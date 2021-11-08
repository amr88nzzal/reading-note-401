# Authentication

## Review, Research, and Discussion

* Explain what a “Singleton” is?
  * the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance.

![01](./pic/c06-01.png)

* Explain how the Singleton pattern can be used with Node modules, specifically with classes
  * Singleton is used by creating a ES6 class.
  * to make sure that you have one and only one instance of an object.
  * A singleton represents a single instance of an object.

* If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
* to use the singleton approach.

## Vocabulary Terms

### Router Middleware :

* Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing. 

### Dynamic Module Loading:

* is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory .
  
### Singleton Pattern :

* the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance.
  
### CRUD -> REST Method Matches :

* (Create, Read, Update, Delete) is an acronym for ways one can operate on stored data.

![01](./pic/c06-02.png)

### Mock Testing :

* it is mocking real test to test the program like a fack data. 

## Securing Passwords with Bcrypt Hashing Function 

* Passwords are the first line of defense against cyber criminals.

* Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible. 
* The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords. 

![01](./pic/c06-03.jpg)

# Basic access authentication

* is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. 

![01](./pic/c06-04.gif)
