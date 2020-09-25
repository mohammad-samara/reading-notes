# Event Driven Applications

- Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

## concepts of the Event-Driven Programming

- An Event Handler is a callback function that will be called when an event is triggered.
- A Main Loop listens for event triggers and calls the associated event handler for that event.

## Emitting Events

- EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away.
- In node.js an event can be described as a string with a corresponding callback.
- An event can be “emitted” multiple times, we can choose to only listen for the first time event is emitted.
- The EventEmitter class is defined and exposed by the events module:  
`const EventEmitter = require('events').EventEmitter;`

## Removing Listeners

- To remove event listeners in EventEmitter we can use the *removeListener* or *removeAllListeners* method.
- It’s important to note that in the EventEmitter that comes built-in with Node you must pass a reference to the exact function you wish to remove when using the removeListener method.

## Object Oriented Programming + Event-Driven Programming

- These two make for a very valuable combination in a wide variety of situations and I think it can be beneficial to understand and conceptualize why.
