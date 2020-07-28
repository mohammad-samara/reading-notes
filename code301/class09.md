# Concepts of Functional Programming in Javascript

**What is functional programming?**  
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

## pure functions

1. It returns the same result if given the same arguments (it is also referred as deterministic)
2. It does not cause any observable side effects

## Immutability
>>> Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.  

>>>Basically, if a function consistently yields the same result for the same input, it is referentially transparent.  

**pure functions + immutable data = referential transparency**

# Higher-order functions

### Filter
Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.


### Map
The idea of map is to transform a collection.
The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.

### Reduce
The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

