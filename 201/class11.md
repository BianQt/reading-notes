# Images 
Controlling the size and alignment of
your images using CSS keeps rules that
affect the presentation of your page in
the CSS and out of the HTML markup.
 ## Controlling sizes of images in CSS
 You can control the size of an
image using the width and
height properties in CSS, just
like you can for any other box.

### Example 
```img.large {
width: 500px;
height: 500px;}
img.medium {
width: 250px;
height: 250px;}
img.small {
width: 100px;
height: 100px;}
```

## Aligning images Using CSS
There are two ways that
this is commonly achieved:
1. The float property is added
to the class that was created to
represent the size of the image
(such as the small class in our
example).
2. New classes are created with
names such as align-left or
align-right to align the images
to the left or right of the page.
These class names are used in
addition to classes that indicate
the size of the image.
### Example 
```img.align-left {
float: left;
margin-right: 10px;}
img.align-right {
float: right;
margin-left: 10px;}
img.medium {
width: 250px;
height: 250px;}
```

## Background Images
The background-image
property allows you to place
an image behind any HTML
element. This could be the entire
page or just part of the page. By
default, a background image will
repeat to fill the entire box.
### Example 
```body {
background-image: url("images/pattern.gif");}
```
## Gradients
CSS3 is going to introduce the
ability to specify a gradient for
the background of a box. The
gradient is created using the
background-image property
and, at the time of writing,
different browsers required a
different syntax.

### Example 
```#gradient {
/* fallback color */
background-color: #66cccc;
/* fallback image */
background-image: url(images/fallback-image.png);
/* Firefox 3.6+ */
background-image: -moz-linear-gradient(#336666,
 #66cccc);
/* Safari 4+, Chrome 1+ */
background-image: -webkit-gradient(linear, 0% 0%,
 0% 100%, from(#66cccc), to(#336666));
/* Safari 5.1+, Chrome 10+ */
background-image: -webkit-linear-gradient(#336666,
 #66cccc);
/* Opera 11.10+ */
background-image: -o-linear-gradient(#336666,
 #66cccc);
height: 150px;
width: 300px;}
```



# Practical Information

## Search Engine Optimization (SEO)
In simple terms, it means the process of improving your site to increase its visibility when people search for products or services related to your business in Google, Bing, and other search engines. The better visibility your pages have in search results, the more likely you are to garner attention and attract prospective and existing customers to your business.

## Why is SEO important?
SEO is a fundamental part of digital marketing because people conduct trillions of searches every year, often with commercial intent to find information about products and services. Search is often the primary source of digital traffic for brands and complements other marketing channels. Greater visibility and ranking higher in search results than your competition can have a material impact on your bottom line.

# Flash, Video & Audio

## Flash
Flash is a very popular technology used
to add animations, video, and audio to
websites. This chapter begins by looking
at how to use it in your web pages.
Since 2005, a number of factors have meant
that fewer websites are written in Flash or even
use elements of Flash in their pages.

## Video
he HTML ```<video>``` element is used to show a video on a web page.
### Example
```<!DOCTYPE html> 
<html> 
<body> 

<video width="400" controls>
  <source src="mov_bbb.mp4" type="video/mp4">
  <source src="mov_bbb.ogg" type="video/ogg">
  Your browser does not support HTML video.
</video>

<p>
Video courtesy of 
<a href="https://www.bigbuckbunny.org/" target="_blank">Big Buck Bunny</a>.
</p>

</body> 
</html>
```
## Audio
To play an audio file in HTML, use the ```<audio>``` element:
### Example
```<!DOCTYPE html>
<html>
<body>

<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>

</body>
</html>
```

