# Node Ecosystem, TDD, CI/CD

## Array map() Method
The map() method in JavaScript creates an array by calling a specific function on each element present in the parent array. It is a non-mutating method. Generally map() method is used to iterate over an array and calling function on every element of array.
Syntax:

```array.map(function(currentValue, index, arr), thisValue)```

**Parameters:** This method accepts two parameters as mentioned above and described below:
###
**function(currentValue, index, arr):** It is required parameter and it runs on each element of array. It contains three parameters which are listed below:
###
* currentValue: It is required parameter and it holds the value of current element.
* index: It is optional parameter and it holds the index of current element.
* arr: It is optional parameter and it holds the array.
###
**thisValue:** It is optional parameter and used to hold the value of passed to the function.
###
**Return Value:** It returns a new array and elements of arrays are result of callback function.

## Array reduce() Method
The arr.reduce() method in JavaScript is used to reduce the array to a single value and executes a provided function for each value of the array (from left-to-right) and the return value of the function is stored in an accumulator.
###
**Syntax:**

```
array.reduce( function(total, currentValue, currentIndex, arr), 
initialValue )
```

**Parameter:** This method accepts five parameters as mentioned above and described below:

**function(total, currentValue, index, arr):** It is the required parameter and used to run for each element of array. It contains four parameter which are listed below:

* total: It is required parameter and used to specify the initialValue, or the previously returned value of the function.
* currentValue: It is required parameter and used to specify the value of the current element.
* currentIndex: It is optional parameter and used to specify the array index of the current element.
* arr: It is optional parameter and used to specify the array object the current element belongs to.

 ###
**initialValue:** It is optional parameter and used to specify the value to be passed to the function as the initial value.


## Superagent()

 ### Promise syntax
 ```
 function  getCharacters(){
  let characters = {};
  superagent.get('https://swapi.dev/api/people/').then((data)=>{
    data.body.results.forEach((char)=> {
      characters[char.name] = char.url;
    })
    console.log(characters)
  }).catch((err)=>console.log(err));
}
```

### async / await syntax
```
async function location(name){
  let data = await superagent.get(`https://geocode.xyz/${name}?json=1`);
  let long = data.body.longt, lat = data.body.latt;
  console.log('longitude:',long,', latitude:',lat)
}
```

## Promises
Promises present the eventual completion or failure of an asyncronouns operation and it's resulting value.
###
A promise is one of these states:
* Pending
* Fulfilled
* Rejected

## Are all callback functions considered to be Asynchronous? Why or Why Not?
No, taking a callback doesn't make a function asynchronous. There are many examples of functions that take a function argument but are not asynchronous. For example there's forEach in Array.
###
For a function to be asynchronous it needs to perform an asynchronous operation. It needs to incorporate the argument callback in handling the results of this asynchronous operation. Only this way the function becomes asynchronous.