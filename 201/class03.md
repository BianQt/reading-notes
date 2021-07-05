# HTML Lists
### HTML provides us with three different types:
* **Ordered lists** are lists where each item in the list is
numbered. For example, the list might be a set of steps for
a recipe that must be performed in order, or a legal contract
where each point needs to be identified by a section
number.
* **Unordered lists** are lists that begin with a bullet point
(rather than characters that indicate order).
* **Definition lists** are made up of a set of terms along with the
definitions for each of those terms.
## Example
```
<html>
<head>
 <title>Lists</title>
 </head>
 <body>
 <h1>Scrambled Eggs</h1>
 <p>Eggs are one of my favourite foods. Here is a
 recipe for deliciously rich scrambled eggs.</p>
 <h2>Ingredients</h2>
 <ul>
 <li>2 eggs</li>
 <li>1tbs butter</li>
 <li>2tbs cream</li>
 </ul>
 <h2>Method</h2>
 <ol>
 <li>Melt butter in a frying pan over a medium
 heat</li>
 <li>Gently mix the eggs and cream in a bowl</li>
 <li>Once butter has melted add cream and eggs</li>
 <li>Using a spatula fold the eggs from the edge of
 the pan to the center every 20 seconds (as if
 you are making an omelette)</li>
 <li>When the eggs are still moist remove from the
 heat (it will continue to cook on the plate
 until served)</li>
 </ol>
</body>
</html>
```
# CSS Boxs
## CSS treats each HTML element as if it lives in its own box.
You can set several properties that affect the appearance of
these boxes such as:
* Controlling the dimensions of your boxes
* Creating borders around boxes
* Set margins and padding for boxes
* Showing and hiding boxes

## Example

```
<!DOCTYPE html>
<html>
<head>
 <title>Boxes</title>
 <style type="text/css">
 body {
 font-size: 80%;
 font-family: "Courier New", Courier, monospace;
 letter-spacing: 0.15em;
 background-color: #efefef;}
 #page {
 max-width: 940px;
 min-width: 720px;
 margin: 10px auto 10px auto;
 padding: 20px;
 border: 4px double #000;
 background-color: #ffffff;}
 #logo {
 width: 150px;
 margin: 10px auto 25px auto;}
 ul {
 width: 570px;
 padding: 15px;
 margin: 0px auto 0px auto;
 border-top: 2px solid #000;
 border-bottom: 1px solid #000;
 text-align: center;}
 li {
 display: inline;
 margin: 0px 3px;}
 p {
 text-align: center;
 width: 600px;
 margin: 20px auto 20px auto;
 font-weight: normal;}
 a {
 color: #000000;
 text-transform: uppercase;
 text-decoration: none;
 padding: 6px 18px 5px 18px;}
 a:hover, a.on {
 color: #cc3333;
 background-color: #ffffff;}
 </style>
</head>
<body>
 <div id="page">
 <div id="logo">
 <img src="images/logo.gif" alt="The Analog Specialists" />
 </div>
 <ul id="navigation">
 <li><a href="#" class="on">Home</a></li>
 <li><a href="#">For Sale</a></li>
 <li><a href="#">Repairs</a></li>
 <li><a href="#">About</a></li>
 <li><a href="#">Contact</a></li>
 </ul>
 <p>
 <img src="images/keys.jpg" alt="Fender Rhodes, Hohner Clavinet,
 and Wurlitzer EP200" />
 </p>
 <p>
 We specialise in the sales and repair of classic keyboards, in particular
 the Fender Rhodes, Wurlitzer EP200, and Hohner Clavinet.
 </p>
 </div>
</body>
</html>
```


# Basics of JavaScript
JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it.

**Do not confuse JavaScript with the Java programming language.** Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantic, and use.

### Modules

1. JavaScript first steps

2. JavaScript building blocks

3. Introducing JavaScript objects

4. Asynchronous JavaScript

  Source - [Class02 read](https://bianqt.github.io/reading-notes/201/class02)

# Decisions and Loops
Looking at a flowchart (for all but the most basic scripts), the code can take more than one path, which means the browser runs different code in different situations. 
To determine which path to take, programmers often rely upon the following three concepts: 
* **EVALUATIONS :** You can analyze values in your scripts to determine whether or note they match expected results. 
* **DECISIONS :** Using the results of evaluations, you can decide which path your script should go down. 
* **LOOPS :** There are also many occasions where you will want to perform the same set of steps repeatedly. 

## Decision Making in JavaScript
### If Statement
if is used to check for a condition whether its true or not. Condition could be any expression that returns true or false. When condition satisfies then statements following if statement are executed.
### Else Statement
else statements are used with if statements. When if condition gets fail then else statement is executed.
### Else If Statement
Suppose there are variety of conditions that you want to check. You can use multiple if statements to do this task. All the if conditions will be checked one by one. But what if you want that if one condition satisfies then don't perform further conditional checks. At this point else if statement is what you need.

### Example

```
<script>

var a=3;
var b=4;

if(a > b)
{
    document.write("a is greater than b");
}
else if(a < b)
{
    document.write("a is smaller than b");
}
else
{
    document.write("Nothing worked");
}
</script>
```

 ### Switch Statements
 switch statements do the same task that else if statements do. But use switch statements when conditions are more. In that case, switch statements perform better than else if statements. switch evaluates the expression and checks whether it matches with any case. If it matches with any case then statements within that case construct are executed followed by break statement. break statement makes sure that no more case statement gets executed. In case if the expression doesn't match any case value then default case is executed.
 There could be any number of statements. No curly braces is needed inside case construct. Also you can omit the break statement in the default construct if default is the last statement within switch.
 ### Example
 ```
 <script>

var a = 7;

switch(a)
{
	case 1: document.write("one"); break;
	case 2: document.write("two"); break;
	case 3: document.write("three"); break;
	case 4: document.write("four"); break;
	case 5: document.write("five"); break;
	default: document.write("number not found");
}
//outputs three
</script>
```

## Loops in JavaScript
### While Loop
while loop checks for a given condition to be true to execute statements that it contains within it. When the condition becomes false, while loop break the execution of statements.
### Example
```
<script>
var i = 0;
while(i<6)
{
    document.write(i);
    document.write("<br />");
    i++;
}
</script>
```
## For Loop
for loop is generally used when the number of iterations/repetitions are already known. Its not that such tasks can't be done by while loop but its just a matter of preference.
### Example
```
<script>
for(var i=0;i<10;i++)
{
    document.write(i);
    document.write("<br />");
}
</script>
```
