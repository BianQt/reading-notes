# Authentication
## Review, Research, and Discussion

* Explain what a “Singleton” is (in Computer Science terms)
  - Is an object which can only be instantiated one time
* Explain how the Singleton pattern can be used with Node modules, specifically with classes
  - Using ES6, you can represent a singleton using ES Modules 
* If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
  - I will create a global Middleware to run on every HTTP request of the application and Routing Middleware to test a specific route
## Vocabulary Terms

* **Router Middleware** : A  Middleware assigned to a specific route.
* **Dynamic Module Loading** : Is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.
* **Singleton Pattern** : Is a software design pattern that restricts the instantiation of a class to one "single" instance.
* **CRUD ** : Create, Read, Update, and Delete (CRUD) are the four basic functions that models should be able to do, at most.
* **Mock Testing** : Testing a fake version of an external or internal service that can stand in for the real one.
## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  - ES6 Classes
  - Testing

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - PostgreSQL
  - Data Modeling

* What are you most excited about trying to implement or see how it works?
  - Data Structures
  - Authentication
  - SQL Databases

## Preparation Materials
### Securing Passwords
Passwords are the first line of defense against cyber criminals. There are many ways to secure the passwords such as bycrption , hashing, salting ..etc.

#### Hashing
Hashing is a type of algorithm which takes any size of data and turns it into a fixed-length of data. This is often used to ease the retrieval of data as you can shorten large amounts of data to a shorter string (which is easier to compare).

### Basic Auth
Authentication is the process of verifying that an individual, entity or website is whom it claims to be. 
#### How does authentication work?
During authentication, credentials provided by the user are compared to those on file in a database of authorized users' information either on the local operating system server or through an authentication server. If the credentials entered match those on file and the authenticated entity is authorized to use the resource, the user is granted access. User permissions determine which resources the user gains access to and also any other access rights that are linked to the user, such as during which hours the user can access the resource and how much of the resource the user is allowed to consume.
###
However, the web's application protocols -- Hypertext Transfer Protocol and HTTP Secure -- are stateless, meaning that strict authentication would require end users to reauthenticate each time they access a resource using HTTPS. To simplify user authentication for web applications, the authenticating system issues a signed authentication token to the end-user application; that token is appended to every request from the client. This means that users do not have to sign on every time they use a web application.

### bcrypt docs
A library to help you hash passwords.
#### Install via NPM
```npm install bcrypt```

#### Usage
```const bcrypt = require('bcrypt');
const saltRounds = 10;
const myPlaintextPassword = 's0/\/\P4$$w0rD';
const someOtherPlaintextPassword = 'not_bacon';
```

#### To hash a password:
```
bcrypt.genSalt(saltRounds, function(err, salt) {
    bcrypt.hash(myPlaintextPassword, salt, function(err, hash) {
        // Store hash in your password DB.
    });
});
```
#### To check a password:
```
// Load hash from your password DB.
bcrypt.compare(myPlaintextPassword, hash, function(err, result) {
    // result == true
});
bcrypt.compare(someOtherPlaintextPassword, hash, function(err, result) {
    // result == false
});
```