# Component Composition

- React's composition model we use it for example to re-use component code is tabs which show different content when selected. This guide will start with a set of tabs that re-use no code whatsoever and build specialized components, container components, and a combination of both to achieve re-use through composition.

- All React components have a special children prop so that consumers can pass components directly by nesting them inside the jsx. This prop can be used by a tab content component to accept the actual content without needing to know anything else about it.

## Containment

- Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.  

## Specialization

- Sometimes we think about components as being “special cases” of other components. For example, we might say that a WelcomeDialog is a special case of Dialog.

## Inheritance

- Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. Remember that components may accept arbitrary props, including primitive values, React elements, or functions.

- If you want to reuse non-UI functionality between components, we suggest extracting it into a separate JavaScript module. The components may import it and use that function, object, or a class, without extending it.

## discusion

- Can a parent component access the state of a child component?

  - By declaring a **ref** in the parent component and then pass it as a ref attribute to the child

- What can be passed along in a prop variable?

  - Props pass data from one component to another. This data is **read-only**, meaning that data coming from a parent is not changed by child components.

- How can a child component “know” the state of another component?
  - A child component can "know" the state of another component if a parent passed the same set of props to multiple child components?git

## Vocabulary

- **component props** - Props, short for **properties** is a key word that functions to pass data from one component to another. They are passed in a uni-directional flow, meaning one way from parent to child. This data is read-only and does not change when passed to a child component.

- **component state** - State is an object that determines now a component renders and behaves. It is what allows creation of components that are dynamic and interactive. An example of state would be water vs ice. They are the same thing, but have a different state depending upon the temperature.

- **application state** - State is the interface between data from any kind of backend and the representation of the data with UI-elements in the frontend. State is able to keep the data of different components in sync because each state update with rerender all relevant components.
