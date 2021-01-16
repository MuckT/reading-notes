# class-03 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### HTML Chapter 3: Lists

* Numbered Lists a.k.a. an ordered list

```html
<ol>
  <li>Item #1</li>
  <li>Item #2</li>
  <li>Item #3</li>
</ol>
```

* Bullet lists a.ka. an unordered list

```html
<ul>
  <li>Item</li>
  <li>Item</li>
  <li>Item</li>
</ul>
```

* Definition lists

```html
<dl>
  <dt>Item Name</dt>
  <dd>Item Description...</dd>
  <dt>Item Name</dt>
  <dd>Item Description...</dd>
  <dt>Item Name</dt>
  <dd>Item Description...</dd>
</dl>
```

* Nested lists - Can be achieved by putting a second list in a <li> or <dd>

```html
<ul>
  <li>
    <ol>
      <li>Item #1</li>
      <li>Item #2</li>
      <li>Item #3</li>
    </ol>
  </li>
  <li>Item</li>
  <li>Item</li>
</ul>
```

### HTML Chapter 13: Boxes TODO

* Controlling the size of boxes
* Box model for boarders, margin, and padding
* Displaying and hiding boxes

### JavaScript Chapter 4: Decisions and Loops

* Switch Statements
  * Compare a value against possible outcomes and have a default returned option

  ```javascript
  var result;

  switch(2) {
  case 1:
    result = false;
    break;
  case 2:
    result = true;
    break;
  default:
    result = false;
    break;
  }

  return result
  ```

* Type Coercion
  * Data Types can be coerced from one type to another in JavaScript
  * JavaScript uses weak typing being the data type for a value can change.
  * Languages such as C# are strongly typed where the variables data type must be specified
  * Use `===` instead of `==` to compare not only values but types
  * Data Types:
    * string
    * number
    * Boolean
    * null
    * undefined

* Checking Equality
  * All JavaScript values can be evaluated in terms of truthy or falsy
  * Truthy Values:
    * The boolean `true`
    * Numbers other than 0
    * Strings with content
    * Number calculations
  * Falsy Values:
    * The boolean `false`
    * The number 0 e.g. `0`
    * An empty string e.g. `''`
    * Not a number `NaN`
    * undefined
* Short Circuits - Logical operators are processed left to right; as soon as they have a result they return the value that stopped the processing

  ```javascript
  var valA = 0;
  var valB = 1;
  var valC = 2;
  
  if (valA || valB || valC) {
    // This would stop once valB is hit
  }
  ```

* Loops
  * Key Loop Concepts
    * `break` - causes loop termination
    * `continue` - stop the current iteration then update and check the condition again
    * Any variable you cna define outside the loop that does not change should be so as to not be recalculated on each iteration
    * O(n) – Linear by default

  * For Loops
  ```javascript
  for(var i=0; i < 3; i++) {
    console.log(`This is loop ${i}`)
  }
  /* Should return
  'This is loop 0'
  'This is loop 1'
  'This is loop 2'
  */ 
  ```

  * While Loops
  * Do While
