# Links
Links are the defining feature of the web because they allow you to move from
one web page to another — enabling the
very idea of browsing or surfing.
### Types of links:
* Links from one website to another
* Links from one page to another on the same website
* Links from one part of a web page to another part of the
same page
* Links that open in a new browser window
* Links that start up your email program and address a new
email to someone

X Links are created using the ```<a>``` element.
X The ```<a>``` element uses the href attribute to indicate
the page you are linking to.
X If you are linking to a page within your own site, it is
best to use relative links rather than qualified URLs.
X You can create links to open email programs with an
email address in the "to" field.
X You can use the id attribute to target elements within
a page that can be linked to.

### Example:
```
<html>
<head>
 <title>Links</title>
</head>
<body>
 <h1 id="top">Film Folk</h1>
 <h2>Festival Diary</h2>
 <p>Here are some of the film festivals we
 will be attending this year.<br />Please
 <a href="mailto:filmfolk@example.org">
 contact us</a> if you would like more
 information.</p>
 <h3>January</h3>
 <p><a href="http://www.sundance.org">
 Sundance Film Festival</a><br />
 Park City, Utah, USA<br />
 20 - 30 January 2011</p>
 <h3>February</h3>
 <p><a href="http://www.tropfest.com">
 Tropfest</a><br />
 Sydney, Australia<br />
 20 February 2011</p>
 <!-- additional content -->
 <p><a href="about.html">About Film Folk</a></p>
 <p><a href="#top">Top of page</a></p>
</body>
</html>
```
 
 # Layout
 CSS layout helps control where each element sits on a page and how to create attractive page layouts.

## Key Concepts in Positioning Elements
### Building Blocks
CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
#### Block-level elements
start on a new line, examples include:
```<h1> <p> <ul> <li>```
#### Inline elements
flow in between
surrounding text, examples include:
```<img> <b> <i>```

## Containing Elements
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

### Controlling the Position of Elements
CSS has the following positioning schemes that allow you to control
the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position
property in CSS. You can also float elements using the float property.
#### Normal flow
Every block-level element
appears on a new line, causing
each item to appear lower down
the page than the previous one.
Even if you specify the width
of the boxes and there is space
for two elements to sit side-byside, they will not appear next
to each other. This is the default
behavior (unless you tell the
browser to do something else).
#### Relative Positioning
This moves an element from the
position it would be in normal
flow, shifting it to the top, right,
bottom, or left of where it
would have been placed. This
does not affect the position of
surrounding elements; they stay
in the position they would be in
in normal flow.
#### Absolute positioning
This positions the element
in relation to its containing
element. It is taken out of
normal flow, meaning that it
does not affect the position
of any surrounding elements
(as they simply ignore the
space it would have taken up).
Absolutely positioned elements
move as users scroll up and
down the page.
#### Fixed Positioning
This is a form of absolute
positioning that positions
the element in relation to the
browser window, as opposed
to the containing element.
Elements with fixed positioning
do not affect the position of
surrounding elements and they
do not move when the user
scrolls up or down the page.
#### Floating Elements
Floating an element allows
you to take that element out
of normal flow and position
it to the far left or right of a
containing box. The floated
element becomes a block-level
element around which other
content can flow. 
![css positioning](https://cdn.educba.com/academy/wp-content/uploads/2019/12/CSS-Position.jpg)

# Functions, Methods, and Objects
Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.
## Function declarations
A function definition consists of the followings:
* The name of the function.
* A list of parameters to the function, enclosed in parentheses and separated by commas.
* The JavaScript statements that define the function, enclosed in curly brackets, {...}.

>function square(number) { return number * number;
}

## Calling functions
Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters.

## Example
```
function myFunc(theObject) {
  theObject.make = 'Toyota';
}

var mycar = {make: 'Honda', model: 'Accord', year: 1998};
var x, y;

x = mycar.make; // x gets the value "Honda"

myFunc(mycar);
y = mycar.make; // y gets the value "Toyota"
                // (the make property was changed by the function)
```

# 6 Reasons for Pair Programming
Pair programming is the practice of two developers sharing a single workstation to interactively tackle a coding task together. Pair programming touches on all four skills that help anyone learn a new language: developers explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves.
## 1. Greater efficiency
## 2. Engaged collaboration
## 3. Learning from fellow students
## 4. Social skills
## 5. Job interview readiness
## 6. Work environment readiness