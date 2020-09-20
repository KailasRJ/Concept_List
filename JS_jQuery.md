# NEOITO TRAINING

# JS Concept List and Fundamentals

# Running Javascript
## Script tags

The Script tag is used to embed a client-side script (JavaScript). The script element either contains scripting statements, or it points to an external script file through the src attribute.

```javascript

<script>
document.getElementById("trial").innerHTML = "NEOITO";
</script>

```
___

## Browser console
Js also can be written on the console in the web browser

```javascript

function add(num1, num2) {
  return num1 + num2;
}
add(2,3);

```
---
## Link external file
It can also be written in another seperate file and can be called in whatever file we want.
```javascript
<script src="script.js"></script>
```
---
# Variables
## Declarations
Declarations are used to declare varriables in js and there are of mainly 3 types

* var
* let
* const

### var
Var declarations are globally scoped or function/locally scoped. The scope is global when a var variable is declared outside a function. This means that any variable that is declared with var outside a function block is available for use in the whole window.

var is function scoped when it is declared within a function. This means that it is available and can be accessed only within that function.

```javascript
var demo= "Neoito training";
    function NotInScope() {
        var hello = "hello";
    }
    console.log(hello); //error:undefined

```

>var variables can be  **re-declared** / **updated**

### let

Just like var, a variable declared with let can be updated within its scope. Unlike var, 

>a let variable cannot be **re-declared** within its scope. 

```javascript
  let greeting = "say Hi";
  let greeting = "say Hello instead"; // error: Identifier 'greeting' has already been declared
```
### const
Variables declared with the const maintain constant values. const declarations share some similarities with let declarations. Like let declarations, const declarations can only be accessed within the block they were declared. 

>it cannot be __re-declared__ / **updated**

```javascript
const greeting = "say Hi";
greeting = "say Hello instead";// error: Assignment to constant variable not possible again. 
```

# Scope

## Global

A variable declared outside a function, becomes GLOBAL. A global variable has global scope: All scripts and functions on a web page can access it

## Function

Each function creates a new scope. Scope determines the accessibility (visibility) of these variables. Variables defined inside a function are not accessible (visible) from outside the function.

## Block
A block scope is the area within if, switch conditions or for and while loops. const and let keywords allow to declare variables in the block scope, which means those variables exist only within the corresponding block


# Data Types and Data structures

## Primitive Types

Data that is not an object and has no methods and below are the primitve data types in js

## undefined
The undefined type is a primitive type that has one special value undefined . By default, when a variable is declared but not initialized, it is assigned the value of undefined .
```javascript
var undef; //If a value is never assigned, any output will be 'undefined'
```

## Boolean
These are yes/no type
```javascript
var isReading = true; //Yes, I'm reading
var isSleeping = false; //No, I'm not sleeping
```
## Number
Number type
```javascript
var num = 25; //Integer
var flo = 80.5; //Floating-point number
var exp = 4.25e+6; //Exponential notation, this equates to 4250000
```
## BigInt
The BigInt type is a numeric primitive in JavaScript that can represent integers with arbitrary precision
```javascript
const theBiggestInt = 9007199254740991n
const alsoHuge = BigInt(9007199254740991) // 9007199254740991n
const hugeString = BigInt("9007199254740991") // 9007199254740991n
```
## String
String type
```javascript
var strSingle = 'John'; //String with single quotes
var strDouble = "Bob"; //String with double quotes
```

## Symbol

To create a new primitive symbol, you write Symbol() with an optional string as its description: Once you create a symbol, its value is kept private and for internal use
```javascript
let sym1 = Symbol()
let sym2 = Symbol('foo')
//cant create a symbol object like this
let sym = new Symbol()  // TypeError
//it can be archieved by
let sym = Symbol('foo')
typeof sym      // "symbol" 
let symObj = Object(sym)
typeof symObj   // "object"
```
## null
In JavaScript null is "nothing". It is supposed to be something that doesn't exist. Unfortunately, in JavaScript, the data type of null is an object
```javascript
var noValue = null; //Null meaning that it is has no value, not the same as 0 or ""
```
## Object
An object contains properties, defined as a key-value pair. A property key (name) is always a string, but the value can be any data type, like strings, numbers, booleans, or complex data types like arrays, function and other objects
```javascript
var emptyObject = {};
var person = {"name": "Kailas", "surname": "RJ", "age": "22"}; 
var car = { 
	model: "Zen Esteelo", 
	color: "pink",
	doors: 5
}
```

