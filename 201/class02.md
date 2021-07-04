# Basics of HTML

![html img](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/03/difference-between-html-and-html5.png)
## 1. Text
When creating a web page, you add tags (known as markup) to the contents of the page. These tags provide extra meaning
and allow browsers to show users the appropriate structure for the page.

In this chapter we focus on how to add markup to the text that
appears on your pages. You will learn about:
* **Structural markup:** the elements that you can use to
describe both headings and paragraphs
* **Semantic markup:** which provides extra information; such
as where emphasis is placed in a sentence, that something
you have written is a quotation (and who said it), the
meaning of acronyms, and so on

* ### Headings
Browsers display the contents of
headings at different sizes. The
contents of an < h1 > element is
the largest, and the contents of
an < h6 > element is the smallest.
![headings](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSkMftKlwfQxeVlSKyRhzRRrN10DWabBeWKuN7FHAKWfwzAyeNUORBC-6M3fVf8RSBIMGM&usqp=CAU)

* ### Paragraphs
To create a paragraph, surround
the words that make up the
paragraph with an opening < p >
tag and closing < /p > tag.

* ### Bold & Italic
By enclosing words in the tags
< b > and < /b > we can make
characters appear bold.
By enclosing words in the tags
< i > and < /i > we can make
characters appear italic.
* ### Superscript & Subscrip
The < sup > element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 22.
< sub >
The < sub > element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H20.

### Summary
* HTML elements are used to describe the structure of
the page (e.g. headings, subheadings, paragraphs).
* They also provide semantic information (e.g. where
emphasis should be placed, the definition of any
acronyms used, when given text is a quotation).


# Basics of CSS 

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

# Basics of JS
![JS](https://2.bp.blogspot.com/-z6q9nVbRxTI/XD-eNSUWtrI/AAAAAAAAMC0/bYratloel2AytKlQXuaFqD51D3P54xE5gCLcBGAs/s1600/%25D9%2585%25D8%25B5%25D8%25A7%25D8%25AF%25D8%25B1%2B%25D8%25AA%25D8%25B9%25D9%2584%25D9%2585%2B%25D8%25AC%25D8%25A7%25D9%2581%25D8%25A7%2B%25D8%25B3%25D9%2583%25D8%25B1%25D9%258A%25D8%25A8%25D8%25AA.png)
JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it.

** Do not confuse JavaScript with the Java programming language.** Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantic, and use.

### Modules

1. JavaScript first steps

2. JavaScript building blocks

3. Introducing JavaScript objects

4. Asynchronous JavaScript

## Loops and iteration
Loops offer a quick and easy way to do something repeatedly.You can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another.



### For Statement
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

A for statement looks as follows:
> for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement

### While Statement
A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:
>while (condition)
  statement