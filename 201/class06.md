# Understanding The Problem Domain Is The Hardest Part Of Programming
What is the hardest thing about writing code?

There are many common answers to this question:

* Learning a new technology
* Naming things
* Testing your code
* Debugging
* Fixing bugs
* Making software maintainable

### But he single hardest thing about programming is learning the problem domain.
### Why problem domains are hard
programming just like puzzel you can’t really see what you are trying to build very clearly.The real world is a messy place.  Many of the problem domains we face as programmers are difficult to understand and look completely different depending on your viewpoint. As programmers, we also are often not given complete information about the problem domain, so we don’t even have the information we need to understand it.

## Programming is easy if you understand the problem domain
If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

1. Make the problem domain easier
2. Get better at understanding the problem domain

# Object Literals
## WHAT IS AN OBJECT?
Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names. 
```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

# Document Object Model
The document object represents your web page.

If you want to access any element in an HTML page, you always start with accessing the document object.

Below are some examples of how you can use the document object to access and manipulate HTML.


## Finding HTML Elements

* document.getElementById(id)  -  Find an element by element id
* document.getElementsByTagName(name)  -  Find elements by tag name
* document.getElementsByClassName(name)  -  Find elements by class name
## Changing HTML Elements

* element.innerHTML =  new html content  -  Change the inner HTML of an element
* element.attribute = new value  -  Change the attribute value of an HTML element
* element.style.property = new style  -  Change the style of an HTML element
* element.setAttribute(attribute, value)  -  Change the attribute value of an HTML element
## Adding and Deleting Elements

* document.createElement(element)  -  Create an HTML element
* document.removeChild(element)  -  Remove an HTML element
* document.appendChild(element)  -  Add an HTML element
* document.replaceChild(new, old)  -  Replace an HTML element
* document.write(text)  -  Write into the HTML output stream