## Function
```javascript
var func = function() { //Calling the function: func();
  alert("Code excuted"); //Outputs: Code executed
}

var funcVar = function(amount) { //Calling the function: funcVar(6); 
  alert("Code excuted " + amount + " times"); //Outputs: Code executed 6 times (if input was 6)
}
```
# Data Structures
Data structures, at a high level, are techniques for storing and organizing data that make it easier to modify, navigate, and access. Data structures determine how data is collected, the functions we can use to access it, and the relationships between data

## Array
An array is a special variable, which can hold more than one value at a time.

### creating an array
```javascript
var cars = [
  "Saab",
  "Volvo",
  "BMW"
];
var cars = ["Saab", "Volvo", "BMW"];
```

## Array methods

### concat()

The concat() method is used to join two or more arrays.
```javascript
var hege = ["Cecilie", "Lone"];
var stale = ["Emil", "Tobias", "Linus"];
var children = hege.concat(stale);
```

### filter()

The filter() method creates an array filled with all array elements that pass a test (provided as a function).filter() does not change the original array.
```javascript
var ages = [32, 33, 16, 40];

function checkAdult(age) {
  return age >= 18;
}

console.log(ages.filter(checkAdult))
```

### find()

The find() method returns the value of the first element in an array that pass a test (provided as a function).

The find() method executes the function once for each element present in the array:

If it finds an array element where the function returns a true value, find() returns the value of that array element (and does not check the remaining values) Otherwise it returns undefined. find() does not execute the function for empty arrays. find() does not change the original array.
```javascript
var ages = [3, 10, 18, 20];

function checkAdult(age) {
  return age >= 18;
}

console.log(ages.find(checkAdult);)
```

### include()

The includes() method determines whether an array contains a specified element. This method returns true if the array contains the element, and false if not. The includes() method is case sensitive.
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var n = fruits.includes("Mango");
console.log(n) //true
```
### from()

The Array.from() method returns an Array object from any object with a length property or an iterable object
```javascript
var myArr = Array.from("ABCDEFG");
console.log(myArr) //A,B,C,D,E,F,G
```

### indexof()

The indexOf() method searches the array for the specified item, and returns its position.

The search will start at the specified position, or at the beginning if no start position is specified, and end the search at the end of the array.

Returns -1 if the item is not found.

If the item is present more than once, the indexOf method returns the position of the first occurence.
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var a = fruits.indexOf("Apple"); 
console.log(a) //2
```

# Type Conversion
## Explicite Conversion
Converting data types as per our requirement For example, String conversion
```javascript
let value = true;
alert(typeof value); // boolean

value = String(value); // now value is a string "true"
alert(typeof value); // string
```

## implicite Conversion
Convert automatically to the required data type.Most of the time, operators and functions automatically convert the values given to them to the right type. For example, alert automatically converts any value to a string to show it

## Equality
```javascript
== vs ===
```

Triple equal -> Strict equality compares two values for equality. Neither value is implicitly converted to some other value before being compared. If the values have different types, the values are considered unequal.
```javascript
var num = 0;
var obj = new String('0');

console.log(num === num); // true
console.log(num === obj); // false
```

Double equal -> Loose equality compares two values for equality, after converting both values to a common type. After conversions (one or both sides may undergo conversions), the final equality comparison is performed exactly as === performs
```javascript
var num = 0;
var obj = new String('0');

console.log(num === num); // true
console.log(num === obj); // true
```

# Loops
## break/continue
## for..in
for/in loops are used to find something that are to be finded from the collection of data we have
```javascript
var person = {fname:"John", lname:"Doe", age:25};

var text = "";
var x;
for (x in person) {
  text += person[x] + " ";
} //output : joe Doe 25
```

## for..of
The for...of statement creates a loop iterating over iterable objects in the array
```javascript
const array1 = ['a', 'b', 'c'];

for (const element of array1) {
  console.log(element);
}
//  output: "a"
//  output: "b"
//  output: "c"
```

# Control Flow
## try/catch/throw
It is used for exception handling.

The try statement lets you test a block of code for errors.

The catch statement lets you handle the error.

The throw statement lets you create custom errors.

The finally statement lets you execute code, after try and catch, regardless of the result.
```javascript
try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
finally {
  Block of code to be executed regardless of the try / catch result
}
```

