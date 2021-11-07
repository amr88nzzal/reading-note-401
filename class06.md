# Authentication

## 1. What is the “Singleton” is (in Computer Science terms)? 

In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.


## 2. how the Singleton pattern can be used with Node modules, specifically with classes?

   ```
   class PrivateSingleton {
       constructor() {
           this.message = 'I am an instance';
       }
   }

   class Singleton {
       constructor() {
           throw new Error('Use Singleton.getInstance()');
       }
   }

   static getInstance() {
       if(!Singleton.instance) {
           singleton.instance = new PrivateSingleton();
       }
       return Singleton.instance;
   }

   module.exports SingleTon.instance;

   ```
## 3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
#### Layers approach.


## Vocabulary Terms

|          Term        |                                                                                                                             Definition **                                                                                                                              |
| :-------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      Router Middleware      |                                                                                                           function hand off the control to the next callback.                                                                                                            |
|   Dynamic Module Loading    | mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. |
|      Singleton Pattern      |                                          software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system                                          |
| CRUD -> REST Method Matches |                                                                Create = PUT with a new URI POST to a base URI returning a newly created URI Read = GET Update = PUT with an existing URI Delete = DELETE                                                                 |
|        Mock Testing         |                                                             Mock testing is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules.


## Preparation Materials

#### Securing Passwords

1- Passwords: minimum length of 8 characters, common maximum length is 64 characters

2-Transmit passwords only over TLS (transport layer protection) or other strong transport

3-Require re-authentication for sensitive features

4-Account lockout: prevent any more login attempts after a series of failed logins

#### Basic Auth 

basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :.

* Server side : 
When the server wants the user agent to authenticate itself towards the server, the server must respond appropriately to unauthenticated requests.

To unauthenticated requests, the server should return a response which contains a HTTP 401 Unauthorized status line[5] and a WWW-Authenticate header field.

* Client side: 

When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.
