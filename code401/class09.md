# API Server

## Joining Data/Documents in Mongo

- `populate()` is a method we can use in Mongoose to connect 2 collections
- `pre('find')` you do a collection “on the fly” which can be more efficient than storing the relation.

## Middleware

- also called `pre and post hooks`
- are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.

## Types of Middleware

- **Mongoose has 4 types of middleware:**
  - 1. document middleware
    - is supported for the following document functions. In document middleware functions, this refers to the document.
  - 2. model middleware
    - is supported for the following model functions. In model middleware functions, `this` refers to the model.
  - 3. aggregate middleware
    - is for `MyModel.aggregate()`.
    - executes when you call `exec()` on an aggregate object.
      - `this` refers to the aggregation object.
  - 4. query middleware.
    - is supported for the following Model and Query functions. In query middleware functions, `this` refers to the query.

### Pre middleware functions

- are executed one after another, when each middleware calls next.

### post middleware

- are executed after the hooked method and all of its pre middleware have completed.

## Subdocuments

- are documents embedded in other documents.
- In Mongoose, this means you can nest schemas in other schemas.
- Mongoose has two distinct notions of subdocuments: *arrays of subdocuments* and *single nested subdocuments*.

### What is a Subdocument

- are similar to normal documents. Nested schemas can have middleware, custom validation logic, virtuals, and any other feature top-level schemas can use.
- **The major difference** is that subdocuments are not saved individually, they are saved whenever their top-level parent document is saved.
