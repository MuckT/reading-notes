# class-01 reading notes

## [Quizlet Terms #TODO](https://quizlet.com/)

### HTML Introduction

* How People Access The Web
  * Browser
  * Web Servers
  * Devices
  * Screen Readers
* How Websites created
  * HTML / CSS - Static sites
  * HTML / CSS / JavaScript - More Interactive websites
  * Content Management Systems (CMS) such as Wordpress
* How The Web Works
  * Domain Name System (DNS)
  * Internet Service Provider (ISP)

### HTML Chapter 1: Structure

* HTML Describes the structure of the page
* Attributes provide additional information about elements
  * Commonly lowercase with parenthesis
  * Require a name and value
* Body Element
  * Everything inside this is displayed in the browser window
* Head Element
  * Contains information about the page e.g. &lt;title&gt; & &lt;meta&gt;
  * Content in the &lt;title&gt; will display in the top of the browser above the url

### HTML Chapter 8: Extra Markup

* DOCTYPE &lt;!DOCTYPE html&gt;
* Comments <-- This is a comment !-->
* ID Attribute
  * Must be unique
  * &lt;div id="sample-id"&gt;
* Class Attribute
  * Used to identify several elements
  * &lt;div class="sample classes"&gt;
* Block level Elements
  * Always appear to start on a new line by default
  * &lt;h1&gt;, &lt;p&gt;, &lt;ul&gt;, &lt;li&gt;
* Inline Elements
  * Always appear to continue on the same line by default
  * &lt;a&gt;, &lt;b&gt;, &lt;em&gt;, &lt;img&gt;
* &lt;div&gt; allows grouping of elements together in a block
* &lt;span&gt; allows grouping of elements together inline
* &lt;iframe&gt; allows embedded content from another page e.g. Google Maps or YouTube
* &lt;meta&gt; present in the header contains information about the page
  * &lt;meta name="description"&gt;
  * &lt;meta name="keywords"&gt;
  * &lt;meta name="robots"&gt;
  * &lt;meta name="author"&gt;
  * &lt;meta name="pragma"&gt;
  * &lt;meta name="expires"&gt;
* Escape characters
  * Alternatives to reserved characters used by HTML

### HTML Chapter 17: HTML5 Layout

* Traditional HTML Layouts
  * Div elements to group together related elements on the page
  * Class or id used to indicate role of the div

### JavaScript Introduction

* JavaScript makes webpages interactive by:
  * Accessing the content of the page
  * Modifying the content of the page
  * Programming rules or instructions
  * Reacting to events

### JS Chapter 1: The ABC of Programming

* A script is a series of instructions that the computer can follow in order to achieve a goal
* Objects can contain:
  * Properties - characteristics in a name value pair
  * Events - interactions that can change the values of the properties
  * Methods - can retrieve or update the values of properties
* How HTML CSS & JavaScript work together
  * HTML - Contains Content
  * CSS - Controls Presentation of Content
  * JavaScript - Controls interactions with the page
    * Should be loaded from an external file to avoid cluttering the html
    * Runs where it is found in the page e.g. &lt;script&gt; tag in the header will run before a &lt;script&gt; tag in the body.
