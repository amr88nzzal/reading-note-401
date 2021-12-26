# Redux - Additional Topics

### 1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
- The most ‘redux-like’ way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.

### 2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
- by exporting the new data to replace the state from the reducer. The action calling the reducer will be sent as a function rather than an object and then you can dispatch it.

*** 
##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| Middleware|Code you put in between the framework receiving a request and the framework generating the response.|
| Thunk| A middleware that allows you to return functions, rather than just actions, within Redux. This allows for delayed actions, including working with promises. One of the main use cases for this middleware is for handling actions that might not be synchronous, for example, using axios to send a GET request.|
*** 


## Preparation Materials:
- Redux Toolkit
   * Purpose:
   * The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

     1. “Configuring a Redux store is too complicated”
     2. “I have to add a lot of packages to get Redux to do anything useful”
     3.“Redux requires too much boilerplate code”
- Advantages
    1. Simple Includes utilities to simplify common use cases like store setup, creating reducers, immutable update logic, and more.

   2. Opinionated Provides good defaults for store setup out of the box, and includes the most commonly used Redux addons built-in.
   3. Powerful Takes inspiration from libraries like Immer and Autodux to let you write “mutative” immutable update logic, and even create entire “slices” of state automatically.

    4. Effective Lets you focus on the core logic your app needs, so you can do more work with less code.
- Redux Toolkit includes:
  - !. configureStore() function with simplified configuration options. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.

1. reateReducer() utility that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements.

2. createAction() utility that returns an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.

3. createSlice() function that accepts a set of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.

4. createSelector utility from the Reselect library, re-exported for ease of use.
***
* The core idea
  - State is the heart of each application and there is no quicker way to create buggy, unmanageable applications than by producing an inconsistent state or state that is out-of-sync with local variables that linger around. Hence many state management solutions try to restrict the ways in which you can modify state, for example by making state immutable. But this introduces new problems; data needs to be normalized, referential integrity can no longer be guaranteed and it becomes next to impossible to use powerful concepts like classes in case you fancy those.
 
 *** 
