# HTML Images
A picture can say a thousand words, and great
images help make the difference between an
average-looking site and a really engaging one. There are several things to consider when selecting and
preparing images for your site, such as:
* Include an image in your web pages using HTML
* Pick which image format to use
* Show an image at the right size
* Optimize an image for use on the web to make pages load faster

## To add an image into the page
you need to use an ```<img>```
element. This is an empty
element (which means there is
no closing tag). It must carry the
### following two attributes:
1. **src :**
This tells the browser where
it can find the image file. This
will usually be a relative URL
pointing to an image on your
own site. (Here you can see that
the images are in a child folder
called images — relative URLs
were covered on pages 83-84).
2. **alt :** 
This provides a text description
of the image which describes the
image if you cannot see it.

You must always specify a src attribute to indicate the
source of an image and an alt attribute to describe the
content of an image.
Also you should save images at the size you will be using
them on the web page and in the appropriate format.
Photographs are best saved as JPEGs; illustrations or
logos that use flat colors are better saved as GIFs.

 [JPEG vs PNG vs GIF](https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d)

# CSS Color 
Color will bring your pages to life.
## Foreground Color
### color
The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways:
1. **rgb values :**
These express colors in terms
of how much red, green and
blue are used to make it up. For
example: rgb(100,100,90)
2. **hex codes :**
These are six-digit codes that
represent the amount of red,
green and blue in a color,
preceded by a pound or hash #
sign. For example: #ee3e80
3. **color names :**
There are 147 predefined color
names that are recognized
by browsers. For example:
DarkCyan
We look at these three different
ways of specifying colors on the
next double-page spread.

/* color name */
h1 {
color: DarkCyan;}
/* hex code */
h2 {
color: #ee3e80;}
/* rgb value */
p {
color: rgb(100,100,90);}

## Background Color
### background-color
CSS treats each HTML element
as if it appears in a box, and the
background-color property
sets the color of the background
for that box.
You can specify your choice of
background color in the same
three ways you can specify
foreground colors: RGB values,
hex codes, and color names
(covered on the next page).
If you do not specify a
background color, then the
background is transparent.
By default, most browser
windows have a white
background, but browser users
can set a background color for
their windows, so if you want
to be sure that the background
is white you can use the
background-color property on
the ```<body>``` element.

# Text CSS
The formatting of your text can have a significant effect
on how readable your pages are. The CSS properties used to style text generally fall into two categories:

## 1. Font styles: 
Properties that affect the font that is applied to the text, affecting what font is applied, how big it is, whether it is bold, italic, etc.
## 2. Text layout styles:
 Properties that affect the spacing and other layout features of the text, allowing manipulation of, for example, the space between lines and letters, and how the text is aligned within the content box.

