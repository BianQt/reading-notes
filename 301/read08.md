# APIs
API stands for Application Programming Interface.
* A Web API is an application programming interface for the Web.
* A Browser API can extend the functionality of a web browser.
* A Server API can extend the functionality of a web server.

# REST
 REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP.

## Define API operations in terms of HTTP methods
The HTTP protocol defines a number of methods that assign semantic meaning to a request. The common HTTP methods used by most RESTful web APIs are:

* **GET** retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
* **POST** creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.
* **PUT** either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
* **PATCH** performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
* **DELETE** removes the resource at the specified URI.

## HTTP response status codes
HTTP response status codes indicate whether a specific HTTP request has been successfully completed. Responses are grouped in five classes:

* **Informational responses** (100–199)
* **Successful responses** (200–299)
* **Redirects** (300–399)
* **Client errors** (400–499)
* **Server errors** (500–599)