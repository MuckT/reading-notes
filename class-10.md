# class-07 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### JavaScript Chapter 10: Error Handling and Debugging

* Order of Execution - The order in which statements are processed

* Execution Contexts - Every statement in a script live in one of three execution contexts

  * Global Context - Code that is in a script but not in a function, only one per page.

  * Function Context - Code that is run within a function: each function has it's own context

  * Eval Context - Code that is in an internal function called `eval()`

* Variable Scope

  * Global Scope for variables defined outside of a function.

  * Function-level scope for variables declared within a function.

* The Stack - JavaScript processed one line of code at a time; When a statement needs data form another function it stacks the new function on top of the current task.

  * Each time a new item is added to the stack,, it creates a new execution context.

* Execution Context & Hosting - Each time a script enters a new execution context, there are two phases.

  * Prepare

    * The new scope is created

    * Variables, functions and arguments are created.

  * Execute

    * Assign values to variables

    * Reference functions and run their code

    * Execute statements

* Scope - Functions in JavaScript have lexical scope: they are linked to the objects they were defined within.

* Errors - If a statement generates an error, then it throws an exception.

  * Whenever the interpreter comes across an error it will look for code for error-handling code.

* Error Objects - Objects that have defined properties

  * `name` - Type of error

  * `message` - Description

  * `fileNumber` - Name of the JavaScript file

  * `lineNumber` - Line number of the error

  * JavaScripts Built In error Objects

    * `Error` - Generic error - basis for all other errors

    * `Syntax Error` - Syntax has not been followed

    * `ReferenceError` - Tried to reference a variable tat is not declared / within scope

    * `TypeError` - An unexpected data type that cannot be coerced

    * `RangeError` - Numbers not in acceptable range

    * `URIError` - `encodeURI()` & `decodeURI()` used incorrectly

    * `EvalError` - `eval()` used incorrectly

* Dealing With Errors

  * Debug the script to fix the errors

  * Handle the errors gracefully with a try, catch, finally

* Debugging Workflow

  * Where is the problem?
  
    * Relevant script, line number, & error type

    * See how far the script is running

    * Use breakpoints where things go wrong

  * What is the problem?

    * When breakpoints are set you can check variable values as you step through the code

    * Break down / breakout parts of the code to test

      * Write values of variables to the console

      * Call functions from the console

      * Check that objects exist / have the methods expected

      * Check the number of parameters passed to a function of the number of item in an array

      * Be prepared to repeate this process

* Dev Tools

  * Open the console in chrome with Ctrl + Shift + I or right click and select inspect

  * Get used to looking at network requests tabs and the application tabs.

* Console Logging

  * `console.log()`, `console.table()`, `console.info()`, `console.warn()`, `console.error()`

  * Group console messages e.g. `console.log('tempVar: ', tempVar)`

  * Use console logs to see if you've stepped into an condition or a loop.

* Breakpoints - You can pause the execution of a script on any line using breakpoints.

  * Find the line you want to set a breakpoint to and click it on the left - a red arrow is common.

  * Stepping through code - If you set multiple breakpoints you can step through them one by one.

    * Step through code - Running lines one by one

    * Step into a function call - The debugger will jump to the first line of the function

    * Step out of the function - The debugger moves out of the function and move onto the parent function

  * Conditional breakpoints - A breakpoint that should only be trigger if a condition that you specify is met.

* The Debugger Keyword - Creates a breakpoint in the code using `debugger` on that line

* Handling Exceptions

* Try, Catch, Finally

* Throwing Errors

* Common Errors
