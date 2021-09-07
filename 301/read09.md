# FUNCTIONAL PROGRAMMING
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

## Concepts of functional programming: 

* Pure functions
* Recursion
* Referential transparency
* Functions are First-Class and can be Higher-Order
* Variables are Immutable

### Pure functions: 
These functions have two main properties. First, they always produce the same output for same arguments irrespective of anything else. 
Secondly, they have no side-effects i.e. they do not modify any arguments or local/global variables or input/output streams. 
Later property is called immutability. The pure function’s only result is the value it returns. They are deterministic. 
```sum(x, y)           // sum is function taking x and y as arguments
return x + y    // sum is returning sum of x and y without changing them
```

### Recursion: 
There are no “for” or “while” loop in functional languages. Iteration in functional languages is implemented through recursion. Recursive functions repeatedly call themselves, until it reaches the base case. 
    
###
example of the recursive function:  
```
fib(n)
if (n <= 1)
return 1;
else
return fib(n - 1) + fib(n - 2);
```
### Referential transparency: 
In functional programs variables once defined do not change their value throughout the program. Functional programs do not have assignment statements. If we have to store some value, we define new variables instead. This eliminates any chances of side effects because any variable can be replaced with its actual value at any point of execution. State of any variable is constant at any instant. 
###
Example:  
```
x = x + 1 // this changes the value assigned to the variable x.
          // So the expression is not referentially transparent. 
```

### Functions are First-Class and can be Higher-Order:
 First-class functions are treated as first-class variable. The first class variables can be passed to functions as parameter, can be returned from functions or stored in data structures. Higher order functions are the functions that take other functions as arguments and they can also return functions. 
###
Example: 
```
show_output(f)            // function show_output is declared taking argument f 
                          // which are another function
    f();                  // calling passed function

print_gfg()             // declaring another function 
    print("hello gfg");

show_output(print_gfg)  // passing function in another function
```
### Variables are Immutable: 
In functional programming, we can’t modify a variable after it’s been initialized. We can create new variables – but we can’t modify existing variables, and this really helps to maintain state throughout the runtime of a program. Once we create a variable and set its value, we can have full confidence knowing that the value of that variable will never change.  