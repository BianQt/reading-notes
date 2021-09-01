# Thinking in React
## Start With A Mock

### Step 1: Break The UI Into A Component Hierarchy
The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names. If you’re working with a designer, they may have already done this, so go talk to them! Their Photoshop layer names may end up being the names of your React components!

### Step 2: Build A Static Version in React
Now that you have your component hierarchy, it’s time to implement your app. The easiest way is to build a version that takes your data model and renders the UI but has no interactivity. It’s best to decouple these processes because building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing. We’ll see why.

To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.

### Step 3: Identify The Minimal (but complete) Representation Of UI State

To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.

### Step 4: Identify Where Your State Should Live
React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state. 

### Step 5: Add Inverse Data Flow
Now it’s time to support data flowing the other way: the form components deep in the hierarchy need to update the state in FilterableProductTable.

### And That’s It
Hopefully, this gives you an idea of how to think about building components and applications with React. While it may be a little more typing than you’re used to, remember that code is read far more than it’s written, and it’s less difficult to read this modular, explicit code. As you start to build large libraries of components, you’ll appreciate this explicitness and modularity, and with code reuse, your lines of code will start to shrink. :)