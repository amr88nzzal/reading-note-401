# Application State with Redux


### 1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”.
- Cookies have an expiry date, unlike local storage
- Cookies are automatically saved, sent and removed by the browser.
- cookies can be accessed from both the back-end (req.headers.cookie) and - front-end but the local storage Data is only accessed from the local browser. Server can’t access local storage unless a request been send (POST or GET)
- Cookies have 4094 byte per cookie but local storage 5 MB per domain

### 2. Explain 3rd party cookies.
- Third party cookies are cookies that are set by a website other than the only you are currently on. For example, a "Like" button on a website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites were visited. Such a cookie is considered to be a 3rd party cookie.

### 3. How do pixel tags work?
Pixel tags are typically single pixel, transparent GIF images that are added to a web page. Even though the pixel tag is virtually invisible, it is still served just like any other image you may see online.
 
 ##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| Cookies| A small bit of data stored on a user's computer by the web browser while browsing a webiste, designed to be reliable mechanism for websites to remember stateful information or to record the user's browsing activity.|
| Authorization |The Process of giving someone the ability to access a resource.|
| Access control
| Component of data security that dictates who is allowed to access and use company information and resources. Through authentication and authorization, access control policies make sure users are who they say they are and that they have appropriate access to company data.|
| Conditional rendering
|  - The ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition.
|
*** 
 
## Preparation Materials:


### REDUX 

Redux provides a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse.

The principles of Redux aren't new, but they are packaged and presented for you in an easy to use a library that not only elevates your applications but also improves your general understanding of building JavaScript UIs.

In this course, Dan Abramov will show you the fundamentals of Redux, so that you can start using it to simplify your applications.

### What is Redux? 

Redux takes away some of the hassles faced with state management in large applications. It provides you with a great developer experience, and makes sure that the testability of your app isn’t sacrificed for any of those.

As you develop React applications, you may find that keeping all your state in a top-level component is no longer sufficient for you.

You may also have a lot of data changing in your application over time.


### Why use Redux? 

Redux itself is a standalone library that can be used with any UI layer or framework, including React, Angular, Vue, Ember, and vanilla JS. Although Redux and React are commonly used together, they are independent of each other.

If you are using Redux with any kind of UI framework, you will normally use a "UI binding" library to tie Redux together with your UI framework, rather than directly interacting with the store from your UI code.

React Redux is the official Redux UI binding library for React. If you are using Redux and React together, you should also use React Redux to bind these two libraries.

### Integrating Redux with a UI#

Using Redux with any UI layer requires the same consistent set of steps:

1- Create a Redux store <br>
2-Subscribe to updates <br>
3-Inside the subscription callback: <br>
 a -Get the current store state <br>
 b- Extract the data needed by this piece of UI <br>
 c-Update the UI with the data <br>
4- If necessary, render the UI with initial state <br>
5- Respond to UI inputs by dispatching Redux actions <br>
While it is possible to write this logic by hand, doing so would become very repetitive. In addition, optimizing UI performance would require complicated logic.

The process of subscribing to the store, checking for updated data, and triggering a re-render can be made more generic and reusable. A UI binding library like React Redux handles the store interaction logic, so you don't have to write that code yourself.

***
