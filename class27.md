# useState() Hook

## 1. How does React differ from vanilla JS/HTML/CSS?

- Plain JS apps usually start with the initial UI created on the server (as HTML), whereas React apps start with a blank HTML page, and dynamically create the initial state in JavaScript. React requires you to break your UI into components, but plain JS apps can be structured in any way you see fit.
- Vanilla JS requires a lot of typing : JS requires a lot of codes so would be little messy and that make it less efficient than React.*
    - React JS is for code organization :ReactJs is great for organizing the code. as you can see all the above code is on one page, script.js. 
    - “React :A JavaScript library for building user interfaces. Lots of people use React as the V in MVC. Since React makes no assumptions about the rest of your technology stack, it’s easy to try it out on a small feature in an existing project”. 
    - “Vanilla.JS: A fast, lightweight and cross-platform framework. It is a fast and cross-platform framework for building incredible, powerful JavaScript applications. it is the most lightweight framework available anywhere”.

## 2. What is the primary difference between a function component and a class component?

 - *Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks*
    - *You end up with less code*
    - *They help you to use best practices. It will get easier to separate container and presentational components because you need to think more about your component’s state if you don’t have access to setState() in your component*
    - *The React team mentioned that there may be a performance boost for functional component in future React version*

*** 

## Vocabulary Terms : 

| Term      | Definition                                                                                                      |
| --------- | --------------------------------------------------------------------------------------------------------------- |
| Functional Components |     are basically a JavaScript functions, these are typically arrow functions but can also be created with the regular function keyword (the best practice). Sometimes referred to as “dumb” or “stateless” components as they simply accept data and display them in some form; that is they are mainly responsible for rendering UI.              |
| Children / Child Components
|  children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children. |

***

## Preparation Materials:

* Making Sense of React Hooks
> Why Hooks?

We know that components and top-down data flow help us organize a large UI into small, independent, reusable pieces. However, we often can’t break complex components down any further because the logic is stateful and can’t be extracted to a function or another component. Sometimes that’s what people mean when they say React doesn’t let them “separate concerns.”
> What Are Hooks, Exactly?
 Functions seem to be a perfect mechanism for code reuse. Moving logic between functions takes the least amount of effort. However, functions can’t have local React state inside them. You can’t extract behavior like “watch window size and update the state” or “animate a value over time” from a class component without restructuring your code or introducing an abstraction like Observables. Both approaches hurt the simplicity that we like about React. Hooks solve exactly that problem.      

***

> the state hook
> What is a Hook?
A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.  

***

> Use Hooks : *“when we write a function component, and then we want to add some state to it, previously you do this by converting it to a class. But, now you can do it by using a Hook inside the existing function component”.*

**Using the State Hook :** *In a function component, we have no this, so we can’t assign or read this.state. Instead, we call the useState.*

***

> When would I use a Hook?
If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

***hooks api reference***
> Basic Hooks

- useState
- useEffect
- useContext

> Additional Hooks

- useReducer
- useCallback
- useMemo
- useRef
- useImperativeHandle
- useLayoutEffect
- useDebugValue