# Expressions & Operaters
## Comparision Operaters
## = = (Equal)
Checks if the value of two operands are equal or not, if yes, then the condition becomes true.

Ex: (A == B) is not true.

## != (Not Equal)
Checks if the value of two operands are equal or not, if the values are not equal, then the condition becomes true.

Ex: (A != B) is true.

## > (Greater than)
Checks if the value of the left operand is greater than the value of the right operand, if yes, then the condition becomes true.

Ex: (A > B) is not true.

## < (Less than)
Checks if the value of the left operand is less than the value of the right operand, if yes, then the condition becomes true.

Ex: (A < B) is true.

# Functions
## Arrow Functions
Arrow functions allow us to write shorter function syntax:
```javascript
//Normal
hello = function() {
  return "Hello World!";
}
//Arrow
hello = () => {
  return "Hello World!";
}
//or 
hello = () => "Hello World!";
//with parameter
hello = val => "Hello " + val;
```

## this in arrow fucntion
The handling of this is also different in arrow functions compared to regular functions. In short, with arrow functions there are no binding of this. In regular functions the this keyword represented the object that called the function, which could be the window, the document, a button or whatever. With arrow functions the this keyword always represents the object that defined the arrow function.
```javascript
//Regular Function:
//here when it run first it will be a window object and when a buton click ,it  will be of btn object
hello = function() {
  document.getElementById("demo").innerHTML += this;
}
//The window object calls the function:
window.addEventListener("load", hello);
//A button object calls the function:
document.getElementById("btn").addEventListener("click", hello)
;

//Arrow Function:
//here this  keyword represents the object that owns the function, no matter who calls the function.
hello = () => {
  document.getElementById("demo").innerHTML += this;
}
//The window object calls the function:
window.addEventListener("load", hello);
//A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
```
## Closure

Closure is a special feature of Javascript that allows infinite number of functions from a function, because it can store the variable values as an object variable inside a special closure variable. it would be clear after the following example.
 ```javascript
var addTo = function(passed) {

  var add = function(inner){
    return passed + inner;
  };

  return add;
};
var addThree = new addTo(3);
var addFour = new addTo(4);

console.log(addThree(1));
console.log(addFour(1));

 ```
In this example, the value of passed is stored inside a special closure variable and when we create a new addThree and addFour function, it takes the value of the passed from the stored closure element.


## Currying

A curryable function is a function that takes every argument by itself and then just returns a new function that expects the next dependency of the function until all dependencies have been fulfilled

```javascript
let dragon = 
  name =>
    size =>
      element =>
         name + 'is a' +
         size + 'dragon that breathes' +
         element + '!'

 let output = dragon('Fluffy')('tiny')('lightning')
```
## this

The JavaScript this keyword refers to the object it belongs to.

this in a Method

```javascript
var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```
>this refers to the person object.
The person object is the owner of the fullName method.

this Alone

```javascript
var x = this;
```

 >Here, the owner is the Global object, so this refers to the Global object. [object Window]

this in Event Handlers

```javascript
<button onclick="this.style.display='none'">
  Click to Remove Me!
</button>
```
>this refers to the HTML element that received the event


## Explicit Function Binding


The call() and apply() methods are predefined JavaScript methods.

They can both be used to call an object method with another object as argument.

```javascript
var First = {
  fullName: function() {
    return this.firstName + this.lastName;
  }
}
var Second = {
  firstName:"Neo",
  lastName: "ito",
}
person1.fullName.call(person2);  // Will return "Neoito"

```
Will return the firstname and last name of Second even though it is method of First.

## Prototypes

```javascript
function Student() {
    this.name = 'John';
    this.gender = 'M';
}

Student.prototype.age = 15;

var studObj1 = new Student();
alert(studObj1.age); // 15

var studObj2 = new Student();
alert(studObj2.age); // 15
```
The prototype object is special type of enumerable object to which additional properties can be attached to it which will be shared across all the instances of it's constructor function.

