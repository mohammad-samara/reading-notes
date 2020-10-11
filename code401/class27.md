# React

## setState

- Update to a component state should be done using setState()
- You can pass an object or a function to setState()
- Pass a function when you can to update state multiple times
- Do not depend on this.state immediately after calling setState() and make use of the updater function instead.

## Handling Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

## discussion

- Does a deployed React application require a server?

  - No. React applications build a virtual DOM and performs operations on the client's browser

- Why do we prefer to test a React application at the behavior rather than the unit level?

  - BDD is preferred because the system itself does not evolve due to the framework, so the end goal of the test is always to confirm that a certain behavior takes place. The output must be correct under a given condition, but it does not matter how the output is generated.

- What does `npm run build` do?

  - npm run build creates a **build** directory with a production build of the application.
  - This creates Javascript and CSS files inside a build/static directory

- Describe the actual composition / architecture of a React application
  - React is a view that caters to the user interface. It doesn't enforce an architecture. React comprises of components that may or may not hold state, or data needed to track for making an application work

### Vocabulary

- **BDD** - Behavior Driven Development. Different than Test Driven Development (Unit Testing) in that it tests the actual behavior of the system the end users perspective rather than checking the implementation of functionality.
- BDD is also a test-first approach

- **Acceptance Tests** - Testing to determine whether the software system has met the requirement specifications. Evaluating the system's compliance with business requirements.

- **mounting** - Process of outputting a virtual representation of a component to the final UI representation. For instance, outputting a React Element into the DOM element or DOM tree. This is important because one can only be sure a component is output/rendered when it is mounted.

- **build** - Creating a build directory with a production build of an application

## React Testing  

  There are a few ways to test React components. Broadly, they divide into two categories:  

   1. Rendering component trees  
     - in a simplified test environment and asserting on their output.  
   2. Running a complete app  
     - in a realistic browser environment (also known as “end-to-end” tests).  

## React testing approaches  

- Snapshots  
- Render Testing  
- Shallow Testing  
- Mounting