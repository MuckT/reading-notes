# class-02 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### HTML Chapter 2: Text

* HTML elements are used to describe the structure of the page (e.g. headings, subheadings, paragraphs)
  * Headings
  * SubHeadings
  * Paragraphs
* Semantic information tags
  * TODO

### HTML Chapter 10: Introducing CSS

* TODO

### JS Chapter 2: Basic JavaScript Instructions

* Statements
  * An individual instruction or step
  * Each should start on a new line and end with a semicolon
  * Some statements are surrounded by curly braces these are known as code blocks.
* Comments
  * Should be written to explain what the code does
  * Multiline comments /\*comment\*/
  * Single line comments \/\/ comment
* Variables
  * A temporary store of information
  * 
  * Declared like `var variable;`
  * Shorthand declaration `var variableOne, variableTwo, variableThree`
  * Assigned like `variable = 0;`
  * Rules for naming:
    * The name must being with a letter e.g. `sample`, `$`, or `_`, and must <b>not</b> start with a number
    * Must not contain a `-` or `.`
    * Cannot use [reserved keywords](https://www.w3schools.com/Js/js_reserved.asp)
    * names are case sensitive `sample !== Sample`
    * Camel Case e.g. `sampleVariables`
* Data Types
  * Numeric Data Type
    * `typeof(42) === 'number';`
  * String Data Type
    * `typeof('String') === 'number';`
    * <code>\`string\`, 'string', "string"</code>
  * Boolean Data Type
    * `typeof(true) === 'boolean';`
    * `typeof(false) === 'boolean';`
  * Arrays
    * Stores a list of values
    * Should be used when working with a list or a set of values that are related to each other
    * `var sampleArray = ['Text1', 'Text2', 42, { sampleProp: 'Sample Value'}]`
    * `var sampleArray = newArray('Text1', 'Text2', 42, { sampleProp: 'Sample Value'})`
    * Arrays are accessed as if they are a numbered list e.g. `(sampleArray[2] === 42` is true.
  * Expressions
    * Evaluates into a single value
    * Can just assign a value to a variable
    * Can also return the result of two or values to a single variable.
  * Operations
    * Assignment Operators e.g. `var color = 'blue';`
    * Arithmetic Operators e.g. `var area = 3 * 2;`
    * String Operators e.g. `var greeting = 'Hi ' + 'Molly';`
    * Comparison Operators e.g. `var buy = 3 > 5;`
    * Logical Operators e.g. `var buy = (5 > 3) && (2 < 4);`
    * Arithmetic Operators
      * Addition `+`, Subtraction `-`, Division `/`, Multiplication `*`, Increment `++`, Decrement `--`, Modulus `%`

### Chapter 4: Decisions & Loops

* Evaluating Conditions and Conditional Statements
  * if / then / else
  * ...
* Comparison Operators
  * `==` checks that content is equal
  * `!=` checks that content is not equal
  * `===` checks that content & type is equal aka strictly equal
  * `!==` checks that content or type is not equal strictly not equal
  * `>` greater than
  * `<` less than
  * `>=` greater than or equal to
  * `<=` less than or equal to
* Logical Operators
  * `&&` Logical AND
  * `||` Logical OR
  * `!` Logical NOT
* Short Circuit Evaluation
  * Logical expressions are evaluated left to right; evaluation can stop when there is enough information to evaluation
    * `true || null || undefined || false` - stops after seeing true
    * `false && true && 42`- stops after seeing false
* IF Statements
  * Checks of evaluates a condition; if the condition evaluates true code in the if block is executed.
    ```
    if (true) {
      console.log('This code will run');
    }
    ```
* IF ELSE Statements
  * Checks a the first if conditional and if false runs the else statement
    ```
    if (false) {
      console.log('This code will never run');
    } else {
      console.log('This code will always run');
    }
    ```