![prototype](https://www.tutorialsteacher.com/Content/images/oo-js/prototype-2.png)

## Prototype Inheritance

```javascript
let animal = {
  eats: true,
  walk() {
    alert("Animal walk");
  }
};

let rabbit = {
  jumps: true,
  __proto__: animal
};

let longEar = {
  earLength: 10,
  __proto__: rabbit
};

// walk is taken from the prototype chain
longEar.walk(); // Animal walk
alert(longEar.jumps); // true (from rabbit)
```
 When we want to read a property from object, and it’s missing, JavaScript automatically takes it from the prototype. In programming, such thing is called “prototypal inheritance”. 

 The object longEar inherits the properties of rabbit, which inturn inheritants properties of animal. Hence such a long chain of prototypes can be formed.

## Class

Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.

Class declarations

```javascript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

Here the Declaration is "Rectangle".

Class Expressions

```javascript
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```
Always add the constructor() method.

To create a class inheritance, use the extends keyword.

```javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it is a ' + this.model;
  }
}

mycar = new Model("Ford", "Mustang");
document.getElementById("demo").innerHTML = mycar.show();

```
>By calling the super() method in the constructor method, we call the parent's constructor method and gets access to the parent's properties and methods.

Getter and Setter

```javascript
class Car {
  constructor(brand) {
    this._carname = brand;
  }
  get carname() {
    return this._carname;
  }
  set carname(x) {
    this._carname = x;
  }
}

mycar = new Car("Ford");
mycar.carname = "Volvo";
document.getElementById("demo").innerHTML = mycar.carname;
```
It can be smart to use getters and setters for your properties, especially if you want to do something special with the value before returning them, or before you set them.

To add getters and setters in the class, use the get and set keywords.

## Iterators
In JavaScript an iterator is an object which defines a sequence and potentially a return value upon its termination.

Specifically, an iterator is any object which implements the Iterator protocol by having a next() method that returns an object with two properties:

value : 
The next value in the iteration sequence.

done : 
This is true if the last value in the sequence has already been consumed. If value is present alongside done, it is the iterator's return value.
```javascript
function makeRangeIterator(start = 0, end = Infinity, step = 1) {
    let nextIndex = start;
    let iterationCount = 0;

    const rangeIterator = {
       next: function() {
           let result;
           if (nextIndex < end) {
               result = { value: nextIndex, done: false }
               nextIndex += step;
               iterationCount++;
               return result;
           }
           return { value: iterationCount, done: true }
       }
    };
    return rangeIterator;
}
```

```javascript
const it = makeRangeIterator(1, 10, 2);

let result = it.next();
while (!result.done) {
 console.log(result.value); // 1 3 5 7 9
 result = it.next();
}

console.log("Iterated over sequence of size: ", result.value); // [5 numbers returned, that took interval in between: 0 to 10]

```

## Generator
Generator functions allows you to define an iterative algorithm by writing a single function whose execution is not continuous.

When a value is consumed by calling the generator's next method, the Generator function executes until it encounters the yield keyword.

```javascript
function* makeRangeIterator(start = 0, end = 100, step = 1) {
    let iterationCount = 0;
    for (let i = start; i < end; i += step) {
        iterationCount++;
        yield i;
    }
    return iterationCount;
}
```


## Event Loop

The event loop is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading. 

```javascript
const foo = () => console.log("First");
const bar = () => setTimeout(() => console.log("Second"), 500);
const baz = () => console.log("Third");

bar();
foo();
baz();

```

![event loop gif](https://res.cloudinary.com/practicaldev/image/fetch/s--BLtCLQcd--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://devtolydiahallie.s3-us-west-1.amazonaws.com/gif14.1.gif)

* We invoke bar. bar returns a setTimeout function.
* The callback we passed to setTimeout gets added to the Web API, the setTimeout function and bar get popped off the callstack.
* The timer runs, in the meantime foo gets invoked and logs First. foo returns (undefined),baz gets invoked, and the callback gets added to the queue.
* baz logs Third. The event loop sees the callstack is empty after baz returned, after which the callback gets added to the call stack.
* The callback logs Second.

## Asynchronous Javascript
JavaScript is a single-threaded programming language which means only one thing can happen at a time. That is, the JavaScript engine can only process one statement at a time in a single thread.

Imagine requesting some data from an API. Depending upon the situation the server might take some time to process the request while blocking the main thread making the web page unresponsive.

Using asynchronous JavaScript (such as callbacks, promises, and async/await), you can perform long network requests without blocking the main thread.

### setTimeout()
As we said before, setTimeout() executes a particular block of code once after a specified time has elapsed. 

In the following example, the browser will wait two seconds before executing the anonymous function, then will display the alert message :

```javascript
let myGreeting = setTimeout(function() {
  alert('Hello, Mr. Universe!');
}, 2000)
```

### setInterval()
This works in a very similar way to setTimeout(), except that the function you pass as the first parameter is executed repeatedly at no less than the number of milliseconds given by the second parameter apart, rather than once.

```javascript
function displayTime() {
   let date = new Date();
   let time = date.toLocaleTimeString();
   document.getElementById('demo').textContent = time;
}

