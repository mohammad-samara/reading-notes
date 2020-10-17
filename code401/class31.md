# Hooks

## What is a Hook

- A `Hook` is a special function that lets you “hook into” React features.
- `Hooks` are JavaScript functions, but they impose additional rules:

- Hooks must be named with a use prefix (i.e. useFishingPole)
- Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
- Only call Hooks from React function components.

- React hooks allow to to easily create and manage state in a functional component.

## hen would I use a Hook

- If you write a function component and realize you need to add some state to it.
- previously you had to convert it to a class. Now you can use a Hook inside the existing function component.

## How does it work

- by convention, we use set + state-variable to name this function useState() takes a single param, which is the initial value to assign to the state variable
- `useState()` Returns a stateVariable and setterFunction for you to use to manage state in a functional component.
