# class-06 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### HTML Chapter 6: Tables

* Tables represent information in a grid format

  * Each block of the table is referred to as a cell
  
  * A table is drawn out row by row; each row is created with a `<tr>` element

* Basic Table Structure with headings

```html
<table>
  <tr>
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  <tr>
    <th scope="row">Tickets Sold:</th>
    <th>120</th>
    <th>130</th>
  </tr>
  <tr>
    <th scope="row">Total Sales:</th>
    <th>$600</th>
    <th>$675</th>
  </tr>
</table>
```

<table>
  <tr>
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  <tr>
    <th scope="row">Tickets Sold:</th>
    <th>120</th>
    <th>130</th>
  </tr>
  <tr>
    <th scope="row">Total Sales:</th>
    <th>$600</th>
    <th>$675</th>
  </tr>
</table>

```html
<table>
  <tr>
    <th></th>
    <th>9am</th>
    <th>10am</th>
    <th>11am</th>
    <th>12am</th>
  <tr>
    <th>Monday</th>
    <th colspan="2">Geography</th>
    <th>Math</th>
    <th>Art</th>
  </tr>
  <tr>
    <th>Tuesday</th>
    <th colspan="3">Gym</th>
    <th>Home Ec</th>
  </tr>
</table>
```

<table>
  <tr>
    <th></th>
    <th>9am</th>
    <th>10am</th>
    <th>11am</th>
    <th>12am</th>
  <tr>
    <th>Monday</th>
    <th colspan="2">Geography</th>
    <th>Math</th>
    <th>Art</th>
  </tr>
  <tr>
    <th>Tuesday</th>
    <th colspan="3">Gym</th>
    <th>Home Ec</th>
  </tr>
</table>

* Spanning Columns - Used when you need the entries in a table to stretch across more tha one column.

```html
<table>
  <tr>
    <th></th>
    <th>ABC</th>
    <th>BBC</th>
    <th>CNN</th>
  <tr>
    <th>6pm - 7pm</th>
    <th rowspan="2">Movie</th>
    <th>Comedy</th>
    <th>News</th>
  </tr>
  <tr>
    <th>6pm - 7pm</th>
    <th>Sports</th>
    <th>Current Affairs</th>
  </tr>
</table>
```

<table>
  <tr>
    <th></th>
    <th>ABC</th>
    <th>BBC</th>
    <th>CNN</th>
  <tr>
    <th>6pm - 7pm</th>
    <th rowspan="2">Movie</th>
    <th>Comedy</th>
    <th>News</th>
  </tr>
  <tr>
    <th>7pm - 8pm</th>
    <th>Sports</th>
    <th>Current Affairs</th>
  </tr>
</table>

* Spanning Rows - Used when you need the entries in a table to stretch across more tha one row.

* Long tables can use `<thead>` `<tbody>` & `<tfoot>` tags

### JavaScript Chapter 3: Functions, Methods, and Objects

* Constructor Notation

```javascript
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.room - this.booked;
  }
}

var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 120, 77);
```

* An Object Literal

```javascript
costs = {
  room1: 420;
  room2: 460;
  room3: 230;
  room4: 620;
}
```

* An Array

```javascript
costs = [420, 460, 230, 620]
```

* An Array of Objects

```javascript
costs = {
  room1: [420, 40, 10],
  room2: [460, 20, 20], 
  room3: [230, 0, 0],
  room4: [620, 150, 60]
}
```

* Built In Objects

  * `window` - Current browser window or tab
  
    * `window.document` - Current web page

    * `window.history` - Pages in browser history

    * `window.location` - Url of the current page

    * `window.navigator` - Information about browser

    * `window.screen` -  Device display information
  
  * `document` - Represent the page as a whole

    * `document.html` The entire html of the current page

      * `document.head` - The contents of head section of the current document

        * `document.title` - Title of current document

      * `document.body` - The contents of the body section of the current document

        * `document.body.div` - `attribute`

        * `document.body.p`

        * `document.body.text`
  
* Global Javascript Objects

  * `String` - For working with string values

    * `length` - Returns the number of characters in the string or items in the array

    * `toUpperCase()` - Changes string to uppercase characters

    * `toLowerCase()` - Changes string to lowercase characters

    * `charAt()` - Takes an index as a parameter and returns the character that is found within a string

    * `indexOf()` - Returns the index number of the first time a character or set of characters is found in a string; returns -1 if not found.

    * `lastIndexOf()` - Returns index number of the last time a character or set of characters is found in a string; returns -1 if not found.

    * `substring()` - Returns characters found between two index numbers where the character for the first index number is included and the character for the last index number is not included

    * `split()` - When a character is specified, it splits the string each time it's found

    * `trim()` - Removes whitespace from the start and end of a string

    * `replace()` - Like find and replace, it takes one value that should be found and another to replace it and by default only replaces the first match.

  * `Number` - For working with numeric values

    * `isNaN()` -  Checks if the value is not a number

    * `toFixed()` - Rounds to a specified number of decimal places (returns a string)

    * `toPrecision()` - Rounds to total number of places (returns a string)

    * `toExponential()` - Returns a string representing the number in exponential notation

  * `Boolean` - For working with boolean values

  * `Date` - To represent and handle dates

    * `getDate()` & `setDate()` - Returns / sets the day of the month (1 - 31)

    * `getDay()` - Returns the day of the week (0 - 6)

    * `getFullYear()` & `setFullYear()` - Returns / sets the year (4 digits)

    * `getHours()` & `setHours()` - Returns / sets the hours (0 - 23)

    * `getMilliseconds()` & `setMilliseconds()` - Returns / sets the milliseconds (0 - 9999)

    * `getMinutes()` & `setMinutes()` - Returns / sets the minute (0 - 59)

    * `getSeconds()` & `setSeconds()` - Returns / sets the seconds (0 - 59)

    * `getMonth()` & `setMonth()` - Returns / sets the month (0 - 11)

    * `getTime()` & `setTime()` - Returns / sets the number of milliseconds since Unix Epoch on January 1st, 1970 at UTC

    * `getTimeZoneOffset()` - Returns time zone offset in mins for locale

    * `toDateString()` - Returns "date" as a human-readable string

    * `toTimeString()` - Return "time" as a human readable string

    * `toString()` - Returns a string representing the specific date

  * `Math` - For working with numbers and calculations

    * `Math.PI` - Returns pi (3.14159265359...)

    * `Math.round()` - Rounds number to the nearest integer

    * `Math.sqrt(n)` - Returns square root of positive number, e.g. `Math.sqrt(9) === 3`

    * `Math.ceil()` - Rounds number up to the nearest integer

    * `Math.floor()` - Rounds number down to the nearest integer

  * `Regex` - For matching patterns within strings of text
