# What Is Node.js?

Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine. Or inother words its: 'an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.'

> you may also ask your self What is "The V8 engine"??
it is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers

> simply you can say: Node.js is JavaScript runtime


# What Is Node.js Used For?
simply it can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking...
& 4sure 'running JavaScript on the server!'

## The Node.js Execution Model:

In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations (for example, interacting with a database) block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result. If new requests come in while this is happening, the server will spawn new threads to deal with them. This is potentially inefficient, as a large number of threads can cause a system to become sluggish — and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers, Node.js, however, is single-threaded. It’s also **event-driven**, which means that everything that happens in Node is in reaction to an event!
 Node also uses the **libuv** library to implement this asynchronous (that is, non-blocking) behavior.

![cap](https://github.com/3madov-77/Reading-Notes/blob/master/Resorses/301capture05-1.png?raw=true)

## How To Install:
go ahed & check which version you have installed on your system, type `npm -v`
you may get somthing like: v12.14.1
if you dont, lets start by:

<br>

1. ### Installing a Package Globally:

by typing `npm install -g jshint` in your terminal, This will install the jshint package globally on your system. We can use it to lint the `.js` files;
or what about

<br>

2. ### Installing a Package Locally:
We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory. Next type: `npm init -y` This will create and auto-populate a package.json file in the same folder. Next, use npm to install the lodash package and save it as a project dependency:
`npm install lodash --save`

perfect! :D
you can now start coding your node.js' file by: Create a file named 'test.js' and add the following:
```
const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];
console.log(_.compact(arr));
```
then run the script using node test.js

You should see [ 1, 2, 3 ] output to the terminal..

<br>
<hr>

## Start With “Hello, World! ^_^”:
Let’s have a quick look at a “Hello, World!” example HTTP server:
```
const http = require('http');

http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);

console.log('Server running on http://localhost:3000');
```
To run this, copy the code into a file named ***hello-world-server.js*** and run it using `node hello-world-server.js`
Open up a browser and navigate to `http://localhost:3000` to see “Hello, World!” displayed in the browser.

so first We started by requiring **Node’s native HTTP module**
then use its createServer method to create a new web server object, to which we pass an anonymous function. This function will be invoked for every new connection that’s made to the server...
The anonymous function is called with two arguments `(request and response)`, These contain the request from the user and the response, which we use to send back a 200 HTTP status code, along with our **“Hello World!”** message
& Finally, we tell the server to listen for incoming requests on **port 3000**, and output a message to the terminal to let us know it’s running.
Obviously, there’s a lot more to creating even a simple server in Node (for example, it’s important to handle errors correctly), so I’d advise you to check the documentation or consult our tutorial if you’d like to find out more...

<br>

## What Kind of Apps Is Node.js Suited To?
Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else. It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded.

And it doesn’t stop at the server. There are many other exciting and varied uses of Node.js!
For example it can be used as a scripting language to automate repetitive or error prone tasks on your PC. It can also be used to write your own command line tool, such as this Yeoman-Style generator to scaffold out new projects.
Node.js can also can be used to build cross-platform desktop apps and even to create your own robots. What’s not to love?? ^-^


<br>
<br>
<hr>