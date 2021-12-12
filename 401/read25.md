# Context API

## Review, Research, and Discussion

* Describe use cases useState() vs useReducer()
   - Next state depends on the previous: It is always better to use this method when the state depends on the previous one. 
   - Complex state shape: When the state consists of more than primitive values, like nested object or arrays
   - Easy to test: Reducers are pure functions, and this means they have no side effects and must return the same outcome given the same arguments. 
* Why do custom hooks need the use prefix?
   - This convention is very important. Without it, we wouldn’t be able to automatically check for violations of rules of Hooks because we couldn’t tell if a certain function contains calls to Hooks inside of it.
* What do custom hooks usually do?
   - Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.

* Using any list of custom hooks, research and name one that you think will be useful in your applications
   - useReducer
* Describe how a hook that fetches API data might work 
  - create an asynchronous function to fetch our data. 
  - Put the fetchData function above in the useEffect hook and call it
  - Once we get a response, we are parsing it using the .json() function, meaning that we are transforming the response into JSON data that we can easily read

## Vocabulary Terms

* **reducer**: is a pure function that takes an action and the previous state of the application and returns the new state. The action describes what happened and it is the reducer's job to return the new state based on that action.

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