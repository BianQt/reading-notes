# HTTP Response Codes for CRUD

Most people familiar with web technology should know codes like a 200 Success or 404 Not Found. That's great; you can get a really long way in API development with just those codes alone. However, many other response codes can give a little more context back to the requester. This article will talk a little bit more about what types of codes should be sent for success and failure from CRUD endpoints in an API.

## Response Codes
### 200 Success
The requester has made a request in which it expects the API to return some data. The API has located/constructed the data and returned it as the body of the response. This is the most common success response and some API’s use only this code to signify success.
### 201 Created
This is the most appropriate response to return when there has been a request to create a new item. This signifies to the requester that their request was not only successful but there has been an item created for use later.
### 202 Accepted
It is used to signify to the requester that their request has been received; however, the response back is not the data they requested. It’s only an indication that the processing for their data has started. This can be appropriate for longer running processes or processes when the endpoint returns the data in an alternate format, e.g., inserting directly to a database or sending an email when the processing is complete.
### 204 No Content
This response is useful to indicate that the request was successful; however, there is no data returned in the response. This is often used to indicate that a resource was successfully deleted, and the API wants to confirm that with the requester but not actually return and response body.
### 206 Partial Content
This response is generally returned by a read operation when the response's body is too large to fit into a single response. This often signifies that paging has been applied and that the requester will have to apply this logic to their requests to get the rest of the data.
400 Bad Request
When the API has trouble parsing the request or if the request was malformed in some way, then it is common to return this response.
### 403 Forbidden
This is one way to signify to the requester that they need to be authorised before attempting to request this resource. There are security implications here, as information can be leaked by returning this for some resource ID’s but then 404’s for others. I suggest you either return all 403’s when the appropriate authorisation hasn't been supplied or return 404’s always as your standard error.
### 404 Not Found
This is the appropriate response when a resource ID has been passed to the API it cannot locate (or, as mentioned above, won't locate).
405 Method Not Allowed
This code signifies that the HTTP method was inappropriate for this endpoint. For example, the client used GET on a POST only endpoint.
### 409 Conflict
This tells the requester that they have tried to create a resource that already exists. There are a few other niche cases where the most appropriate response is a 409. This could be when the request contradicts itself, with the endpoint ID and the request ID not matching in an update request. However, these could also be described as malformed requests, and a 400 can be returned.
### 500 Internal Server Error
If the API server suffered an internal error, it should return this as it lets the client know it is not their fault, and they should probably contact the API owner.
### 501 Not Implemented
This code is used to say that the requested endpoint/method has not been implemented. It often signifies that the API intends to introduce this later, but currently, it cannot be used. I often use them as my standard response when building out an API. It's useful during CI/testing as I know it doesn't mean my code was bad… it's just I haven't written the code for that endpoint yet.
