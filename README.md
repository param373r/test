# Introduction
## Data Types

- Number - Any number, (including number with decimals)
- String - Group of characters (enclosed in single/double quotes (doesn't matter at all))
- Boolean - `true` / `false`
- Null - `null` (Intentional absence of a value)
- Undefined - `undefined` (a non defined entity; different than null)
- Symbol - A newer feature to the language (no need to give stress on this one for now)
- Object - Collection of a related data

> The first 6 are more of a primitive data types. Objects are different

## Arithmetic Operators
- + 
- -
- * (multiply)
- /
- % (remainder; known as the modulo)

## String Concatenation
Nothing just adding strings

- Use `,` to add space between to lines `console.log('Hello','World')`


> Following sections are about properties and methods and built-in objects. Like any other OOP; properties and methods are as same as attributes (variables defined inside a class) and methods (functions defined inside a class) in javascript. 
## Properties
This is rather something to pick up on. Every object in javascript has a certain properties. (It's more like attributes in css. Like `<p>` and `<div>` tag had their attributes.)
- Every _String_ instance has a property called `length`, which can be used as `console.log('Hello'.length);`
- The `.` is another _operator_ (aka the _dot operator_)

> Fun fact: Javascript can be played without semicolons. But use them still. Don't wanna use? Good luck debugging your 1000 lines of javascript code.

## Methods
Methods are actions that we can perform.
- Methods are nothing but functions made for object (YES! ThE OOPs)

> console.log(); // YESS!! Here .log() is a method. of console class
> TODO: Practice with `console` class in your free time. Seems cute to me.

### Methods for string datatypes
- `.toUpperCase()`: Uppify the string
- `startsWith(searchString)`: Checks if the string starts with the given string
- `trim()`: Trim the whitespaces at the beginning and the end of a string.

> In the javascript docs, if there is a function's syntax like
> `''.startsWith( searchString [, length])` it means it has a must needed argument (that's outside the \[\]) and _can take an extra_ argument (more like as a feature) inside the \[\]. Here, \[length\] is an _extra_ argument.

## Built-in objects
Objects are nothing but instances of classes in javascript. Some common objects we use include `Math` from class of math.

> `Math.random()` returns a value between `0` (inclusive) and `1` (exclusive).

# Variables
Here, we will work with `var`, `let`, `const`.

- There's a difference between `var` and `let` but will cover when it comes to _functions and block codes in javascript (whatever the shit is)_
- `var` and `let` if left unassigned (`var myVar; let myVar2`) their value is automatically set to `undefined` [[javascript 101#Data Types]]
- With `var` and `let` we can reassign variables, unlike `const`.
- You need to assign a value to the variable when using `const` (Can't leave it undefined).

## Mathematical Assignment Operators
- We have `+=` as an assignment operator
```javascript
let w = 4
let w = w + 1 // makes w = 5

let w = 10
let w += 1 // makes w = 11; FEATURE OP
```
- Similarly `-= *= /=` also exists

## Increment and Decrement Operator
- Yeps they exist; both ways
	- `++a //increments and then puts the value; a++ //puts the value and then increment`
	- `--a // decrements and then puts the value; a-- //puts the value and then decrements`

## String concatenation with variables
pff, move on.

## String Interpolation
Side stuff: Remember anything about `eval` and how "\`"(backticks) were used to interpret things inside it. Well here it comes. _YOU CAN CREATE __TEMPLATE STRINGS__ USING BACKTICKS.

```javascript
const myPet = 'armadillo';  
console.log(`I own a pet ${myPet}.`); // Notice the backticks are used as in to evaluate the string before logging it to the console.
```

## typeof
This operator is used to check the data type of a variable.
```javascript
let unknown1 = 'hello world'
let unknown2 = 2
typeof unknown1 // string
typeof unknown2 // number
```

> ProTip: You can use `typeof` as an _operator_ as well as a function.
> `typeof operand`
> `typeof(operand)` 
> Think of places where you cannot use space.


## Extra Remarks 
- Adding (+) a `boolean` to a `number` value adds one `1` to the `number`. However if you use `,` (comma) it separates the 2 value with a space.

# The Javascript Frameworks
- 2009 - **Node.js** was launched to allow for javascript code execution outside the browser
- 2010 - **Angular.js** framework was released and grew in popularity with its object oriented and reactive programming.
- 2013 - **React.js** library was released with functional programming model.
	- On a little sidenote - **Electron.js** was also released in this year to develop desktop apps with front / back-end web languages
- 2014 - **Vue.js** framework was released and grew popularity due to its reactive programming model.

# Conditionals

## if statements
```javascript
if (true) {  
 console.log('This message will print!');  
}
```

## if-else statements
```javascript
if (false) {  
 console.log('The code in this block will not run.');  
} else {  
 console.log('But the code in this block will!');  
}
```

## Comparison operators
- < - less than
- > - greater than
- <= - less than or equal to
- >= - greater than or equal to
- === - is strictly equal to
- !== - is not equal to

> For once `1 == true` would return true but not `1 === true`. This is because of the strict comparison. 
> Source: https://discuss.codecademy.com/t/whats-the-different-between-two-and-three-equal-signs/505767

## Logical Operators
- && - and
- || - or
- ! - not

## Truthy and Falsy

The following conditions evaluate to be false:
- (Datatype: Number) 0
- Empty Strings like "" or ''
- `null` which represent when there is no value at all
- `undefined` represent when a declared variable lacks a value
- `NaN` or Not a Number

__REST ALL EVALUATES TO TRUE__

> In a boolean condition, JavaScript assigns the truthy value to a variable if you use the `||` operator in your assignment:
```javascript
let username = '';  
let defaultName = username || 'Stranger';
console.log(defaultName); // Prints: Stranger
```

## Ternary operator

```javascript
// (condition) ? true-statement : false-statement
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```

## Elseif statement

```javascript
if (season === 'spring') {
 console.log('It\'s spring! The trees are budding!');
} else if (season === 'winter') {
 console.log('It\'s winter! Everything is covered in snow.')
} else {
 console.log('Invalid season.');
}
```

## The switch keyword

```javascript
let athleteFinalPosition = 'first place';

switch (athleteFinalPosition){
 case 'first place':
	 console.log('You get the gold medal!')
	 break
 case 'second place':
	 console.log('You get the silver medal!')
	 break
 case 'third place':
	 console.log('You get the bronze medal!')
	 break
 default:
	 console.log('No medal awarded.')
	 break
}
```

# Functions

In javascript there are many ways to declare a function. One possible way is by this:

```javascript
function greetWorld(){
	console.log('Hello World!');
}
```

> Be aware of the _hoisting_ feature in JavaScript which allows access to function declarations before they’re defined. FUCK YEAA.

```javascript
greetWorld();

function greetWorld(){
	console.log('Hello World!');
}
```

## Parameters and Arguments

> There's a difference between parameters and arguments.
>
> **Parameter**: Parameter are _variables_ passed into a function; (it is usually when _Defining a function_)
> **Arguments**: The _values_ that are passed into a function when it is called; `greetWorld("Hello","World")`

## Default Parameters
> Default parameters allow parameters to have a predetermined value in case there is no argument passed into the function or if the argument is `undefined` when called.

> ```javascript
> function greeting (name = 'stranger') {  
>  console.log(`Hello, ${name}!`)  
> }  
>   
> greeting('Nick') // Output: Hello, Nick!  
> greeting() // Output: Hello, stranger!
> ```

> If in case you want to give value to 1, 3 but want to keep the 2nd variable _default_. You can use `undefined` for the 2nd variable
```javascript
function makeShoppingList(item1='milk', item2='bread', item3='eggs'){
 console.log(`Remember to buy ${item1}`);
 console.log(`Remember to buy ${item2}`);
 console.log(`Remember to buy ${item3}`);
}
makeShoppingList('almonds',undefined,'chicken')
```

## Return

```javascript

const numOfMonitors = monitorCount(5,4)

function monitorCount(rows, columns){
 return rows*columns
}
console.log(numOfMonitors)
```

### Helper Functions

We can use the return value of 1 function in the return value of another.

```javascript
function multiplyByNineFifths(number) {  
	return number * (9/5);
};

function getFahrenheit(celsius) {  
	return multiplyByNineFifths(celsius) + 32;
}; 

getFahrenheit(15); // Returns 59
```

## Function Expressions

Oooh! Here comes the second way of defining functions.

```JAVASCRIPT
const functionName = function(parameter1, parameter2) { // function is the actual keyword to be used.
	// lines of a function
	return // not necessary
}

// To call this function you call it by it's variable name.

functionName(argument1,argument2)

```

> NOTE THAT FUNCTION EXPRESSIONS ARE NOT HOISTED. SO YOU CANNOT CALL THE `functionName` BEFORE IT'S DEFINITION.

## Arrow Functions

HOO HOO HOO!! The third type.
Arrow functions remove the need to type out the keyword `function` every time you need to create a function. (Even better lol)

```javascript
const functionName = (parameter1, parameter2) => {  
	// code here  
	return // not necessary
};
```

### Concise Body Arrow Functions

Ooohhooo. This just keeps getting better.
 
> The most condensed form of the function is known as _concise body_. (In short, the shorter the function the better.)

- Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a function takes zero or multiple parameters, parentheses are required.
```javascript
// Zero Parameters
const functionName = () => {};

// One Parameters
const functionName = parameter1 => {};

// Two or more parameters
const functionName = (parameter1,parameter2) => {};
```

- _A function body composed of a single-line block does not need curly braces_. Without the curly braces, whatever that line evaluates will be automatically returned. The contents of the block should immediately follow the arrow `=>` and the `return` keyword can be removed. This is referred to as __implicit return__.

```javascript
// One parameter and one line of code inside the function
const sumNumbers = number => number + number;
```

> Note the `return` keyword has been removed since the function consists of a single-line block 

# Scope
Defining the scope of a variable and other stuff
## Blocks and Scope

A block is set of instructions defined in `{}`. A function has a block, an if statement has a block.

> It is preferable to have one variable outside of a block and the other inside of a block, because it will then be global and thus can be accessed by any piece of code.

## Global Scope
In _global scope_, variables are declared outside of blocks. Thus are termed as _global variables_

## Block Scope
This is where the defined variables are known as _local variables_

## Scope Pollution
It seems like if you change the value of a global variable in any _block_ it changes it's value globally. 

```javascript
let num = 50;  
  
const logNum = () => {  
 num = 100; // Take note of this line of code  
 console.log(num);  
};  
  
logNum(); // Prints 100  
console.log(num); // Prints 100
```
This is also known as _scope pollution_.
- The solution to this problem is use `let num = 100` in the _block code_. 
	- That way a new variable called `num` will be assigned in the block. Even tho `num` is already assigned to a value in global namespace, we will have a second instance of `num` in the local namespace.

> Note that re-assignment of a (new for the local block) variable is not throwing error. __MAKE SURE TO NOTE THAT CHANGING OF GLOBAL VARIABLES IS PERMITTED IN THE LOCAL BLOCK.__

## Practice Good scoping
Again to prevent scope pollution use `let` to define variables inside a local scope by practice.

# Arrays

The classic way of defining arrays:

```javascript
let newYearsResolutions = ['Keep a journal', 'Take a falconry class', 'Learn to juggle'];
```

> An array can hold different data types.

## Accessing Elements

*There was an image here*

> You can also access individual characters in a string.
> 
> ```javascript
> const mystring = 'hello world'
> console.log(mystring[6]) // will print out 'w'
> ```

- If you try to access an index that is beyond the last element then it states `undefined`.

## Updating Elements

```javascript
let seasons = ['Winter', 'Spring', 'Summer', 'Fall'];  
  
seasons[3] = 'Autumn';  
console.log(seasons);  
//Output: ['Winter', 'Spring', 'Summer', 'Autumn']
```

## Arrays with let and const

Note that arrays defined with let can be changed and re-assigned. But the arrays defined with `const` can be changed BUT CAN'T BE RE-ASSIGNED.
- Meaning:

```javascript
const cars = ['toyota','bmw','ferrari']
cars[2] = 'maruti' // Executes correctly

cars = ['maruti'] // throws an error because const arrays cannot be re-defined.
```

## The .length property

`console.log(myarray.length) // prints length of myarray`

## The .push() method
This method is used to add items at the end of an array.

```javascript
const itemlist = ['','','']

itemlist.push('','') // yes this can take single or multiple arguments.
```

> You might also see `.push()` referred to as a _destructive_ array method since it changes the initial array.

## The .pop() method

Removes the last item from the array. 
- After popping the element from the array _it saves the array with the same name_ and returns the popped item
```javascript
const newItemTracker = ['item 0', 'item 1', 'item 2']; 
const removed = newItemTracker.pop(); 
console.log(newItemTracker); // Output: [ 'item 0', 'item 1' ]console.log(removed);// Output: item 2
```

## More array methods

Some arrays methods that are available to JavaScript developers include: `.join()`, `.slice()`, `.splice()`, `.shift()`, `.unshift()`, and `.concat()` amongst many others.

- shift() - removes the element in the begginning of an array
- unshift( arg) - adds the item or 2 (can take multiple) at the beginning of an array. It needs an argument. `arrat.unshift('hello','world',69)`
- slice(arg1, \[arg2\]) - returns a part of an array in a new array object. `array.slice(2)// will display all the elements from 3rd element onwards(including 3rd); array.slice(2,4) // will display all the elements from 3rd element on and before the 5th element (not including 5)`
- .splice(index, \[remove any element? specify how many\], \[arg3\], \[arg4\]): edit an array. This is little complex to understand.
	- *index* makes it place the pointer at the index. 
	- *remove any element* part specifies whether you want to remove any element from the array if any number is given it removes that many elements. This is optional.
	- then following *arg3, arg4* are the elements that has to be newly added to the array ON THAT PARTICULAR *index*.
- indexOf(arg, \[numOfOccurence\]) - Returns the first index at which the given argument can be found (if not found -1 is returned). Say if you want to find the index of 2,3,4th occurence and so on occurence. `array.indexOf('pasta',3)` will give out the index of 3rd occurence of 'pasta' string in the array.

## Nested Arrays
Uk the drill... Go on. To access elements in nested arrays chain indices using bracket notation.

# Loops

## The For loop

```javascript
for (let counter = 0; counter < 4; counter++) {  
 console.log(counter);  
}
```

## Looping Through Arrays
```javascript
const vacationSpots = ['Bali', 'Paris', 'Tulum'];

for (let i = 0 ; i < vacationSpots.length; i++){
 console.log(`I would love to visit ${vacationSpots[i]}`);
}
```

## while loop

```javascript
let counterTwo = 1;  
while (counterTwo < 4) {  
 console.log(counterTwo);  
 counterTwo++;
}
```

## do-while statements

Hellow, brother! Long time no see huh!
```javascript
let countString = '';
let i = 0; 
do {  
countString = countString + i;  
i++;
} while (i < 5); 
console.log(countString);
```

## The break keyword
```javascript
for (let i = 0; i < 99; i++) {  
 if (i > 2 ) {  
 break;  
 }  
 console.log('Banana.');  
}
```

# Higher Order Functions
A _higher-order function_ is a function that either accepts functions as parameters, returns a function, or both!

Abstraction: Long-story-short assign meaningful names to function, so that code readability++

## Function as Data
In javascript you can re-assign a function as variables and use that variable to reference to that particular function.
```javascript
var announceThatIAmDoingImportantWork = () => console.log('I\'m doing some important shit').
const busy = announceThatIAmDoingImportantWork; 
busy(); // This function call barely takes any space!
```

> In JavaScript, functions are _first class objects_. This means that, like other objects you’ve encountered, JavaScript functions can have properties and methods. (props like .length / .name; methods like toString())

## Function as parameters
- We call the functions that get passed in as parameters and invoked _callback functions_ because they get called during the execution of the higher-order function.

```javascript
const timeFuncRuntime = funcParameter => {  
 let t1 = Date.now();  
 funcParameter();  
 let t2 = Date.now();  
 return t2 - t1;  
}  
  
const addOneToOne = () => 1 + 1;  
  
timeFuncRuntime(addOneToOne);
```

- We invoked `timeFuncRuntime()` first with the `addOneToOne()` function as parameter - note how we passed in `addOneToOne` and did not invoke it.

> When we pass a function in as an argument to another function, we don’t invoke it. Invoking the function would evaluate to the return value of that function call. SO JUST CALL THE FUNCTION NAME WITHOUT THE PARANTHESIS.

## Anonymous Functions as arguments

```javascript
timeFuncRuntime(() => {  
	for (let i = 10; i>0; i--){
		console.log(i);  
}
});
```

Here you can see an _anonymous function_ passed as an argument. YESSS ANONYMOUS FUNCTIONS CAN BE ARGUMENTS TOO... This just makes javascript too complicated... But smart. No wonder how javascript obfuscation is a thing.

# Iterators
## forEach() function

- `.forEach()` function loops through the given array.
- It takes in a *callback function* (A function that is being passed as an argument to another function).
- `forEach()` loops through the array and executes the callback function for each element.
```javascript
groceries = ['brown sugar','salt','craneberries','walnuts']

groceries.forEach(function(a){console.log(' - '+ a);});
```

- You can also use the ARRAY FUNCTIONS within .forEach()

```javascript
groceries.forEach(groceryItem => console.log(groceryItem));
```

- We can also define a function beforehand to be used as the callback function.

```javascript
function printGrocery(element){
	console.log(element);
} 

groceries.forEach(printGrocery);
```

## .map() function

- This function is called on an array (with a callback function as an argument) and returns a new array.

```javascript
const numbers = [1, 2, 3, 4, 5];  
const bigNumbers = numbers.map(number => {  return number * 10;});
```

> The only difference between .map() and .forEach() is .map() returns a new array.

## .filter() function

- Like `.map()` function `.filter()` also returns an array. However it filters out certain elements out of it.
	- To put the element to the new array the callback function has to `return true`

```javascript
const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door'];  
const shortWords = words.filter(word => {  return word.length < 6;})
```

## .findIndex() function
- This function returns the index of the first element that `return true`.
	- It returns a `number` value in the variable.
	- Note that the loop in the callback function is checking through the element and returned value into the variable is the index of that element that evaluates to true.

```javascript
const jumbledNums = [123, 25, 78, 5, 9];  
const lessThanTen = jumbledNums.findIndex(num => {  return num < 10;});
```

- If the element is not present in the index it return `-1`

## .reduce() function
