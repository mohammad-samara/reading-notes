
# Express

Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

## Express Middleware

- series of functions that the request “goes through”
- Each function receives request, response and next as parameters
- Types of middleware: *Application* and *Route*
  - **Application Middleware**
    - Error Handling
      - Bringing in other routes
      - Applies Defaults
      - JSON, Body and Form Parsing
      - Runs on every request
    - **Route Middleware**
      - Dealing with specific things for a route
      - Generally, things many routes would participate in

#### PUT VS PATCH

PUT = replace the ENTIRE RESOURCE with the new representation provided (no mention of related resources in the spec from what i can see)
PATCH = replace parts of the source resource with the values provided AND|OR other parts of the resource are updated that you havent provided (timestamps) AND|OR updating the resource effects other resources (relationships)

#### HTTP Status Codes

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error

#### 3 services or tools that allow you to “mock” an API for development

- [Wiremock](http://wiremock.org/)
- [Mocky.io](https://designer.mocky.io/)
- [Mockoon](https://mockoon.com/)

#### Compare and contrast SOAP and ReST

- SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.
- SOAP is a protocol whereas REST is an architectural pattern.
- SOAP uses service interfaces to expose its functionality to client applications while REST uses Uniform Service locators to access to the components on the hardware device.
- SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.
- SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.
- SOAP cannot make use of REST whereas REST can make use of SOAP.

### Vocabulary Terms

- SOAP : Simple Object Access Protocol.
- ReST Verbs : POST, GET, PUT, PATCH, and DELETE.
- CRUD Verbs : create, read, update, and delete.
- Swagger : Swagger is in essence an Interface Description Language for describing RESTful APIs expressed using JSON. Swagger is used together with a set of open-source software tools to design, build, document, and use RESTful web services. Swagger includes automated documentation, code generation (into many programming languages), and test-case generation.
