### Hi everyone. My name Is Mohammad Samara, and I will share with you what I have learned about **Operators and Loops in JavaScript**

#### Comparison operators:
evaluating conditions

- you can evaluate a situation by comparing one value in the script to what you expect it might be. the result will be a Boolean: *true or false*

* (==) : is equal to
   * compares between two values(numbers, strings, or booleans) to see if they are the same
* (===) : strict equal to
   * compares to values to check that both the data type and value are the same
* (!=) : is not equal to
   * compares between two values(numbers, strings, or booleans) to see if they are not the same
* (!==) : strict not equal to
   * compares to values to check that both the data type or the value are not the same
* (>) : greater than
   * checks if the number on the left is greater than the number on the right
* (<) : less than
   * checks if the number on the left is less than the number on the right
* (>=) greater than or equal to
   * checks if the number on the left is greater than or equal to the number on the right
* (<=) : less than or equal to
   * checks if the number on the left is less than or equal to the number on the right

------------------------------------------
#### Logical Operators

Comparison operators usually return single values of **true** or **false**, logical operators allow you to compare the results of more than one comparison operator.

![image of logical operator sentence](/images/javascript2/logical.png)



1. logical and (&&) : if both expressions evaluate to true then the expression returns true. if just one of these returns false, then the expression will return false.
2. logical or (||) : if either expression evaluates to true, then the expression returns true. if both false, then the expression will return false.
3. logical not (!) : reverses the state of an expression. if it was false (without the ! before it) it would return true. if the statement was true, it would return false>

![image of T-F table](https://1.bp.blogspot.com/-E3z93RXYCGc/XfXd0T8x3FI/AAAAAAAAE04/zNAwwEov8cw-t353RBQ4rAq59znfY0C5QCLcBGAsYHQ/s1600/Screenshot%2B%2528455%2529.png)

----------------------------------------------------------------------------------------------------------------

## loops 

loops check a condition. if it returns true, a code block will run, then the condition will be checked again and if it still return true, the block code will run again. it repeats until the condition returns false.

1. **for**: if you need to run code a specific number of times, use a *for* loop, in a *for loop*, the condition is usually a **counter** which is used to tell how many times the loop should run.

![image of logical operator sentence](/images/javascript2/for-statement.png)

   * a ***for* loop uses a *counter* as a condition**
   this instructs the code to run a specific number of times
   **the condition in the *for loop* is made up of three statements:**
     - initializing : create a variable and set it to 0 (or any value you want) (var i =0;)
     - condition : the loop should continue to run untill the counter reaches a specific number. EX: (i <10 ;)
     - update : every time the loop run the statement in the curly braces, it adds one (or any value you choose) to the counter



2. **while** : if you don't know how many times the code should run, you can use a *while* loop, and the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true.



3. **do while** : very similar to *while loop*, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.



you can find more about logical loops at the click me below:

[click me](https://www.freecodecamp.org/news/the-complete-guide-to-loops-in-javascript-f5e242921d8c/)








