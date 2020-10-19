# Context API

- `React Context API` is a way to essentially create global variables that can be passed around in a React app.
- Context provides a way to pass data through the component tree without having to pass props down manually at every level.

## When to Use Context

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

- *The React team suggests to stick to props if you have just a few levels of children to pass, because it’s still a much less complicated API than the Context API.*

## How does it work

- You create a context using React.createContext(), which returns a Context object.:

```
const { Provider, Consumer } = React.createContext()
```

- Then you create a wrapper component that returns a Provider component, and you add as children all the components from which you want to access the context.

- Inside a component that’s wrapped in a Provider, you use a Consumer component to make use of the context.
- You can also pass functions into a Provider value, and those functions will be used by the Consumer to update the context state.
- When using multiple files, you create the content in one file, and import it in all the places you use it.
