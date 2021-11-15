# Socket.io

* **Observer Pattern** : is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.
* **Listener** : event listeners are just like event handlers, except that you can assign as many event listeners as you like to a particular event on particular element.
* **Event Handler** : is a piece of code that will execute to respond to that event.

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


## Web Sockets
Socket.IO is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js. Both components have a nearly identical API. Like Node.js, it is event-driven.
####
Socket.IO primarily uses the WebSocket protocol with polling as a fallback option,while providing the same interface. Although it can be used as simply a wrapper for WebSocket, it provides many more features, including broadcasting to multiple sockets, storing data associated with each client, and asynchronous I/O.

## Socket.io vs Web Sockets

WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011, and the WebSocket API in Web IDL is being standardized by the W3C.

WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they are different, RFC 6455 states that WebSocket "is designed to work over HTTP ports 443 and 80 as well as to support HTTP proxies and intermediaries," thus making it compatible with HTTP. To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header[1] to change from the HTTP protocol to the WebSocket protocol.
###
There are few common misconceptions regarding WebSocket and Socket.IO:

- The first misconception is that using Socket.IO is significantly easier than using WebSocket which doesn't seem to be the case. See examples below.

- The second misconception is that WebSocket is not widely supported in the browsers. See below for more info.

- The third misconception is that Socket.IO downgrades the connection as a fallback on older browsers. It actually assumes that the browser is old and starts an AJAX connection to the server, that gets later upgraded on browsers supporting WebSocket, after some traffic is exchanged. See below for details.
