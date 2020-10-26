# Asynchronous Actions

- Every time an action was dispatched, the state was updated immediately.
- When you call an asynchronous API, there are two crucial moments in time:  
 *the moment you start the call*, and *the moment when you receive an answer* .

- Each of these two moments usually require a change in the application state; to do that, you need to dispatch normal actions that will be processed by reducers synchronously.
- Usually, for any API request you'll want to dispatch at least three different kinds of actions:

- An action informing the reducers that the request began.
  - The reducers may handle this action by toggling an isFetching flag in the state. This way the UI knows it's time to show a spinner.

- An action informing the reducers that the request finished successfully.
  - The reducers may handle this action by merging the new data into the state they manage and resetting isFetching. The UI would hide the spinner, and display the fetched data.

- An action informing the reducers that the request failed.
  - The reducers may handle this action by resetting isFetching. Additionally, some reducers may want to store the error message so the UI can display it.

## Thunking for Data

- **Thunk**is middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met.
- Using Redux actions to connect to remote APIs via Thunk Middleware.
- **Thunk** will inspects every dispatched action and then either lets it go through (in the case of a normal action that returns an object) or it processes the function and then dispatches what that function returns.
- In Redux, middleware is implemented as a curried function that ultimately evaluates the action and determines whether it’s a function or not. If so, it gets invoked with the store’s dispatch() and getState() methods. Otherwise (a normal action creator), it simply runs your action.
- **Thunk** provides more stability and error checking for us.
