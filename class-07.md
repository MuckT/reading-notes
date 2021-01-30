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

* ...