const createClock = setInterval(displayTime, 1000);
```

### Callback

```javascript
function loadAsset(url, type, callback) {
  let xhr = new XMLHttpRequest();
  xhr.open('GET', url);
  xhr.responseType = type;

  xhr.onload = function() {
    callback(xhr.response);
  };

  xhr.send();
}

function displayImage(blob) {
  let objectURL = URL.createObjectURL(blob);

  let image = document.createElement('img');
  image.src = objectURL;
  document.body.appendChild(image);
}

loadAsset('coffee.jpg', 'blob', displayImage);
```

Here we create a displayImage() function that simply represents a blob passed to it as an object URL, then creates an image to display the URL in, appending it to the document's <body>. However, we then create a loadAsset() function that takes a callback as a parameter, along with a URL to fetch and a content type. It uses XMLHttpRequest (often abbreviated to "XHR") to fetch the resource at the given URL, then pass the response to the callback to do something with. In this case the callback is waiting on the XHR call to finish downloading the resource (using the onload event handler) before it passes it to the callback.

### Promises
A promise is an object that wraps an asynchronous operation and notifies when it’s done. This sounds exactly like callbacks, but the important differences are in the usage of Promises. Instead of providing a callback, a promise has its own methods which you call to tell the promise what will happen when it is successful or when it fails. The methods a promise provides are “then(…)” for when a successful result is available and “catch(…)” for when something went wrong.

```javascript
someAsyncOperation(someParams)
.then(function(result){
    // Do something with the result
})
.catch(function(error){
    // Handle error
});
```
* The creation of a Promise object is done via the Promise constructor by calling “new Promise()”. 
*  It takes a function as an argument and that function gets passed two callbacks: one for notifying when the operation is successful (resolve) and one for notifying when the operation has failed (reject). 

* We can wrap a callback based asynchronous operation with a Promise like this:
```javascript

function getAsyncData(someValue){
    return new Promise(function(resolve, reject){
        getData(someValue, function(error, result){
            if(error){
                reject(error);
            }
            else{
                resolve(result);
            }
        })
    });
}
```

## Async/Await

Async/Await is the next step in the evolution of handling asynchronous operations in JavaScript. It gives you two new keywords to use in your code: “async” and “await”. Async is for declaring that a function will handle asynchronous operations and await is used to declare that we want to “await” the result of an asynchronous operation inside a function that has the async keyword.

```javascript
async function getSomeAsyncData(value){
    const result = await fetchTheData(someUrl, value);
    return result;
}
```
* Inside the scope of an async function you can use try/catch for error handling.


## Module System

A module is just a file. One script is one module. As simple as that.

Modules can load each other and use special directives export and import to interchange functionality, call functions of one module from another one:

* export keyword labels variables and functions that should be accessible from outside the current module.
* import allows the import of functionality from other modules.

In the beginning, Javascript did not have a way to import/export modules. This is a problem. Imagine writing your app in just one file.

Then, people much attempted to add modularity to Javascript. 

## CJS

CJS is short for CommonJS.

```javascript
//importing 
const doSomething = require('./doSomething.js'); 

//exporting
module.exports = function doSomething(n) {
  // do something
}
```
* CJS imports module synchronously.
* You can import from a library node_modules or local dir. Either by const myLocalModule = require('./some/local/file.js') or var React = require('react'); works.

* When CJS imports, it will give you a copy of the imported object.
* CJS will not work in the browser. It will have to be transpiled and bundled.

## ESM

ESM stands for EcmaScript Modules. It is Javascript's proposal to implement a standard module system.

![ESM](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/04_import_graph.png)

```javascript
// add.js
  export function add(r) {
    return r + r;
  }


  // index.js
  import add from "./add";
  add(4); // = 8
```
>ESM is the best module format thanks to its simple syntax, async nature, and tree-shakeability.

```javascript
import {foo, bar} from './myLib';

...

