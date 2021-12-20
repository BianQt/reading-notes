# Redux - Combined Reducers

## Review, Research, and Discussion
* Why choose Redux instead of the Context API for global state?
   - Context API is easy to is use as it has a short learning curve. It requires less code, and because there's no need of extra libraries, bundle sizes are reduced. Redux on the other hand requires adding more libraries to the application bundle. The syntax is complex and extensive creating unnecessary work and complexity.

* What is the purpose of a reducer?
   - A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

* What does an action contain?
   - Actions: Actions are a plain JavaScript object that contains information. Actions are the only source of information for the store. Actions have a type field that tells what kind of action to perform and all other fields contain information or data.

* Why do we need to copy the state in a reducer?
   - If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part.



## Vocabulary Terms
* **immutable state** : its value cannot be changed once it's created.
* **time travel in redux** : is the ability to move back and forth among the previous states of an application and view the results in real time.  
* **action creator** : is merely a function that returns an action object. 
* **reducer** : it's a pure function that takes an action and the previous state of the application and returns the new state.
* **dispatch** : is a function of the Redux store


## Preparation Materials
The components of Redux architecture are explained below.

* **STORE:** A Store is a place where the entire state of your application lists. It manages the status of the application and has a dispatch(action) function. It is like a brain responsible for all moving parts in Redux.

* **ACTION:** Action is sent or dispatched from the view which are payloads that can be read by Reducers. It is a pure object created to store the information of the user's event. It includes information such as type of action, time of occurrence, location of occurrence, its coordinates, and which state it aims to change.

* **REDUCER:** Reducer read the payloads from the actions and then updates the store via the state accordingly. It is a pure function to return a new state from the initial state.

### Using combineReducers
The most common state shape for a Redux app is a plain Javascript object containing "slices" of domain-specific data at each top-level key. Similarly, the most common approach to writing reducer logic for that state shape is to have "slice reducer" functions, each with the same (state, action) signature, and each responsible for managing all updates to that specific slice of state. Multiple slice reducers can respond to the same action, independently update their own slice as needed, and the updated slices are combined into the new state object.

Because this pattern is so common, Redux provides the combineReducers utility to implement that behavior. It is an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function.