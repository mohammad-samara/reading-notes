# Routing

* **react-router**: React Router is the standard routing library for React.
* React Router keeps your UI in sync with the URL.
* **react-router** allows you to toggle the visibility of components (or even pages) based on the URL/Route that the user engages with
* `import { Route } from 'react-router-dom';`
* for routing in react we use the built-in tag `<Link>` instead of `<a>`.

* `React Router` does is conditionally render certain components to display depending on the route being used in the URL (/ for the home page, /about for the about page, etc...).
* To use React Router, you first have to install it using NPM:

```
npm install react-router-dom
```

* Also we need to `import { Route } from 'react-router-dom';`

* To tell the <Route> tags which component to load, simply add a path attribute and the name of the component you want to load with component attribute.

 ```
 <Route path='/' component={Home} />
 ```

## hooks

React Router ships with a few hooks that let you access the state of the router and perform navigation from inside your components

* useHistory : The useHistory hook gives you access to the history instance that you may use to navigate.
* useLocation : The useLocation hook returns the location object that represents the current URL
* useParams
useParams returns an object of key/value pairs of URL parameters. Use it to access match.params of the current <Route>.
* useRouteMatch
The useRouteMatch hook attempts to match the current URL in the same way that a <Route> would

