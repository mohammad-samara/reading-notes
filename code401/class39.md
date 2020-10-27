# redux-additional topics

## Redux Toolkit "RTK"

a package for making stores, which was created by the creators of Redux (the Redux Team), and intended to be the standard way to write Redux logic

* To add the package `npm install @reduxjs/toolkit`.
* Includes utilities to simplify common use cases like store setup, creating reducers, immutable update logic, and more.
* **Toolkit** specifies a few different means of building a reducer and action set that work well together and are easier to understand and integrate.
* We can replace the plain Redux createStore function with RTK's configureStore. This will automatically set up the Redux DevTools Extension for us.

## Redux Reducer Bundles

The reducer/actions pair that ever needs their associated actions, it makes more sense for these pieces to be bundled together in an isolated module that is self contained, and can even be packaged easily into a library.

## Hookstate

Is a modern alternative to Redux, Mobx, Formik without boilerplate, it is simple but incredibly fast and flexible state management that is based on React state hook.

## MobX

* **MobX** is a simple, scalable and battle tested state management solution.
* it is a standalone library, but most people are using it with React.
* `The core idea`
  * State is the heart of each application and there is no quicker way to create buggy, unmanageable applications than by producing an inconsistent state or state that is out-of-sync with local variables that linger around.
* **MobX** makes state management simple again by addressing the root issue:
  * it makes it impossible to produce an inconsistent state.
  * `The strategy to achieve that is simple:`
    * Make sure that everything that can be derived from the application state, will be derived.
