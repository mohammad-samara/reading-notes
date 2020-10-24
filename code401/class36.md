# Application State with Redux

- Redux is a predictable state container for JavaScript apps.
- It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test
- You can use Redux together with React, or with any other view library

## Installation

`npm install redux`

## Should You Use Redux

Redux is a valuable tool for organizing your state, but you should also consider whether it's appropriate for your situation.

- Here are some suggestions on when it makes sense to use Redux:

- You have reasonable amounts of data changing over time
- You need a single source of truth for your state
- You find that keeping all your state in a top-level component is no longer sufficient

## Where is redux state stored

- The state in Redux is stored in memory, in the Redux store. This means that, if you refresh the page, that state gets wiped out.
- The state in redux is just a variable that persists in memory because it is referenced (via closure) by all redux functions .

## How do I manage a state in Redux

- *State management in ReactJS using Redux library*

- Store: all our data will keep here.
- Actions: they let us to send our data to Redux. ...
- Dispatch: it is a redux API that runs our actions. ...
- Reducers: they are just pure javascript functions that accept actions as their argument and decide what to save in - - - store when an action is sent to them.
