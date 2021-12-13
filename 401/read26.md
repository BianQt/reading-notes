# Context API - Behaviors

## Review, Research, and Discussion
* When you have multiple contexts, what component type should you use (class/function) and why?
   - Function
* What are some good use cases for using the Context API for global state?
   - Authentication 
* How can you best test context?
   - The best way to test Context is to make our tests unaware of its existence and avoiding mocks. 

## Vocabulary Terms
* **context** : Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component: class App extends React.

* **useContext()** : “useContext” hook is used to create common data that can be accessed throughout the component hierarchy without passing the props down manually to each level. Context defined will be available to all the child components without involving “props”.

* **static context** : This rule applies when the static contextType property of a React component is not properly specified. The contextType property is used to consume a context created with React. ... When the property is specified for a React component, you can access the current value of the context using this.




## Preview
- Which 3 things had you heard about previously and now have better clarity on?
  - Hooks 
  - Function components
  - Context API

- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   - Hooks 
   - Context API

- What are you most excited about trying to implement or see how it works?
  - AWS
  - React Hooks
  - React State management


## Preparation Materials
### context api
Context API is a React API that can solve a lot of problems that modern applications face related to state management and how they’re passing state to their components. Instead of installing a state management library in your project that will eventually cost your project performance and increase your bundle size, you can easily go with Context API and be fine with it.

###
The Context API can be used to share data with multiple components, without having to pass data through props manually. For example, some use cases the Context API is ideal for: theming, user language, authentication, etc.

#### createContext
To start with the Context API, the first thing we need to do is create a context using the createContext function from React.
```
const NotesContext = createContext([]);
```
The createContext function accepts an initial value, but this initial value is not required.

After creating your context, that context now has two React components that are going to be used: Provider and Consumer.

#### Provider
The Provider component is going to be used to wrap the components that are going to have access to our context.

```
<NotesContext.Provider value={this.state.notes}>
...
</Notes.Provider>
```

The Provider component receives a prop called value, which can be accessed from all the components that are wrapped inside Provider, and it will be responsible to grant access to the context data.

#### Consumer
After you wrap all the components that are going to need access to the context with the Provider component, you need to tell which component is going to consume that data.

The Consumer component allows a React component to subscribe to the context changes. The component makes the data available using a render prop.
```
<NotesContext.Consumer>
  {values => <h1>{value</h1>}
</Notes.Consumer>
```