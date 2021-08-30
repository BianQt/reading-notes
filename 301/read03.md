#  React Docs - lists and keys

## List in React
Showing a list of elements happened almost in every project I was ever writing. And React really simplifies the rendering of lists inside the JSX by supporting the Javascript .map() method.

The .map() method in Javascript iterates through the parent array and calls a function on every element of that array. Then it creates a new array with transformed values. It doesn’t change the parent array.

Now, let’s imagine that you are creating a simple Todo App. The main element of your project will be a list of tasks. To show them, you will need data, which in most cases will be an array of elements, can be objects or strings, for example.

While you have the array with data, you can use the .map() method inside the JSX component the transform the data into the element.
###
Let’s take a look at the graphic and code.

```
const tasks = [
  {text: "Buy flowers", status: "todo"},
  {text: "Go to the dentist", status: "done"},
]

const tasksList = tasks.map(task => {
  return (
  <p>{task.text} - {task.status}</p>
  )
});
```

## Keys in React
When creating a list of elements in a way you can see above, there’s one more necessary thing, and it’s a key.

key is a special attribute that you need to include in the element, and it should be a string. Keys in each list should be unique, which means that you shouldn’t use values that can be the same as the key. In other words, keys should be unique among the siblings, not globally.

For example, you should not use status or text as a key in our example.

Key is kind of the id for the element, and it helps React to identify which element was changed, added, or removed.

It’s a good practice to select a value that is a unique identifier for an item in the array, commonly it’s the ID.


```
const tasks = [
  {id: "1", text: "Buy flowers", status: "todo"},
  {id: "3", text: "Go to the dentist", status: "done"},
]

const tasksList = tasks.map(task => {
  return (
  <p key={task.id}>{task.text} - {task.status}</p>
  )
});
```

# The Spread Operator 
Spread syntax (...) allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected. 

## Description
Spread syntax can be used when all elements from an object or array need to be included in a list of some kind.

In the above example, the defined function takes x, y, and z as arguments and returns the sum of these values. An array value is also defined.

When we invoke the function, we pass it all the values in the array using the spread syntax and the array name — ...numbers.
### 
A very simple version of this kind of action could look like so:

```
let numberStore = [0, 1, 2];
let newNumber = 12;
numberStore = [...numberStore, newNumber];
```

## Syntax
For function calls:

```
myFunction(...iterableObj); // pass all elements of iterableObj as arguments to function myFunction
Copy to Clipboard
```

For array literals or strings:

```
[...iterableObj, '4', 'five', 6]; // combine two arrays by inserting all elements from iterableObj
Copy to Clipboard
```
For object literals (new in ECMAScript 2018):

```
let objClone = { ...obj }; // pass all key:value pairs from an object
 ```