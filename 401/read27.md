# ```<Login />``` and ```<Auth />```

## Review, Research, and Discussion
* Why is the Context API useful?
  - The Context API is a React structure that enables you to exchange unique details and assists in solving prop-drilling from all levels of your application.

* Can a component outside of a provider get its context?
  - To access a React context outside of the render function, we can use the useContext hook. We create the UserContext by calling the React. createContext method with a default context value. Then in the Users component, we call the useContext hook with UserContext to access the current value of UserContext .

* What are some common use cases for using the Context API?
  - Theming — Pass down app theme.
  - Authentication — Pass down current authenticated user.

* Describe “Context Hell”
  - In this kind of structure, our reliable “parent component solution” becomes a problem, because we would unnecessarily need to pass down the required state data through intermediate components to reach our destination.


## Vocabulary Terms

* **global state** : is the data that is shared between all the components within a React application. When the state is changed, or let's say a filter is added, the components re-render accordingly.

* **global context** : is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component: class App extends React.

* **provider** : is component makes the Redux store available to any nested components that need to access the Redux store. Since any React component in a React Redux app can be connected to the store, most applications will render a <Provider> at the top level, with the entire app's component tree inside of it.

* **consumer** :  is a method to pass props from parent to child component(s), by storing the props in a store(similar in Redux) and using these props from the store by child component(s) without actually passing them manually at each level of the component tree.

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
### what is role based access control?
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that users have to the network.

### react-cookies component
Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them. ... To set or remove the cookies, we are going to use a third-party dependency of react-cookie.


### react-cookies 
Load and save cookies with React

#### Install
```$ npm install react-cookies --save```
#### Usage
```
import { Component } from 'react'
import cookie from 'react-cookies'
 
import LoginPanel from './LoginPanel'
import Dashboard from './Dashboard'
 
class MyApp extends Component {
  constructor () {
    super()
 
    this.onLogin = this.onLogin.bind(this)
    this.onLogout = this.onLogout.bind(this)
  }
 
  componentWillMount() {
    this.state =  { userId: cookie.load('userId') }
  }
 
  onLogin(userId) {
    this.setState({ userId })
    cookie.save('userId', userId, { path: '/' })
  }
 
  onLogout() {
    cookie.remove('userId', { path: '/' })
  }
 
  render() {
    const { userId } = this.state
 
    if (!userId) {
      return <LoginPanel onSuccess={this.onLogin} />
    }
 
    return <Dashboard userId={userId} />
  }
}
```