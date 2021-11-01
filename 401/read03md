# Express REST API

## Review, Research, and Discussion

* Name 3 real world use cases where you’d want to change the request with custom middleware
    - Authentication
    - Async Actions
    - Routing 
###
* True or false: The route handler is middleware?
   - False, Middleware functions are functions that take an extra argument, ```next``` along with ```req``` and ```res``` which is used to invoke the next middleware function.
```app.use()``` and the other HTTP derived methods(```app.get()```, ```app.all()``` etc) can use middleware functions. The difference between handler function and middleware function is same on both app and router object.
       ###
     On the other hand, a handler function is a function that is specified by the routing methods. So when any of the routing methods pass a function that has ```req```, ```res```, and ```next``` then it is both a middleware function and a handler function.

* In what ways can a middleware function end the process and send data to the browser?
   - By not calling ```next()``` and ends the request-response by calling ```res.end```, ```res.send```, etc

* At what point in the request lifecycle can you “inject” middleware?
  - In the Calling function/Handler function
* What can cause express to error with “Request headers sent twice, cannot start a second response”
  - "Error :Can't set headers after they are sent." means that some function tried to set a header or statusCode after you're already in the Finished state.

####
## Vocabulary Terms
|  Term  | Description   |
| ----------- | ----------- |
|   Middleware |  A function that has access to the request object (req), the response object (res), and the next function in the application’s request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.    |
|   Request Object |  The req object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on.    |
|   Response Object |  The response object contains the request response value along with various HTTP headers and flags. When a lifecycle method returns a value, the value is wrapped in a response object along with some default flags (e.g. 200 status code).   |
|  Application Middleware |  A global Middleware will run on every HTTP request of the application    |
|  Routing Middleware |  A  Middleware assigned to a specific route   |
|  Test Driven Development | (TDD) is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.    |
|  Behavioral Testing |  Is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing.   |

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  - Express
  - HTTP methods
  - Request Response Cycle

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - Middlewares
  - Testing
  - Request/Response methods

What are you most excited about trying to implement or see how it works?
  - Data Structure
  - Authentication
  - SQL Databases