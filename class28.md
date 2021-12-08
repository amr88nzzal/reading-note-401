# Component Lifecycle / useEffect() Hook

### 1. Why do we not need more .html pages in a multi-page React app?
because the React app consists of a single HTML file index. html . The views are coded in JSX format as components. But we sometimes need to build multi-page websites because a single-page website can not always represent complete information.

***

### 2. If we wanted a component to show up on every page, where would we put it and why?
  * Inside a <Route /> : because React Router is a standard library for routing in React. It enables the navigation among views of various components in a React Application, allows changing the browser URL, and keeps the UI in sync with the URL.
***


### 3. What does routing do with the components that were rendered when a new route is requested
React Router uses component structure to call components, which display the appropriate information. By preventing a page refresh, and using Router or Link, the flash of a white screen or blank page is prevented. This is one increasingly common way of having a more seamless user experience. React router also allows the user to utilize browser functionality like the back button and the refresh page while maintaining the correct view of the application.
***
### 4. What does props.children contain?
props .children represents the content between the opening and the closing tags when invoking/rendering a component. can have one element, multiple elements, or none at all, its value is respectively a single child node, an array of child nodes or undefined.
***
### 5. How do useState() and this.setState() differ?

setState is merging the previous state with the new one, it means that you dont have to pass the full state object every time you want to change some part of the state. React will update given properties and won’t touch the rest. The useState’s updater rewrites a previous state with a new one and it does not perform any merging. Its just replacement instead of merging.

*** 
##  Vocabulary Terms :

| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| State Hook|A special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.|
| Mounting and Un-Mounting|The main job of React is to figure out how to modify the DOM to match what the components want to be rendered on the screen. React does so by mounting (adding nodes to the DOM), unmounting (removing them from the DOM), and updating (making changes to nodes already in the DOM).   |
*** 
## Preparation Materials: 

 
### Using the Effect Hook

* The Effect Hook lets you perform side effects in function components, Data fetching, setting up a subscription, and manually changing the DOM in React components are all examples of side effects.

* useEffect Hook as componentDidMount, componentDidUpdate, and componentWillUnmount combined.

* In React class components, the render method itself shouldn’t cause side effects. It would be too early — we typically want to perform our effects after React has updated the DOM.

* Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect.

* By default, it runs both after the first render and after every update. (We will later talk about how to customize this.) Instead of thinking in terms of “mounting” and “updating”, you might find it easier to think that effects happen “after render”.

* Every effect may return a function that cleans up after it. This lets us keep the logic for adding and removing subscriptions close to each other.

* The Effect Hook unifies both use cases with a single API.

* Tips for Using Effects :

    * Use Multiple Effects to Separate Concerns
    * Optimizing Performance by Skipping Effect
