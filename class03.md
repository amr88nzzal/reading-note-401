# Express REST API
![img](./pic/c03-01.png)

***

## 1. Name 3 real world use cases where you’d want to change the request with custom middleware.
  * API management
  * authentication 
  * messaging
  
***

## 2. True or false: The route handler is middleware?
  false, Route handler is a code that's handling the HTTP methods: Get(), Put(), Post() and Delete(). 

***

##  3. In what ways can a middleware function end the process and send data to the browser?
* Execute any code.
* Make changes to the request and the response objects.
* End the request-response cycle.
* Call the next middleware in the stack.

***

## 4. At what point in the request lifecycle can you “inject” middleware?
  After receiving  the requests, and before sending the response, and at any point get an error.

***

## 5. What can cause express to error with “Request headers sent twice, cannot start a second response”.
  when request handler function already sent a response to the client

***

## Vocabulary Terms:
|        word          |                                                                         definition                                                                         |
| :---------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       Middleware        | Any functionality that sits in between request/response, but does not send out response itself (have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle). |
|      Request Object   |                               The request object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers (represents the information in the HTTP request from the client to the server).                        |
| Application Middleware  |                                                 Middleware that plays a role in the function of the application.                                                 |
|   Routing Middleware    |                                                        a middleware that works on router level router.use                                                        |
| Test Driven Development |                        is software development approach in which test cases are developed to specify and validate what the code will do.                         |
|   Behavioral Testing    |                                                         Testing of the external behavior of the program.                                                         |
|         Response object   |              The response object represents the HTTP response that an Express app sends when it gets an HTTP request(Information in the HTTP response from the server to the client.)                      |

***

## Preparation Materials

### ES6 Classes
Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

***

### Express Routing
* Routing refers to how an application’s endpoints (URIs) respond to client requests.
* Define routing using methods of the Express app object that correspond to HTTP methods
* Routing methods specify a callback function (sometimes called "handler functions") called when the application receives a request to the specified route (endpoint) and HTTP method
* Routing methods can have more than one callback function as arguments

***