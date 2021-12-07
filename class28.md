# Advanced State with Reducers

### 1. How can we ensure that an effect hook runs only once?
if you provide an empty array or nothing, the useEffect will only execute once, similar to how componentDidMount works.

### 2. Can useState() update more than one state variable at the same time?
We could do one setState call and there will only be one render. Unlike the setState in class components, the setState returned from useState doesn’t merge objects with existing state, it replaces the object entirely.

### 3. Is useState() synchronous?
Both useState and setState are asynchronous operations. The useState and setState methods do not return promises, despite the fact that they are asynchronous. As a result, we can't utilize async/await to obtain the updated state values or attach a then handler to it.

*** 
##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| State Hook|A special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.|
| Component Lifecycle|  Every React Component has a lifecycle of its own, lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component's existence. ... Mounting: Mounting is the stage of rendering the JSX returned by the render method itself.|
*** 
## Preparation Materials: 
#### How does useReducer work? 
* useReducer is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.

* useReducer is one of the additional Hooks that shipped with React 16.8. An alternative to the useState Hook, it helps you manage complex state logic in React applications. When combined with other Hooks like useContext, useReducer can be a good alternative to Redux or MobX — indeed, it can sometimes be an outright better option.

* There are three main building blocks in Redux:
   * A store — an immutable object that holds the applications state data
   * A reducer — a function that returns some state data, triggered by an action type.
   * An action — an object that tells the reducer how to change the state. It must contain a type property, and it can contain an optional payload property
const initialState = { count: 0 }

* const [state, dispatch] = useReducer(reducer, initialState)
The reduce() method in JavaScript executes a reducer function on each element of the array an and then returns a single value.

* There are two different ways to initialize the useReducer state.

 1. The simplest way is to pass the initial state as a second argument
  const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );

2. You can also create the initial state lazily
To do this, you can pass an init function as the third argument. The initial state will be set to init(initialArg)
***
