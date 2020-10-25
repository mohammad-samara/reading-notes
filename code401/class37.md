# Combined Reducers

## Combined-Reducers

- As your app grows more complex, you'll want to split your **reducing function** into separate functions, each managing independent parts of the **state**.

- The `combineReducers` helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`.

- The resulting reducer calls every child reducer, and gathers their results into a single state object. 
- **The state produced by `combineReducers()` namespaces the states of each reducer under their keys as passed to `combineReducers()`**

- You can control state key names by using different keys for the reducers in the passed object. 
  - For example, you may call `combineReducers({ todos: myTodosReducer, counter: myCounterReducer })` for the state shape to be `{ todos, counter }`

- Each reducer technically has it’s own actions and creators.
- However, they can cross over and both be dispatched.
- This can be` very powerful, as often times actions are valid for multiple reducers