# Review, Research, and Discussion

1. array.map()  
creates a new array with the results of calling a function for every array element.

2. array.reduce()
  - executes a reducer function (that you provide) on each element of the array, resulting in single output value.
  - Your reducer function's returned value is assigned to the accumulator, whose value is remembered across each iteration throughout the array, and ultimately becomes the final, single resulting value.

3. superagent()
to fetch data from a URL (usually to get data from an API).  
### code snippets for using superagent:

#### With normal Promise .then() syntax
```
let allCharactersObj = {};
  superagent.get(`https://swapi.dev/api/people/`).then(data =>{
    //console.log(data.body.results);
    data.body.results.forEach(person =>{allCharactersObj[person.name]= person.url});
    console.log(allCharactersObj);
  });
```
#### with async / await syntax
```
async function cityGeo(city) {
  let results = await superagent.get(`https://geocode.xyz/${city}?json=1`);
  console.log(`longitude : ${results.body.longt}`);
  console.log(`latitude : ${results.body.latt}`);
}
```

# promises
Promises are one way to manage Asynchronous actions. Like a callback, a promise allows you to execute some code and “move on”, allowing for that code to take as long as it needs to run then when it finish processeing we use `.then()` to process the data that the promise outputed . Unlike a callback, the syntax of a promise feels and reads a bit more “inline”.

#  callback functions
When a function simply accepts another function as an argument, this contained function is known as a callback function  
  - Are all callback functions considered to be Asynchronous?  No, because some callback functions does not need time to excute code within like a callback function that performs simple math operations without the need to fetch data from any outer resources, so javascript will run them synchronously because they procces data immediately.

# Node.js
is a JavaScript runtime built on Chrome’s V8 JavaScript engine , that lets you run your javascript code out of the browser which allows you to use javascript on servers.  
it is used to generate dynamic page content, to (create, open, read, write, delete, and close) files on the server, collect form data , and (add, delete, modify) data in your database.

# npm
NPM is an online repository that allows the publishing and sharing of open-source Node.JS projects and its a command line utility for interacting with those repositories, and it helps in the installation, version management and depenedency management.  
the most uses of npm are to adapt packages of code for your apps, or incorporate packages as they are, and to download standalone tools you can use right away.