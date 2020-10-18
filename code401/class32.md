# Custom Hooks

- What are custom hooks?

  - Extract duplicated logic from components

  - Share common functionality

    - But not State

  - Takes advantage of useEffect lifecycle

- Common use cases - make things DRY

  - Handle forms easily

  - Pre-fetch API data

  - Connect to services (like socket.io, Q, etc.)

  *Unlike a React component, a custom Hook doesn’t need to have a specific signature. We can decide what it takes as arguments, and what, if anything, it should return. In other words, it’s just like a normal function. Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.*

- Here is a simple example that demonstrates proper wiring:

  - Hooks are exported as a function, named as useXXX()

  - Hooks return data or behaviors (functions) that are required to reuse their internal functionality

  - Hooks are imported into components

  - Components can re-use the hook functionality or data/state as needed

  - Hooks do not render

use-food-hook.js

```
export default function useFoodHook(hungry) {
  let food = 'cookies';
  return hungry ? food : null;
}
```

- Using a hook is as simple, then, as requiring it and calling it.

my-component.js

```
import useFeedme from 'use-food-hook.js';
function myComponent() {
  const food = useFeedMe(true);
  return <div>{food}</div>
}
```

## React Hooks with Async-Await  

- We cannot use 'async' keyword with 'useEffect' callback method. It will result in race conditions.  
- so we should fetch our data from an API then updating our 'setResult' state  
    so React.useEffect method will only run when our 'state' got change.
