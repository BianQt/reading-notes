# Bearer Authorization
## Review, Research, and Discussion

* Write the following steps in the correct order:
   - Register your application to get a client_id and client_secret
   - Ask the client if they want to sign in via a third party
   - Redirect to a third party authentication endpoint
   - Receive access token
   - Make a request to the access token endpoint
   - Receive authorization code
   - Make a request to a third-party API endpoint
* What can you do with an authorization code?
* What can you do with an access token?
 - make API requests on behalf of a user
* What’s a benefit of using OAuth instead of your own basic authentication?
 - It's More secure!

## Vocabulary Terms

* Client ID : is a public identifier for apps
* Client Secret : is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors.
* Authentication Endpoint : is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.
* Access Token Endpoint : is used by the application in order to get an access token or a refresh token.
* API Endpoint :  is a point at which an API -- the code that allows two software programs to communicate with each other -- connects with the software program.

* Authorization Code : is a temporary code that the client will exchange for an access token. 
* Access Tokens : are the thing that applications use to make API requests on behalf of a user.

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  - Authentication
  - Authentication-Testing

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - JWT
  - Authentication - Testing

* What are you most excited about trying to implement or see how it works?
  - Data Structures
  - Authentication
  - SQL Databases


## Preparation Materials

### JWTs
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

* JSON Web Tokens uses
  - Authorization
  - Information Exchange

* JSON Web Token structure
 - Header
 ```
 {
  "alg": "HS256",
  "typ": "JWT"
}
```
 - Payload
```
 {
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```
 - Signature
```
 HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
  ```