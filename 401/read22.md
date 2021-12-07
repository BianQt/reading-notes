# Component Lifecycle / ```useEffect()``` Hook

## Review, Research, and Discussion
In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

Why do we not need more .html pages in a multi-page React app?
If we wanted a component to show up on every page, where would we put it and why?
Outside the <BrowserRouter/>
Inside the <BrowserRouter />, outside a <Route />
Inside a <Route />
What does routing do with the components that were rendered when a new route is requested
What does props.children contain?
How do useState() and this.setState() differ?
## Vocabulary Terms
* **State Hook** : A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We'll learn other Hooks later.

* **Mounting and Un-Mounting** : The main job of React is to figure out how to modify the DOM to match what the components want to be rendered on the screen. React does so by "mounting" (adding nodes to the DOM), "unmounting" (removing them from the DOM), and "updating" (making changes to nodes already in the DOM).

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
### effects hook

The useEffect Hook allows you to perform side effects in your components.

Some examples of side effects are: fetching data, directly updating the DOM, and timers.

useEffect accepts two arguments. The second argument is optional.

useEffect(<function>, <dependency>)

#### Example
```
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  });

  return <h1>I've rendered {count} times!</h1>;
}

ReactDOM.render(<Timer />, document.getElementById('root'));
```