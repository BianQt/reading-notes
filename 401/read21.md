# ```useState()``` Hook

## Review, Research, and Discussion

* How does React differ from vanilla JS/HTML/CSS? 
   - Plain JS apps usually start with the initial UI created on the server (as HTML), whereas React apps start with a blank HTML page, and dynamically create the initial state in JavaScript. React requires you to break your UI into components, but plain JS apps can be structured in any way you see fit.

* What is the primary difference between a function component and a class component?
  - A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element. A class component requires you to extend from React. Component and create a render function which returns a React element. There is no render method used in functional components.


## Vocabulary Terms
* **Functional Components** : A Functional component is a function that takes props and returns JSX. They do not have state or lifecycle methods. Functional components are easier to read, debug, and test. They offer performance benefits, decreased coupling, and greater reusability.

* **Children / Child Components** : Children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children

## Preview

- Which 3 things had you heard about previously and now have better clarity on?
  - Hooks 
  - Function components

- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   - Hooks 
   - Function components

- What are you most excited about trying to implement or see how it works?
  - AWS
  - React
  - SQL Databases

## React Hooks

Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components.
Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.
Since Hooks are regular JavaScript functions, you can combine built-in Hooks provided by React into your own “custom Hooks”. 

### ```useState```
In function component, we have no this, so we can’t assign or read this.state. Instead, we call the useState Hook directly inside our component:
```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);
  ```

-  **What does calling useState do?** It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

-  **What do we pass to useState as an argument?** The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

-  **What does useState return?** It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair.