# advanced web development  
at this webpage I will tell you about what I have learnt today about **error handling & debugging** in **javascript**.  
## How the interrepter reads and executes the scripts:
you need first to understand the way the interrupter works to make it easier to track errors.  
**order of exrcution**  
inorder to determine where the error happens track your code from the the first syntax that runs into the next one (it will help you to use `consol log()` at the end of any tracked code block to know what are the inputs and the outputs of that code block).  
**execution contest**  
it is like the variable scoop but for code lines,and it have 3 types:  
1. global contex: when the code is not inside a function.
2. function context: when the code is inside a function.
3. eval context: text is executed like code in an internal function called `eval()`  
note that there is only one global context, and each function creates a function context.  
* any code scripts that are in the global context can be called before execution, because each time a script enters a new execution context it will be prepared(all variables and functions and arguments are created before executing any line) then the interrupter begins execution(assign values and run functions and execute statements)

**Stack**: javascript run the code line by line so when a code line requires data from another function the interepter moves to that function and stacks it on the top of the current task even if the second function lines are above the first. and once it finishes the second function it return to the first if the second function do not require any data from other functions.  

**scoop**:
each execution context creates it's own **variable object** where it stores all variables, functions and parameter within it. and each execution context can access to it's parent's variable object.  
**errors**: if the interrepter reaches a statement that have errors it will stop reading and executing the scripts and checks the current execution for ***exception-handling code***(used to know where is the problem), when it found where is the problem it will look for ***error handling code*** in the function with the problem.  
if there is not an exception-handling code in the function where error happened the interrepter will go to the line of code that called the function and search foor the exception-handling code. untill it reaches the global context ,and so if it didn't find it then it creates an **Error Object**(stores info about the error like at which line it is) that the console can read and give you the error informations.  
**Error object types**  
| object | describtion |
| ---------------|--------------- |
| Error | Generic error |
| Syntax Error | Syntax has not been followed |
| ReferenceError | used a variable that is not declared whithin the scope |
| TypeError | unexpected data type that can not be handled |
| Range Error | Numbers not in acceptable range |
| URI Error | encodeURI ().decodeURI(),and similar methods used incorrectly |
| EvalError | eval () function used incorrectly |  

**dealing with errors**: you can either debug the script or handle errors gracefully which means that you write an error-handling code which tells the interrepter to check whether something will work, and offer an alternative option if it fails (usually used for errors that does not come from the same page).

#### debug tip:
1. look at the error message to find where is the error happining and it's type.
2. use `consol.log()` to write messages to see where the execution stops
3. Use breakpoints where things are going wrong. They let you pause execution and inspect the values that are stored in variables.
4. try checking variables values and calling functions the console to test if they work as expected.
5. check if the variable or properties or the function or method do exist.
6. Check the number of parameters for a function, or the number of items in an array.
7. solve the loops and the conditional statements manually to check their functionality.  

## console methods:
* assert(): Writes an error message to the console if the assertion is false.
* error(): Outputs an error message to the console.
* group(): Creates a new inline group in the console. This indents following console messages by an additional level, until console.groupEnd() is called.
* groupEnd(): Exits the current inline group in the console.
* info(): Outputs an informational message to the console.
* log(): Outputs a message to the console.
* table(): Displays tabular data as a table.
* warn(): Outputs a warning message to the console.

##### breakpoints:
You can pause the execution of a script on any line using breakpoints. Then you can check the values stored in variables at that point in time.