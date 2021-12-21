# Redux - Asynchronous Actions

### 1. How granular should your reducers be?
- There should be a separate reducer function for each slice of data. They are combined before being put into the store.

### 2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched.
- It depends on the execution (implementation), it can cause errors if written poorly, or can result in clean firm code if done with caution.

### 3. Name a strategy for preventing the above/
- Redux middleware thunk, allows for evaluating the actions.

##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| Store|An immutable object tree in Redux. A store is a state container which holds the application’s state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.|
| Combined reducers|Helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.|
*** 
## Preparation Materials:

#### Redux Middleware and Side Effects#
By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:

1-Logging a value to the console
2-Saving a file
3-Setting an async timer
4-Making an AJAX HTTP request
5-Modifying some state that exists outside of a function, or mutating arguments to a function
6-Generating random numbers or unique random IDs (such as Math.random() or Date.now())


#### Redux middleware were designed to enable writing logic that has side effects.

As we said in Part 4, a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.

#### Using Middleware to Enable Async Logic#
Let's look at a couple examples of how middleware can enable us to write some kind of async logic that interacts with the Redux store.

One possibility is writing a middleware that looks for specific action types, and runs async logic when it sees those actions, like these examples:

```
import { client } from '../api/client'

const delayedActionMiddleware = storeAPI => next => action => {
  if (action.type === 'toDos/todoAdded') {
    setTimeout(() => {
      // Delay this action by one second
      next(action)
    }, 1000)
    return
  }

  return next(action)
}

const fetchToDosMiDdleware = storeAPI => next => action => {
  if (action.type === 'toDos/fetchToDos') {
    // Make an API call to fetch toDos from the server
    client.get('toDos').then(toDos => {
      // Dispatch an action with the toDos we received
      storeAPI.dispatch({ type: 'toDos/toDosLoaded', payload: toDos })
    })
  }

  return next(action)
}
```

```
const middlewareEnhancer = applyMiddleware(asyncFunctionMiddleware)
const store = createStore(rootReducer, middlewareEnhancer)

// Write a function that has `dispatch` and `getState` as arguments
const fetchSomeData = (dispatch, getState) => {
  // Make an async HTTP request
  client.get('todos').then(todos => {
    // Dispatch an action with the todos we received
    dispatch({ type: 'todos/todosLoaded', payload: todos })
    // Check the updated store state after dispatching
    const allToDos = getState().todos
    console.log('Number of todos after loading: ', allToDos.length)
  })
}

// Pass the _function_ we wrote to `dispatch`
store.dispatch(fetchSomeData)
// logs: 'Number of todos after loading: ###'
```


#### Thunk 
is a programming concept where a function is used to delay the evaluation/calculation of an operation.

Redux Thunk is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store’s dispatch method, which is then used to dispatch regular synchronous actions inside the function’s body once the asynchronous operations have been completed.

#### Prerequisites
This post assumes you have some basic knowledge of React and Redux. You can refer to this post if you’re getting started with Redux.

This tutorial builds off of a hypothetical Todo application that tracks tasks that need to be accomplished and have been completed. We can presume that create-react-app was used to generate a new React application, and redux, react-redux, and axios have already been installed.

The finer details on how to build a Todo application from scratch are not explained here. It is presented as a conceptual setting for highlighting Redux Thunk.

#### Adding redux-thunk 
`npm install redux-thunk@2.3.0`

Now apply the middleware when creating your app’s store using Redux’s applyMiddleware. Given a React application with redux and react-redux, your index.js file might look like this:

```
import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import { createStore, applyMiddleware } from 'redux';
import thunk from 'redux-thunk';
import './index.css';
import rootReducer from './reducers';
import App from './App';
import * as serviceWorker from './serviceWorker';

// use applyMiddleware to add the thunk middleware to the store
const store = createStore(rootReducer, applyMiddleware(thunk));

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
);
```