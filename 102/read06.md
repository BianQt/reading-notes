# CSS 
![CSS img](https://res.cloudinary.com/practicaldev/image/fetch/s--cqZIl0gD--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://thepracticaldev.s3.amazonaws.com/i/elytski1o23ybosxmors.jpg)

[CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) (Cascading Style Sheets) allows you to create great-looking web pages, but how does it work under the hood? This article explains what CSS is, with a simple syntax example, and also covers some key terms about the language.

## What is CSS for?
CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

A **document** is usually a text file structured using a markup language — [HTML](https://bianqt.github.io/reading-notes/read03)   is the most common markup language, but you may also come across other markup languages such as SVG or XML.

**Presenting** a document to a user means converting it into a form usable by your audience. Browsers, like Firefox, Chrome, or Edge , are designed to present documents visually, for example, on a computer screen, projector or printer.

## CSS Syntax
CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. For example "I want the main heading on my page to be shown as large red text."

The following code shows a very simple CSS rule that would achieve the styling described above:
>h1 {
    color: red;
    font-size: 5em;
}

## How To Add CSS
When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet.

### Three Ways to Insert CSS

* External CSS
* Internal CSS
* Inline CSS


####  External CSS
With an external style sheet, you can change the look of an entire website by changing just one file!

Each HTML page must include a reference to the external style sheet file inside the < link > element, inside the head section.
 
 > < head >
< link rel="stylesheet" href="mystyle.css" >
< /head >

#### Internal CSS
An internal style sheet may be used if one single HTML page has a unique style.

The internal style is defined inside the < style > element, inside the head section.
>< style >
 body {
  background-color: linen;
  }
h1 {
  color: maroon;
  margin-left: 40px;
 }
 < /style >

#### Inline CSS
An inline style may be used to apply a unique style for a single element.

To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.
>< h1 style="color:blue;text-align:center;" >This is a heading< /h1 >