export default function() {
  // your Function
};
export const function1() {...};
export const function2() {...};
```

1. Construction — find, download, and parse all of the files into module records.

2. Instantiation —find boxes in memory to place all of the exported values in (but don’t fill them in with values yet).
Then make both exports and imports point to those boxes in memory. This is called linking.

3. Evaluation —run the code to fill in the boxes with the variables’ actual values.


> ES6 provides two ways to export a module from a file: named export and default export.

## Named Export

With named exports, one can have multiple named exports per file. Then import the specific exports they want surrounded in braces. The name of imported module has to be the same as the name of the exported module.

```javascript
// ex. importing multiple named exports
import { MyComponent, MyComponent2 } from "./MyComponent";

// exports from ./MyComponent.js file
export const MyComponent = () => {}
export const MyComponent2 = () => {}
```

## Default Export

One can have only one default export per file.

```javascript
// import
import MyDefaultComponent from "./MyDefaultExport";
// export
const MyComponent = () => {}
export default MyComponent;
```
---
---
---

* *Named exports are useful to export several values. During the import, one will be able to use the same name to refer to the corresponding value.*

* *Concerning the default export, there is only a single default export per module. A default export can be a function, a class, an object or anything else. This value is to be considered as the “main” exported value since it will be the simplest to import.*

## Web APIs
Web API is an API as the name suggests, it can be accessed over the web using the HTTP protocol. It is a framework that helps you to create and develop HTTP based RESTFUL services. 

Basically Web API is a web development concept. It is limited to Web Application’s client-side and also it does not include a web server or web browser details. 

If an application is to be used on a distributed system and to provide services on different devices like laptops, mobiles, etc then web API services are used. Web API is the enhanced form of the web application.

Web API is a System to System interaction, in which the data or information from one system can be accessed by another system, after the completion of execution the resultant data or we can say as output is shown to the viewer.

![Web APIs](https://media.geeksforgeeks.org/wp-content/uploads/20200517143318/WebAPI.jpg)

## XML HttpRequest

The XMLHttpRequest object can be used to request data from a web server.

* Update a web page without reloading the page
* Request data from a server - after the page has loaded
* Receive data from a server  - after the page has loaded
* Send data to a server - in the background

```javascript
var xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
       // Typical action to be performed when the document is ready:
       document.getElementById("demo").innerHTML = xhttp.responseText;
    }
};
xhttp.open("GET", "filename", true);
xhttp.send();
```
## Fetch API

fetch() allows you to make network requests similar to XMLHttpRequest (XHR). The main difference is that the Fetch API uses Promises, which enables a simpler and cleaner API, avoiding callback hell and having to remember the complex API of XMLHttpRequest.

```javascript
let promise = fetch(url, [options])
```
>First, the promise, returned by fetch, resolves with an object of the built-in Response class as soon as the server responds with headers.

```javascript
let response = await fetch(url);

if (response.ok) { // if HTTP-status is 200-299
  // get the response body (the method explained below)
  let json = await response.json();
} else {
  alert("HTTP-Error: " + response.status);
}
```
>Second, to get the response body, we need to use an additional method call.
```javascript
fetch('https://api.github.com/repos/javascript-tutorial/en.javascript.info/commits')
  .then(response => response.json())
  .then(commits => alert(commits[0].author.login));
```



---
---
---



# jQuery

The purpose of jQuery is to make it much easier to use JavaScript on your website.

```javascript
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
</head>
```
The jQuery syntax is tailor-made for selecting HTML elements and performing some action on the element(s).

Basic syntax is: $(selector).action()

```javascript
$(document).ready(function(){

  // jQuery methods go here...

});
```

This Document ready event is to prevent any jQuery code from running before the document is finished loading.

---

## jQuery Selectors

```javascript
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
    $("#test").hide();
    $(".test").hide();
  });
});
```
When a user clicks on a button, all `<p>` elements, the element with the id test and the elements with class name test will be hidden.

---

## jQuery Events

Example: 

* click()
* dblclick()
* mouseenter()
* mouseleave()
* mousedown()
* mouseup()
* hover()
* focus()
* blur()

## .on() Method

The on() method attaches one or more event handlers for the selected elements.

```javascript
$("p").on({
  mouseenter: function(){
    $(this).css("background-color", "lightgray");
  },
  mouseleave: function(){
    $(this).css("background-color", "lightblue");
  },
  click: function(){
    $(this).css("background-color", "yellow");
  }
});
```
---
## jQuery toggle()

This is a feauture used largly in webdevelopment.You can also toggle between hiding and showing an element with the toggle() method.

```javascript
$("button").click(function(){
  $("p").toggle();
});
```
---

## jQuery Fades

You can fade an element in and out of visibility.

* fadeIn()
* fadeOut()
* fadeToggle()
* fadeTo()

```javascript
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
});
```
---
## jQuery Sliding Methods

This is very useful to create drop down Nav bars.

* slideDown()
* slideUp()
* slideToggle()

```javascript
$("#flip").click(function(){
  $("#panel").slideToggle();
});
```
---
## jQuery animate()

This feauture is very useful for creating amazing web designs or creative cool artworks.

```javascript
$("button").click(function(){
  $("div").animate({
    left: '250px',
    opacity: '0.5',
    height: '150px',
    width: '150px'
  });
}); 

