# Advanced State with Reducers

## Review, Research, and Discussion
* How can we ensure that an effect hook runs only once?
   -  You can pass an empty array ( [] ) as a second argument. 
* Can useState() update more than one state variable at the same time?
   -  You could combine the loading state and data state into one state object and then you could do one setState call and there will only be one render.

* Is useState() synchronous?
  - useState and setState both are asynchronous


## Vocabulary Terms
* **State Hook** : A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.
* **Component Lifecycle** : Each component in React has a lifecycle which you can monitor and manipulate during its three main phases. The three phases are: Mounting, Updating, and Unmounting.


## Preview
- Which 3 things had you heard about previously and now have better clarity on?
  - Hooks 
  - Function components

- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   - Hooks 
   - Function components

- What are you most excited about trying to implement or see how it works?
  -AWS
  - React
  - SQL Databases


## Preparation Materials
### useReducer hook
The useReducer Hook is the better alternative to the useState hook and is generally more preferred over the useState hook when you have complex state-building logic or when the next state value depends upon its previous value or when the components are needed to be optimized.
###
The useReducer hook takes three arguments including reducer, initial state, and the function to load the initial state lazily.

#### Syntax:

```const [state, dispatch] = useReducer(reducer, initialArgs, init);```

