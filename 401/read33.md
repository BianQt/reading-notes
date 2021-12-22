# Redux - Additional Topics

## Review, Research, and Discussion
* What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
    - The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.
* When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
    
    - A state is stored centrally in a store.
    - The UI subscribes to state via the connect HOC from react-redux. It renders and re-renders, following changes in the state.
    - State changes are launched with the help of action-creators. An action creator function actually return an action-object, which has at least the type property.
    - The action-object is passed to redux's dispatch function, which eventually passes it to the reducer function, we define.
    - The reducer function composes and returns a new state, based on the received action-object.
    - The returned state is becoming new state in the store.

## Vocabulary Terms
* **middleware** : is a type of computer software that provides services to software applications beyond those available from the operating system. ... Middleware makes it easier for software developers to implement communication and input/output, so they can focus on the specific purpose of their application.
* **thunk** :  is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the function's body once the asynchronous operations have been completed.

## Preview
- Which 3 things had you heard about previously and now have better clarity on?
  - Hooks 
  - Function components
  - Context API

- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   - Hooks 
   - Context API
   - Redux

- What are you most excited about trying to implement or see how it works?
  - AWS
  - React Hooks
  - React State management


## Preparation Materials
[Redux Toolkit (RTK)](https://redux-toolkit.js.org/tutorials/overview)

