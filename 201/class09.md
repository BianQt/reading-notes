# HTML Forms
An HTML form is used to collect user input. The user input is most often sent to a server for processing.
## 1. The ```<form>``` Element
The ```<form>``` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.
## 2. The ```<input>``` Element
The HTML ```<input>``` element is the most used form element. An ```<input>``` element can be displayed in many ways, depending on the type attribute.

| Type      | Description |
| ----------- | ----------- |
| ```<input type="text">```     | Displays a single-line text input field      |
| ```<input type="radio">```   | Displays a radio button (for selecting one of many choices)        |
| ```<input type="checkbox">```   | Displays a checkbox (for selecting zero or more of many choices)      |
| ```<input type="submit">```   | Displays a submit button (for submitting the form)      |
| ```<input type="button">```   | Displays a clickable button        |

# Lists, Tables & Forms Styling
In addition to the CSS properties which work with the contents of all elements,
there are several others that are specifically used to control the appearance of lists, tables, and forms.

## Lists
List markers can be given different appearances
using the list-style-type and list-style image
properties.
### 1. Bullet Point Styles "list-style-type"
The list-style-type property
allows you to control the shape
or style of a bullet point (also
known as a marker).
It can be used on rules that
apply to the ```<ol>```, ```<ul>```, and ```<li>```
elements.
### 2. Images for Bullets "list-style-image"
You can specify an image to act
as a bullet point using the
list-style-image property.
The value starts with the letters
url and is followed by a pair
of parentheses. Inside the
parentheses, the path to the
image is given inside double
quotes.
This property can be used on
rules that apply to the ```<ul>``` and
```<li> ```elements.


## Tables
Table cells can have different borders and spacing in
different browsers, but there are properties you can
use to control them and make them more consistent. 
###
* **width** to set the width of the
table
* **padding** to set the space
between the border of each table
cell and its content
* **text-transform** to convert the
content of the table headers to
uppercase
* **letter-spacing**, font-size
to add additional styling to the
content of the table headers
* **border-top, border-bottom**
to set borders above and below
the table headers
* **text-align** to align the writing
to the left of some table cells and
to the right of the others
* **background-color** to change
the background color of the
alternating table rows
* **:hover** to highlight a table row
when a user's mouse goes over it

## Forms
Forms are easier to use if the form controls are
vertically aligned using CSS. Also, benefit from styles that make them feel more
interactive. It is most common to style:
* Text inputs and text areas
* Submit buttons
* Labels on forms

# Events 
HTML events are "things" that happen to HTML elements. When JavaScript is used in HTML pages, JavaScript can "react" on these events.
###
The most commonly used events are W3C DOM
events, although there are others in the HTMLS
specification as well as browser-specific events. 
## JavaScript HTML DOM Events 
A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.

To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute: ```onclick=JavaScript```
### Example
```<!DOCTYPE html>
<html>
<body>

<h2>JavaScript HTML Events</h2>
<p>Click "Try it" to execute the displayDate() function.</p>

<button id="myBtn">Try it</button>

<p id="demo"></p>

<script>
document.getElementById("myBtn").onclick = displayDate;

function displayDate() {
  document.getElementById("demo").innerHTML = Date();
}
</script>

</body>
</html> 
```
## JavaScript HTML DOM EventListener
The ```addEventListener()``` method attaches an event handler to the specified element.
### Example
```<!DOCTYPE html>
<html>
<body>

<h2>JavaScript addEventListener()</h2>

<p>This example uses the addEventListener() method to attach a click event to a button.</p>

<button id="myBtn">Try it</button>

<script>
document.getElementById("myBtn").addEventListener("click", function() {
  alert("Hello World!");
});
</script>

</body>
</html>
```
