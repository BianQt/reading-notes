# React Lifecycle
Lifecycle events methods that you are able to use on components as classes or functions.Mounting, Updating, and Unmounting are the three phases of the component lifecycle.

![react lifecycle](https://blog.logrocket.com/wp-content/uploads/2019/01/react-lifecycle-methods-diagram.png)
## 1. Mounting
When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase.
## 2. Updating
Anytime a component is updated or state changes then it is rerendered. These lifecycle events happen during updating in this order.
## 3. Unmounting
The final phase of the lifecycle if called when a component is being removed from the DOM.

* React allows us to pass values from a parent component down to a child component. The values can be any data type, from strings to functions, objects, etc.
* The key difference between props and state is that state is internal and controlled by the component itself while props are external and controlled by whatever renders.
* React components automatically re-render whenever there is a change in their state or props. A simple update of the state, from anywhere in the code, causes all the User Interface (UI) elements to be re-rendered automatically.
* The important thing to know about local state is that when a state value changes, it triggers a re-render.
This state can be passed down to children as props, which allows you to separate your components between smart data-components and dumb presentational-components if you chose.
Here’s a basic counter app using local state:
Your data (the value of the counter) is stored within the App component, and can be passed down its children.