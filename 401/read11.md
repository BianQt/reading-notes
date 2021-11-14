# Event Driven Applications

## Review, Research, and Discussion

* Why is access control important?
  - Access controls limit access to information and information processing systems

* Describe an application that would need access control.
 - Social Network Application, It has a lof of information about the user. So, the only one has to have access to these information is the user himself.
* What is a role used for?
 - User.
* Why is role based access control more scalable than discretionary or mandatory access control?
 RBAC is superior to ACL in terms of security and administrative overhead. ACL is better suited for implementing security at the individual user level and for low-level data, while RBAC better serves a company-wide security system with an overseeing administrator.
 
## Vocabulary Terms

* **Authorization** : is the process of giving someone permission to do or have something.
* **Role Based Access Control** :  is a policy-neutral access-control mechanism defined around roles and privileges.
* **Capabilities** : is the ability to execute a specified action.

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  - Authentication
  - Authentication-Testing
  - Socket io

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - Events
  - Authentication - Testing

* What are you most excited about trying to implement or see how it works?
  - Data Structures
  - Authentication
  - SQL Databases


## Preparation Materials
### Node -Events
Every action on a computer is an event. Like when a connection is made or a file is opened.

Node.js has a built-in module, called "Events", where you can create-, fire-, and listen for- your own events.

To include the built-in Events module use the require() method. In addition, all event properties and methods are an instance of an EventEmitter object. To be able to access these properties and methods, create an EventEmitter object:
```
var events = require('events');
var eventEmitter = new events.EventEmitter();
```

You can assign event handlers to your own events with the EventEmitter object.

In the example below we have created a function that will be executed when a "scream" event is fired.

To fire an event, use the emit() method.


### Event Driven Programming
Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. In this article we’re going to go over how Event-Driven Programming works and how we can make the best use of it in our Node.js projects.
###
Event-Driven Programming makes use of the following concepts:

* An Event Handler is a callback function that will be called when an event is triggered.
* A Main Loop listens for event triggers and calls the associated event handler for that event.