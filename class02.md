# Express

## 1. What’s the difference between PUT and PATCH?
* put: is for checking if resources is exist, then update, else creating a new one.

* Patch : used to update a resource.

## 2.Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
* [Postman](https://www.postman.com/)
* [MockServer](https://www.mock-server.com/)
* [Mirage js](https://miragejs.com/)

## 3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

|                           |                                      *APIDoc*                                       |                                           *swagger*                                            |
| :-----------------------: | :---------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------: |
|        Popularity         |                                    Less Popular                                     |                                          More Popular                                          |
|        Consistency        |                                    Less consist                                     |                                          More consist                                          |
| Implementation complexity | both required documentation content on implemented method as customize comment data | In addition they allow to write documentation data in separate resource file as .js and .json. |
|        Maintenance        | have to modify documentation for each affected method/endpoints if service changed  |          we can limit changes. But by implementing apidocjs we can isolate the layer.          |

## 4. Compare and contrast SOAP and ReST
| SOAP                                                                                                                                                                                                                                | REST                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| stands for Simple Object Access Protocol                                                                                                                                                                                            | Representational State Transfer                                                                                                                                                                          |
| SOAP is a protocol. SOAP was designed with a specification. It includes a WSDL file which has the required information on what the web service does in addition to the location of the web service.                                 | REST is an Architectural style in which a web service can only be treated as a RESTful service if it follows the constraints of being Client Server Stateless Cacheable Layered System Uniform Interface |
| SOAP cannot make use of REST since SOAP is a protocol and REST is an architectural pattern.                                                                                                                                         | REST can make use of SOAP as the underlying protocol for web services, because in the end it is just an architectural pattern.                                                                           |
| SOAP uses service interfaces to expose its functionality to client applications. In SOAP, the WSDL file provides the client with the necessary information which can be used to understand what services the web service can offer. | REST use Uniform Service locators to access to the components on the hardware device.                                                                                                                    |



## Vocabulary Terms:

|    word    |                                                                                                                                              definition                                                                                                                                               |
| :--------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Web Server | A web server is a computer that runs websites. It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users. This intercommunication is done using Hypertext Transfer Protocol (HTTP). |
|  Express   |It's a web framework that let's you structure a web application to handle multiple different http requests at a specific url                                                                                      |
|  Routing   |is the process of selecting a path for traffic in a network or between or across multiple networks.                                                                                                  |
|    WRRC    | It's a blueprint describes the way that a backend server deals with different http requests/responses and where it redirects each request and response.                                                                        |