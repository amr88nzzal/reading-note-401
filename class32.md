# Context API - Behaviors

### 1. When you have multiple contexts, what component type should you use (class/function) and why?

- The difference is pretty obvious. Class components are ES6 classes and Functional Components are functions. The only constraint for a functional component is to accept props as an argument and return valid JSX.

### 2. What are some good use cases for using the Context API for global state?

- Twilio: Twilio really defines what it means to be API-driven.
- Stripe : Stripe is one of the most successful and best known API-driven businesses.
- Ebay : Unlike the previous companies, eBay didn’t start out with the intent of being API-driven.
- Salesforce : XML APIs have been a part of Salesforce since day one, back in 2000 when it launched.
- Rovi : Rovi is definitely the oldest company on the list, founded as Macrovision in 1983.

### 3. How can you best test context?

- The best way to test Context is to make our tests unaware of its existence and avoiding mocks. We want to test our components in the same way that developers would use them (behavioral testing) and mimic the way they would run in our applications (integration testing).

***

## Vocabulary Terms: 
| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| context|Is a method to pass props from parent to child component(s), by storing the props in a store(similar in Redux) and using these props from the store by child component(s) without actually passing them manually at each level of the component tree.|
|  useContext()| “useContext” hook is used to create common data that can be accessed throughout the component hierarchy without passing the props down manually to each level |
| static context| If you are using the experimental public class fields syntax, you can use a static class field to initialize your contextType.  |

***
 
## Preparation Materials:

 ### Context API

- **Context** provides a way to pass data through the component tree without having to pass props down manually at every level.

- Before You Use Context :Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

- If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

- Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

- The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.

- Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

- The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.
  
 ***
