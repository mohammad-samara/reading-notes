# Heroku :
lets you deploy, run and manage applications written in Ruby, Node.js, Java, Python, Clojure, Scala, Go and PHP.

Heroku is a polyglot[speaking, many languages.] platform it lets you:
- build
- run
- scale applications in a similar manner across all the languages
- utilizing the dependencies and Procfile.
The Procfile exposes an architectural aspect of your application

## Deploying applications :
1. Heroku platform uses Git as the primary means for deploying applications
2. When you create an application on Heroku, it associates a new Git remote, typically named heroku, with the local Git repository for your application. $ git push heroku master

# Node.js For Beginners
First of all, we need to create a JavaScript file. Let's name it server.js:

```
http.createServer( function( request, response) {

response.writeHead( 200, {"Content-Type": "text/plain"} );

response.write( "It's alive!" );

response.end();

}).listen(3000); 
```

make sure it's working. Run at your terminal: node server.js

Let's look more closely at our first Node server. This is an example of how Node provides you with non-blocking and event-driven behavior. Let me explain:

`$.post('/some_requested_resource', function(data) { console.log(data); });`

This code performs a request for some resource
When the response comes back, an anonymous function is called. It contains the argument data, which is the data received from that request.
Node allows you to use the so-called event loop, which works faster because of non-blocking behavior.

# Heroku cloud application :

lets Create your project directory. And then create the server.js file inside of it.

then let's declare some variables:

`var http = require("http");` will give the key to Node's HTTP functionality

`var fs = require("fs");` for possibility to interact with the file system

`var path = require("path");` allows you to handle file paths

`var mime = require("mime");` allows you to determine a file's MIME-type it's not a part of Node.js

<br>

so we need to install third-party dependencies before using it. We need to create the package.json file for that purpose. It will contain project related information:


name
version
description, and so on.
For our project we will use MIME-types recognition, because it's not enough to just send the contents of a file when you use HTTP. You also need to set the Content-Type header with proper MIME-type. That's why we need this plug-in.

Create the package.json file and fill it with proper information. Here's 

run npm install It will create node_modules folder and place all the files inside of it

We will now create send 404() function. It will handle the sending of 404 error, which usually appears when requested file doesn't exist:

```
   response.writeHead(404, {"Content-type" : "text/plain"});
   response.write("Error 404: resource not found");
   response.end(); }
```
Now we will define sendPage() function. It first writes the header and then sends the contents of the file:

```
function sendPage(response, filePath, fileContents) {
   response.writeHead(200, {"Content-type" : mime.lookup(path.basename(filePath))});
   response.end(fileContents); }
```
Now we'll define how our server will handle responses. This function will return the content of the requested file or the 404 error otherwise:

```
function serverWorking(response, absPath) {
   fs.exists(absPath, function(exists) {
      if (exists) {
      fs.readFile(absPath, function(err, data) {
         if (err) { send404(response) }
         else { sendPage(response, absPath, data); } }); }
         else { send404(response); } });
         }
```
And now lets create the HTTP server:

```
var filePath = false;
if (request.url == '/') {
   filePath = "public/index.html";
   } else {
   filePath = "public" + request.url;
   }

var absPath = "./" + filePath;
serverWorking(response, absPath);
});
```


<br>
<br>
<hr>