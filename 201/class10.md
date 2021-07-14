# Error Handling & Debugging
JavaScript can be hard to learn and everyone makes
mistakes when writing it.Programming is like problem solving: you are given a puzzle and not only do you have to solve
it, but you also need to create the instructions that allow the computer to solve it. too.
Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors. Searching for (and fixing) errors in programming code is called code debugging.

**1. THE CONSOLE & DEV TOOLS**
Tools built into the browser
that help you hunt for errors.
###
**2. COMMON PROBLEMS**
Common sources of errors,
and how to solve them.
###
**3. HANDLING ERRORS**
How code can deal with
potential errors gracefully.  

## **The console.log() Method**
The console helps narrow down the area in which the
error is located, so you can try to find the exact error.

### Example
```<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>

<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>

</body>
</html>
```

## **Major Browsers' Debugging Tools**
Normally, you activate debugging in your browser with F12, and select "Console" in the debugger menu.

Otherwise follow these steps:

### 1. Chrome
* Open the browser.
* From the menu, select "More tools".
* From tools, choose "Developer tools".
* Finally, select Console.
### 2. Firefox
* Open the browser.
* From the menu, select "Web Developer".
* Finally, select "Web Console".
### 3. Edge
* Open the browser.
* From the menu, select "Developer Tools".
* Finally, select "Console".
### 4.Opera
* Open the browser.
* From the menu, select "Developer".
* From "Developer", select "Developer tools".
* Finally, select "Console".
### 5.Safari
* Go to Safari, Preferences, Advanced in the main menu.
* Check "Enable Show Develop menu in menu bar".
* When the new option "Develop" appears in the menu:
* Choose "Show Error Console".