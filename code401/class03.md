# Class-03


- 1. Name 3 advantages to Test Driven Development
    -  spend less time in the debugger.
    - TDD reduces time spent on rework.
    - TDD supports a clean interface.
    
- 2. In what case would you need to use beforeEach() or afterEach() in a test suite?
    - beforeEach and afterEach are run before/after every it block in the current context and all nested contexts.
- 3. What is one downside of Test Driven Development
    - HUGE loss of time it takes "getting in to it".
- 4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    - The most important difference between class- and prototype-based inheritance is that a class defines a type which can be instantiated at runtime, whereas a prototype is itself an object instance.
- 5. Name a use case for a static method
    - Use a static method when you want to be able to access the method without an instance of the class. Use static when you want to provide class level access to a method.
- 6. Write an example of a Higher Order function and describe the use case it solves
      - Example 1#
       - Let’s say we have an array of numbers and we want to create a new array which contains double of each value of the first array. Let’s see how we can solve the problem with and without Higher-Order Function.
         - *Without Higher-order function*
              - const arr1 = [1, 2, 3];
              - const arr2 = [];
              - for(let i = 0; i < arr1.length; i++) {
                  - arr2.push(arr1[i] * 2);
              - }
              - // prints [ 2, 4, 6 ]
              - console.log(arr2);
         - *With Higher-order function map*
              - const arr1 = [1, 2, 3];
              - const arr2 = arr1.map(function(item) {
                  - return item * 2;
              - });
              - console.log(arr2);


## Document the following Vocabulary Terms:
  Vocabulary            |  Definition
 -----------------------|-----------------------------------------------------------------------------------------------------------
 functional programming | is the process of building software by composing pure functions, avoiding shared state, mutable data, and                                side-effects.
  pure function         | are functions that accept an input and returns a value without modifying any data outside its scope(Side Effects).
  higher-order function | is a function that can take another function as an argument, or that returns a function as a result.
  immutable state       | is state that cannot be changed. Immutable objects (for which none of the state can be changed) become important when you are dealing with concurrency, the ability for more than one processor in your computer to operate on that object at the same time.
  object                | defined as an unordered collection of related data, of primitive or reference types, in the form of “key: value” pairs.
  (OOP)                 | is a computer programming model that organizes software design around data, or objects, rather than functions and logic.
  class                 |  is a type of function. Classes are declared with the class keyword. We will use function expression syntax to initialize a function and class expression syntax to initialize a class.
  prototype             | object may also have a prototype object, which it inherits methods and properties from, and so on.
  super                 | keyword is used to access and call functions on an object's parent.
  inheritance           | is an important concept in object oriented programming. In the classical inheritance, methods from base class get copied into derived class.
  constructor           | is a special type of subroutine called to create an object. It prepares the new object for use, often accepting arguments that the constructor uses to set required member variables.
  instance              | means a reference to an “object” created by “new” or the equivalent.
  context               | is related to objects. It refers to the object to which a function belongs. When you use the JavaScript “this” keyword, it refers to the object to which function belongs.
  this                  |  keyword refers to an object, that object which is executing the current bit of javascript code.  |

# MDN this
   - A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.
   - A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value.
   - this refers to the global object whether in strict mode or not.
   - Inside a function, the value of this depends on how the function is called.

# MDN class
  - Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.
  - To declare a class, you use the class keyword with the name of the class
  - The body of a class is executed in strict mode