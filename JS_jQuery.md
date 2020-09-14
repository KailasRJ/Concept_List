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
