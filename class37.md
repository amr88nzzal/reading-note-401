# Redux - Combined Reducers

### 1. Why choose Redux instead of the Context API for global state?
- Context API is great for small applications where state changes are minimal but Redux is better for large applications where there are many changes to state. Redux also offer time-travel and single source of truth for state.

- To manage huge applications with complex state management, in a large scale application, Redux is a better way to control state.

- In a large scale application, Redux is a better way to control state.


### 2. What is the purpose of a reducer?
- The reducer takes a state and an action and returns a new state
### 3. What does an action contain?
-  Object literals that tell the reducer what is being done to the app, and any data required for the update.
### 4. Why do we need to copy the state in a reducer?
- Reducers are not allowed to modify the existing state, instead they must make immutable updates by copying the existing state and making changes to the copied values.
 ##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| Immutable state|A State cannot be modified, reducers must make copies of existing state to make updates.|
| Time travel in redux|Time travel is the ability to move back and forth among the previous states of an application and view the results in real time. With Redux, given a specific state and a specific action, the next state of the application is always exactly the same.|
| Action creator|A function that literally creates an action object. In Redux, action creators simply return an action object and pass the argument value if necessary(The only way to change the state is to dispatch an action, an object that describes what happened.)|
| Reducer|A pure functions that take the previous state and an action, and return the next state. Like any other functions, you can split reducers into smaller functions to help do the work, or write reusable reducers for common tasks.|
 dispatch|dispatch is the act of sending something somewhere. In computer science, this term is used to indicate the same concept in different contexts, like to dispatch a call to a function, dispatch an event to a listener, dispatch an interrupt to a handler or dispatch a process to the CPU.\.
 
*** 
 
## Preparation Materials:
 
   ----
### Combined Reducers
  - Why we use Combined Reducers?

-  When the application grows **bigger**, the number of states that we want to maintain the user experience and the whole workflow of the application also increases.
-  Therefore, we tend to **create multiple reducers** for each state instead of making one giant reducer that holds all the information and the functions we want to execute.

- `combineReducers` is simply a utility function to simplify the most common use case when writing Redux reducers. 

- Redux solved this problem by introducing the `combineReducer({reducer_1,reducer_2,...})` function. 
  
- This function takes multiple reducers as an object argument and return one single reducer that manages all the dispatch actions from it.
  
```js
  // reducers.js
export default theDefaultReducer = (state = 0, action) => state

export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

// rootReducer.js
import { combineReducers, createStore } from 'redux'

import theDefaultReducer, {
  firstNamedReducer,
  secondNamedReducer
} from './reducers'

// Use ES6 object literal shorthand syntax to define the object shape
const rootReducer = combineReducers({
  theDefaultReducer,
  firstNamedReducer,
  secondNamedReducer
})

const store = createStore(rootReducer)
```
  
-  What happens when we dispatch an action is that combineReducer invokes all the reducers at once giving each reducer a chance to respond to the action being dispatched. This behavior is somehow not so efficient but it gets the job done, and it will retain the consistency of the whole application work flow.


### combineReducers(reducers)
- As your app grows more complex, you'll want to split your reducing function into separate functions, each managing independent parts of the state.
  
- The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

- The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

`Arguments`
- reducers (Object): An object whose values correspond to different reducing functions that need to be combined into one. See the notes below for some rules every passed reducer must follow.

`Returns`
- (Function): A reducer that invokes every reducer inside the reducers object, and constructs a state object with the same shape.

- [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
- [Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)
- [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)

***