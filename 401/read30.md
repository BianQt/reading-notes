# Application State with Redux
## Review, Research, and Discussion

* What are the advantages of storing tokens in “Cookies” vs “Local Storage”
    - Local Storage is available for every page and remains even when the web browser is closed, but you cannot read it on the server. The stored data has no expiration date in local storage. ... Local Storage is for client side, whereas cookies are for the client as well as server side.

* Explain 3rd party cookies.
   - Third-party cookies are created by domains that are not the website (or domain) that you are visiting. These are usually used for online-advertising purposes and placed on a website through adding scripts or tags. A third-party cookie is accessible on any website that loads the third-party server's code.
* How do pixel tags work?
  - Pixel tags -- or, web beacons, as they are also known -- attach to a browser and collect information about an anonymous user's movements on the Internet. These little beacons allow sites to provide users with ads for services and products that are relevant to them.

## Vocabulary Terms
* **cookies** : Cookies are files created by websites you visit. They make your online experience easier by saving browsing information. With cookies, sites can keep you signed in, remember your site preferences, and give you locally relevant content.

* **authorization** : is the process of giving someone permission to do or have something.
* **access control** : is a method of restricting network access based on the roles of individual users within an enterprise.
* **conditional rendering** : Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition.

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
Redux is an open-source JavaScript library used to manage application state. React uses Redux for building the user interface. It was first introduced by Dan Abramov and Andrew Clark in 2015.

React Redux is the official React binding for Redux. It allows React components to read data from a Redux Store, and dispatch Actions to the Store to update data. Redux helps apps to scale by providing a sensible way to manage state through a unidirectional data flow model. React Redux is conceptually simple. It subscribes to the Redux store, checks to see if the data which your component wants have changed, and re-renders your component.
###
Redux was inspired by Flux. Redux studied the Flux architecture and omitted unnecessary complexity.

    - Redux does not have Dispatcher concept.
    - Redux has an only Store whereas Flux has many Stores.
    - The Action objects will be received and handled directly by Store.

### Why use React Redux?
The main reason to use React Redux are:


* React Redux is the official UI bindings for react Application. It is kept up-to-date with any API changes to ensure that your React components behave as expected.
* It encourages good 'React' architecture.
* It implements many performance optimizations internally, which allows to components re-render only when it actually needs.

### Redux Architecture
The components of Redux architecture are explained below.

* **STORE:** A Store is a place where the entire state of your application lists. It manages the status of the application and has a dispatch(action) function. It is like a brain responsible for all moving parts in Redux.

* **ACTION:** Action is sent or dispatched from the view which are payloads that can be read by Reducers. It is a pure object created to store the information of the user's event. It includes information such as type of action, time of occurrence, location of occurrence, its coordinates, and which state it aims to change.

* **REDUCER:** Reducer read the payloads from the actions and then updates the store via the state accordingly. It is a pure function to return a new state from the initial state.