# Express Routing & Connected API

## Routing

- refers to how an application’s endpoints (URIs) respond to client requests.
- These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method.

## Route methods

- A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

## Route paths

- in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.
- The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.

## Route parameters

- Route parameters are named URL segments that are used to capture the values specified at their position in the URL. 

## Route handlers

- You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks.

## Response methods

- The methods on the response object (res) in the following table can send a response to the client, and terminate the request-response cycle. If none of these methods are called from a route handler, the client request will be left hanging.

## app.route()

- You can create chainable route handlers for a route path by using app.route(). Because the path is specified at a single location, creating modular routes is helpful, as is reducing redundancy and typos.

## express.Router

- Use the express.Router class to create modular, mountable route handlers. A Router instance is a complete middleware and routing system; for this reason, it is often referred to as a “mini-app”.

## express routing

### Express Router

- It is a mini express application without all the bells and whistles of an express application, just the routing stuff.

### Route Middleware router.use()

- Express is a way to do something before a request is processed.