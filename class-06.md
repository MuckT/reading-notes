# class-06 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### Understanding The Problem Domain Is The Hardest Part Of Programming - John Sonmez

* "...single hardest thing about programming is learning the problem domain"

* "As programmers, we also are often not given complete information about the problem domain, so we don’t even have the information we need to understand it."

* How to make the problem domain easier:

  1. Make the problem domain easier - take a part of the problem and fully understand that part before expanding the problem domain.

  2. Get better at understanding the problem domain - Read existing solutions and ask someone familiar with the problem domain, like the product owner.

### JavaScript Chapter 3: Object Literals

* Objects

  * Group together a set of variables and functions to create a new model

  * A variable that is part of an object is known as a property

  * A function that is part of an object is called a method

  * Sample Object:

  ```JavaScript
  var hotel = {
    name: 'Marriott'
    rooms: 20
    booked: 15
    checkAvailability: function () {
      return this.rooms - this.booked;
    }
  }
  ```

### JavaScript Chapter 5: Document Object Model

* The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of the web page while it's in the browser window

* Accessing the elements of the dom requires two steps:

  1. Location the node that represents the element you want to work with

    ```JavaScript
    // Uses the element's id attribute (Unique in the page)
    var element = getElementById();
    ```

    ```JavaScript
    // Uses a CSS selector, and returns the first matching element
    var element = querySelector();
    ```

    ```JavaScript
    // Selects all elements that have a specific value for their class name
    var element = getElementByClassName();
    ```

    ```JavaScript
    // Selects all elements that have a specified tag name.
    var element = getElementByTagName();
    ```

    ```JavaScript
    // Uses a CSS selector to select all matching elements
    var element = querySelectorAll();
    ```

    ```JavaScript
    // Selects the parent of the element node
    var element = parentNode();
    ```

    ```JavaScript
    // Selects the previous sibling
    var element = previousSibling();
    ```

    ```JavaScript
    // Selects the next sibling
    var element = nextSibling();
    ```

    ```JavaScript
    // Selects the first child
    var element = firstChild();
    ```

    ```JavaScript
    // Selects last child
    var element = lastChild();
    ```

  2. Use it's text content, child elements, and attributes to modify, append or remove an element via dom manipulation

    ```JavaScript
    // Access or update the contents of a text node
    getElementById('sample-id').nodeValue = 'Changed'
    ```

    ```JavaScript
    // Update with innerHTML
    getElementById('sample-id').innerHTML = `<div><p>This element has been changed</p></div>`
    ```

    ```JavaScript
    // Adding an element to the dom tree
    // Create a new element and store it as a variable
    var newEl = document.createElement('li');

    // Create a text node and store it in a variable
    var newText = document.createTextNode('new list item');

    // Attach the new text node to the new element
    newEl.appendChild(newText);

    // Find the position where the new element should be added
    var position = document.getElementsByTagName('ul')[0];

    // Insert the new element into its position
    position.appendChild(newEl);
    ```

    ```JavaScript
    // Store the element to be removed
    var removeEl = document.querySelectorAll('#sample-id');
    // Store the parent of the element in a variable
    var containerEl = remove.parentNode;
    // Remove the element from its containing element
    containerEl.removeChild(removeEl);
    ```

* Comparing techniques for updating HTML content

  * `document.write()`

    | Advantages | Disadvantages |
    | :---- | ----: |
    | Quick and Easy | Only works when the page initially loads |
    | | Not best practices generally frowned upon. |

  * `element.innerHTML`

    | Advantages | Disadvantages |
    | :---- | ----: |
    | Can be used to add a lot of new markup | Should not be used to display user provided content |
    | It can be faster than DOM manipulation when adding lots of elements | Can be difficult to isolate single elements |
    | A simple way to remove all the content from one element (by assigning a blank string) | Event handlers may no longer work as intended |

  * DOM Manipulation

    | Advantages | Disadvantages |
    | :---- | ----: |
    | Useful for changing one element for a Dom fragment | Slower than innerHTML to make a lot of changes |
    | Does not affect event handlers | Takes more code than innerHTML |
    | Allows a script to add elements incrementally | |

* Cross-Site Scripting (XSS) Attack

  * <b>NEVER</b> display untrusted data in the DOM

  * Any HTML from an untrusted source opens up your site to XSS attack - This includes external script sources e.g. if you import jquery from their cdn and their source is hacked and you are importing it you are also now pwn'd.

  * Defend against XXS

    * Filter and validation to prevent attacks; however your custom regex is probably not sufficient

    * Do not allow users to submit HTML markup or JavaScript

    * Double check validation on the server, don't rely solely on front end validation as it can be edited by the user and bypassed.

    * Limit where user content goes - <b>Never</b> in script tags, HTML comments, Tag Names, Attributes, or CSS values

    * Escape user content - All Data from untrusted sources should be escaped on the server

    * <b>Never </b> include data from untrusted sources in JavaScript

    | Do use | Do not use |
    | :---- | ----: |
    | `textContent` | `innerHTML` |
    | `innerText` | |

    * In JQuery

    | Do use | Do not use |
    | :---- | ----: |
    | `.text()` | `.html()` |

  * If you use `innerHTML` or `.html()`

    1. Make sure that you control all the markup being generated

    2. The user content is escaped and added as text instead of as HTML

* Attribute Nodes
  
  * Once you have an element node you can use other properties and methods on the element

  * Check for an attribute and get it's value - It's good practice to check that it exists prior to modifying

  ```JavaScript
  var firstItem = document.getElementById('one'); // Get first list item

  if (firstItem.hasAttribute('class')) { // If it has class attribute
    var attr = firstItem.getAttribute('class'); // Get the attribute

    // Add the value of the attribute after the list
    var el = document.getElementById('scriptResults');
    el.innerHTML = `<p>The first item has a class name ${attr} </p>`
  };
  ```

  * Creating attributes and changing their values

  ```JavaScript
  var firstItem = document.getElementById('one'); // Get the first item
  firstItem.className = 'complete'; // Change its class attribute

  var fourthItem = document.getElementsByTagName('li').item(3); // Get the fourth item
  fourthItem.setAttribute('class', 'cool'); // Add an attribute to it
  ```

  * Removing attributes

  ```JavaScript
  var firstItem = document.getElementById('one') // Get the first item
  if (firstItem.hasAttribute('class')) { // If it has a class attribute
    firstItem.removeAttribute('class'); // Remove its class attribute
  }
  ```
