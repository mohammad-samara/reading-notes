# HTTP and REST

## HTTP

HTTP stands for Hyper Text Transfer Protocol, it's a request - response protocol that is used to build different types of information systems, it's also the foundation for the world wide web.

* Applications that are built using HTTP subscribe to the client-server computing model.

* In this model, the provider of the service is called server, while the part that sends requests is called clients.

* HTTP is often associated with serving `.html` files but also can deliver images,videos,json,xml,binary executables and much more.

## HTTP Requests

* HTTP Request is formatted in text and transferred using TCP.

* First line of the request includes: `Method, URL and HTTP Version`, the following line is the request's `HEADER` which is a key value pair seperated using a colon like objects in JS, and lastly an optional body.

* Methods include: GET,HEAD,POST,PUT,DELETE,CONNECT,PATCH etc...

* Some methods are `safe` methods and should only be used for informational retrieval and doesn't change the server state, `Cacheable` means the client should be able to catch the response.

## HTTP Response

* It's also formatted same as requests but the first line contains `HTTP VERSION,STATUS CODE and STATUS MESSAGE` and then it provides the request headers exactly like in the request, also provides an optional body.

## REST

* REST is an acronym for REpresentational State Transfer, and it's a way we can reference,manipulate and transfer state.

* RESTful Endpoint: is a URI (Uniform Resource Identifier) that indentifies the resource that when addressed with a proper method, you can effect state (performing CRUD operations over HTTP).

## REST Documenation (Swagger)

* Open API (Formerlly swagger) is the standard for documenting REST API's and it's a live documentatio system.

* It provides data on how to see the API and how to use it.

* You can generate your own swagger documentation using Swagger inspector and then using all the REST endpoint and data and then select the routes you want to create the documentation for then click "Create API Definition".