```
### Animating using the Internal queue.

```javascript
$("button").click(function(){
  var div = $("div");
  div.animate({height: '300px', opacity: '0.4'}, "slow");
  div.animate({width: '300px', opacity: '0.8'}, "slow");
  div.animate({height: '100px', opacity: '0.4'}, "slow");
  div.animate({width: '100px', opacity: '0.8'}, "slow");
}); 
```

---
## jQuery HTML feautures

jQuery has powerful methods for manipulating HTML elements.

* **text()** - Sets or returns the text content of selected elements
* **html()** - Sets or returns the content of selected elements (including HTML markup)
* **val()** - Sets or returns the value of form fields

```javascript
$("#btn1").click(function(){
  alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
  alert("HTML: " + $("#test").html());
});
$("button").click(function(){
  alert($("#w3s").attr("href"));
});
```
We can use the same methods to **Set** HTML contents.

```javascript
$("#btn1").click(function(){
  $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
  $("#test2").html("<b>Hello world!</b>");
});
$("#btn3").click(function(){
  $("#test3").val("Dolly Duck");
});
```

* Callback function

The callback function has two parameters: the index of the current element in the list of elements selected and the original (old) value.

```javascript
$("#btn1").click(function(){
  $("#test1").text(function(i, origText){
    return "Old text: " + origText + " New text: Hello world!
    (index: " + i + ")";
  });
});

$("#btn2").click(function(){
  $("#test2").html(function(i, origText){
    return "Old html: " + origText + " New html: Hello <b>world!</b>
    (index: " + i + ")";
  });
});
```

* Attributes - attr()

The jQuery attr() method is also used to set/change attribute values.

```javascript
$("button").click(function(){
  $("#w3s").attr({
    "href" : "https://www.w3schools.com/jquery/",
    "title" : "W3Schools jQuery Tutorial"
  });
});
```
---
## Adding elements in jQuery


* append() - Inserts content at the end of the selected elements
* prepend() - Inserts content at the beginning of the selected elements
* after() - Inserts content after the selected elements
* before() - Inserts content before the selected elements

```javascript
function afterText() {
  var txt1 = "<b>I </b>";                    // Create element with HTML 
  var txt2 = $("<i></i>").text("love ");     // Create with jQuery
  var txt3 = document.createElement("b");    // Create with DOM
  txt3.innerHTML = "jQuery!";
  $("img").after(txt1, txt2, txt3);          // Insert new elements after <img>
}
```
---
## Remove Elements in jQuery

* remove() - Removes the selected element (and its child elements)
* empty() - Removes the child elements from the selected element

```javascript
$("p").remove(".test, .demo");
```
removes all `<p>` elements with class="test" and class="demo".
---

## jQuery CSS

We are thus able to set different CSS options to a element upon performing certain function such as pressing of a button.

```javascript
$("p").css({"background-color": "yellow", "font-size": "200%"});
```
---
## jQuery Dimensions

jQuery has several options to return the dimensions of an element. 

* width()
* height()
* innerWidth()
* innerHeight()
* outerWidth()
* outerHeight()



```javascript

$(document).ready(function(){
  $("button").click(function(){
    var txt = "";
    txt += "Width of div: " + $("#div1").width() + "</br>";
    txt += "Height of div: " + $("#div1").height() + "</br>";
    txt += "Inner width of div: " + $("#div1").innerWidth() + "</br>";
    txt += "Inner height of div: " + $("#div1").innerHeight();
    $("#div1").html(txt);
  });
});

```

Returns the width, height, inner width, inner height of the div element.
