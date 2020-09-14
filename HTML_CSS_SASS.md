# NEOITO TRAINING

# HTML

HTML is the standard markup language for creating Web pages.

HTML describes the structure of a Web page
```javascript
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

* The ``<!DOCTYPE html>`` declaration defines that this document is an HTML5 document
* The ``<html>`` element is the root element of an HTML page
* The ``<head>`` element contains meta information about the HTML page
* The ``<title>`` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
* The ``<body>`` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
* The ``<h1>`` element defines a large heading
* The ``<p>`` element defines a paragraph

## The HTML Attributes
* The href attribute of ``<a>`` specifies the URL of the page the link goes to
* The src attribute of ``<img>`` specifies the path to the image to be displayed
* The width and height attributes of ``<img>` provide size information for images
* The alt attribute of ``<img>`` provides an alternate text for an image
* The style attribute is used to add styles to an element, such as color, font, size, and more
* The lang attribute of the ``<html>`` tag declares the language of the Web page
* The title attribute defines some extra information about an element.

## The href atttributes

* The ``<a>`` tag defines a hyperlink. The href attribute specifies the URL of the page the link goes to:
```javascript
<a href="https://www.w3schools.com">Visit W3Schools</a>
```

## HTML Text Formatting

* ``<b>`` - Bold text
* `<strong>` - Important text
* ``<i>`` - Italic text
* ``<em>`` - Emphasized text
* `<mark>` - Marked text
* `<small>` - Smaller text
* `<del>` - Deleted text
* `<ins>` - Inserted text
* `<sub>` - Subscript text
* `<sup>` - Superscript text

## HTML Images Syntax
The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag has two required attributes:

src - Specifies the path to the image
alt - Specifies an alternate text for the image
Syntax
```javascript
<img src="url" alt="alternatetext">
```
## Define an HTML Table

The `<table>` tag defines an HTML table.

Each table row is defined with a `<tr>` tag. Each table header is defined with a `<th>` tag. Each table data/cell is defined with a `<td>` tag.

By default, the text in `<th>` elements are bold and centered.

By default, the text in `<td>` elements are regular and left-aligned.

```javascript
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>

```
## HTML List Tags

* `<ul>`	Defines an unordered list
* `<ol>`	Defines an ordered list
* `<li>`	Defines a list item
* `<dl>`	Defines a description list
* `<dt>`	Defines a term in a description list
* `<dd>`	Describes the term in a description list

```javascript
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
## Block and Inline

A block-level element always starts on a new line and takes up the full width available
An inline element does not start on a new line and it only takes up as much width as necessary
The `<div>` element is a block-level and is often used as a container for other HTML elements
The `<span>` element is an inline container used to mark up a part of a text, or a part of a document

```javascript
<div>Hello World</div>

<span>Hello World</span>
```

### Div

The `<div>` element is often used as a container for other HTML elements.

The `<div>` element has no required attributes, but style, class and id are common.

```javascript
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div>
```
### Span
The `<span>` element is an inline container used to mark up a part of a text, or a part of a document.

The `<span>` element has no required attributes, but style, class and id are common.
```javascript
<p>My mother has <span style="color:blue;font-weight:bold">blue</span> eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes </p>
```

* The HTML class attribute specifies one or more class names for an element.

* Classes are used by CSS and JavaScript to select and access specific elements.

```javascript
<h2 class="city">Paris</h2>
<p class="city">Paris is the capital of France</p>
```
### Id
* The id attribute is used to specify a unique id for an HTML element.

* The value of the id attribute must be unique within the HTML document

```javascript
<h2 id="C4">Chapter 4</h2>
```
# HTML Layout

![Block diagram](https://www.w3schools.com/html/img_sem_elements.gif) 

* `<header>` - Defines a header for a document or a section
* `<nav>` - Defines a set of navigation links
* `<section>` - Defines a section in a document
* `<article>` - Defines an independent, self-contained content
* `<aside>` - Defines content aside from the content (like a sidebar)
* `<footer>` - Defines a footer for a document or a section
* `<details>` - Defines additional details that the user can open and close on demand
* `<summary>` - Defines a heading for the `<details>` element

# HTML Responsive Web Design

Responsive web design is about creating web pages that look good on all devices!

A responsive web design will automatically adjust for different screen sizes and viewports.

We will discuss more on it in the CSS section

## HTML Forms

An HTML form is used to collect user input. The user input is most often sent to a server for processing.


* `<input type="text">`	Displays a single-line text input field
* `<input type="radio">`	Displays a radio button (for selecting one of many choices)
* `<input type="checkbox">`	Displays a checkbox (for selecting zero or more of many choices)
* `<input type="submit">`	Displays a submit button (for submitting the form)
* `<input type="button">`	Displays a clickable button

```javascript
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```
---
---
---


# CSS

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

```javascript
body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```
![syntax](https://www.w3schools.com/css/selector.gif)

## CSS Selectors
* .class :- Selects all elements with class="intro"
* #id	 #firstname	:- Selects the element with id="firstname"
* `*` :- Selects all elements
* p :- Selects all `<p>` elements
* element,element,..	div, p	Selects all `<div>` elements and all `<p>` elements
## Color
```javascript
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>
<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">Ut wisi enim...</p>
```

## Opacity

```javascript
div {
  background-color: green;
  opacity: 0.3;
}
```

## Margin and Padding

![margin and padding](https://mdn.mozillademos.org/files/8685/boxmodel-(3).png)

* The **content area**, bounded by the content edge, contains the "real" content of the element, Its dimensions are the content width (or content-box width) and the content height (or content-box height). 

* The **padding area**, bounded by the padding edge, extends the content area to include the element's padding. Its dimensions are the padding-box width and the padding-box height.

* The thickness of the padding is determined by the padding-top, padding-right, padding-bottom, padding-left, and shorthand padding properties.

* The **border area**, bounded by the border edge, extends the padding area to include the element's borders. Its dimensions are the border-box width and the border-box height.

* The **margin area**, bounded by the margin edge, extends the border area to include an empty area used to separate the element from its neighbors. Its dimensions are the margin-box width and the margin-box height.

* The size of the margin area is determined by the margin-top, margin-right, margin-bottom, margin-left, and shorthand margin properties.

## The position Property

The position property specifies the type of positioning method used for an element.

There are five different position values:

* static
* relative
* fixed
* absolute
* sticky

![position](https://www.cleonix.com/blog/wp-content/uploads/2019/03/blog-15-03-1.png)



## CSS 2D Transforms Methods

With the CSS transform property you can use the following 2D transformation methods:

* translate()
* rotate()
* scaleX()
* scaleY()
* scale()
* skewX()
* skewY()
* skew()
* matrix()

CSS 3D Transforms Methods

With the CSS transform property you can use the following 3D transformation methods:

* rotateX()
* rotateY()
* rotateZ()

## CSS Transitions


![transition](https://miro.medium.com/max/700/1*_6MfwckxNfQTca9SiG8MdQ.png)

* **transition**	A shorthand property for setting the four transition properties into a single property
* **transition-delay**	Specifies a delay (in seconds) for the transition effect
* **transition-duration**	Specifies how many seconds or milliseconds a transition effect takes to complete
* **transition-property**	Specifies the name of the CSS property the transition effect is for
* **transition-timing-function**	Specifies the speed curve of the transition effect

The transition-timing-function property can have the following values:

* **ease** - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
* **linear** - specifies a transition effect with the same speed from start to end
* **ease-in** - specifies a transition effect with a slow start
* **ease-out** - specifies a transition effect with a slow end
* **ease-in-out** - specifies a transition effect with a slow start and end
* **cubic-bezier(n,n,n,n)** - lets you define your own values in a cubic-bezier function.


## CSS Animations

When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.


```javascript
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
  animation-iteration-count: 3;
  animation-direction: reverse;
}

@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}
```
```javascript
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}
```
# CSS Flexbox

The flex container properties are:

* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

### Flex- Direction
The flex-direction property defines in which direction the container wants to stack the flex items. it can be either Row or Column.

```javascript
.flex-container {
  display: flex;
  flex-direction: column;
}
```
![flex1](https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2015/02/flex-direction-illustration.jpg)



### Flex Wrap
The flex-wrap property controls whether the flex container is single-line or multi-line, and the direction of the cross-axis, which determines the direction new lines are stacked in.
```javascript
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```

![flex2](https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2014/10/flex-wrap-illustration.jpg)

### justify-content

The justify-content property aligns flex items along the main axis of the current line of the flex container.

```javascript
.flex-container {
  display: flex;
  justify-content: center;
}
```
![flex3](https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2014/10/justify-content-illustration.jpg)

### Align-items

The align-items property is similar to the justify-content property, but instead of aligning flex items in the main axis, align-items is used to align flex items in the cross-axis (perpendicular to the main axis).

![flex 4](https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2014/10/align-items-illustration.jpg)

### Flex Basis

The flex-grow property sets the flex grow factor of a flex item. A flex grow factor is a <number> which determines how much the flex item will grow relative to the rest of the flex items in the flex container when positive free space is distributed. 

The flex-shrink property sets the flex shrink factor of a flex item. A flex shrink factor is a <number> which determines how much the flex item will shrink relative to the rest of the flex items in the flex container when negative free space is distributed.

The flex-basis property takes the same values as the width property, and sets the flex basis: the initial main size (see concepts and terminology) of the flex item, before free space is distributed according to the flex factors (see flex-shrink and flex-grow).

>check out this link to grab a better understanding of the various properties:  [Different Flex properties](https://codepad.co/snippet/properties-for-the-flexbox-container)




## Media Queries

Media queries can be used to check many things, such as:

* width and height of the viewport
* width and height of the device
* orientation (is the tablet/phone in landscape or portrait mode?)
resolution

Using media queries are a popular technique for delivering a tailored style sheet to desktops, laptops, tablets, and mobile phones (such as iPhone and Android phones).



```javascript
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}
```

```javascript
@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
```
# BootStrap

* Bootstrap is a free front-end framework for faster and easier web development
* Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins
* Bootstrap also gives you the ability to easily create responsive designs.

## BootStrap Grid 

Three Equal Rows :

```javascript
<div class="row">
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-4">.col-sm-4</div>
</div>
```

Two Unequal columns :

```javascript
<div class="row">
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-8">.col-sm-8</div>
</div>
```
---
### BootStrap Images

* The .img-rounded class adds rounded corners to an image

* The .img-circle class shapes the image to a circle

* Create responsive images by adding an .img-responsive class to the `<img>` tag. The image will then scale nicely to the parent element.

* The .img-responsive class applies display: block; and max-width: 100%; and height: auto; to the image
---

### Bootstrap Wells

The .well class adds a rounded border around an element with a gray background color and some padding.

---

### Bootstrap Alerts

Alerts are created with the .alert class, followed by one of the four contextual classes .alert-success, .alert-info, .alert-warning or .alert-danger
```javascript
<div class="alert alert-success">
  <strong>Success!</strong> Indicates a successful or positive action.
</div>

<div class="alert alert-info">
  <strong>Info!</strong> Indicates a neutral informative change or action.
</div>

<div class="alert alert-warning">
  <strong>Warning!</strong> Indicates a warning that might need attention.
</div>

<div class="alert alert-danger">
  <strong>Danger!</strong> Indicates a dangerous or potentially negative action.
</div>
```
---
### Bootstrap buttons

Bootstrap provides different styles of buttons

* .btn
* .btn-default
* .btn-primary
* .btn-success
* .btn-info
* .btn-warning
* .btn-danger
* .btn-link
---

### Bootstrap Badges and Labels

Badges are numerical indicators of how many items are associated with a link

```javascript
<a href="#">News <span class="badge">5</span></a><br>
<a href="#">Comments <span class="badge">10</span></a><br>
<a href="#">Updates <span class="badge">2</span></a>
```

Labels are used to provide additional information about something.

```javascript
<h1>Example <span class="label label-default">New</span></h1>
<h2>Example <span class="label label-default">New</span></h2>
```
---
### Bootstrap Pagination

If you have a web site with lots of pages, you may wish to add some sort of pagination to each page, to specify which page number you are currrently on or the list of names or number of pages.

```javascript
<ul class="pagination">
  <li><a href="#">1</a></li>
  <li class="active"><a href="#">2</a></li>
  <li><a href="#">3</a></li>
  <li><a href="#">4</a></li>
  <li class="disabled"><a href="#">5</a></li>
</ul>

//This is another form of pagination
<ul class="breadcrumb">
  <li><a href="#">Home</a></li>
  <li><a href="#">Private</a></li>
  <li><a href="#">Pictures</a></li>
  <li class="active">Vacation</li>
</ul>
```
---
Bootstrap pager

Pager provides previous and next buttons

```javascript
<ul class="pager">
  <li class="previous"><a href="#">Previous</a></li>
  <li class="next"><a href="#">Next</a></li>
</ul>
```
Bootstrap Lists

```javascript
<div class="list-group">
  <a href="#" class="list-group-item active">First item</a>
  <a href="#" class="list-group-item">Second item</a>
  <a href="#" class="list-group-item disabled">Third item</a>
</div>
```
### Bootstrap NavBar

With Bootstrap, a navigation bar can extend or collapse, depending on the screen size.

A standard navigation bar is created with  ` <nav class="navbar navbar-default">`.

It offers a variety of Variations.
* We can place the content to the right or left
* We can place buttons in the bar
* We can even add a Form to the navbar
* We can do a collapsing navbar for smaller screens

## Bootstrap Forms and inputs

Wrap labels and form controls in `<div class="form-group">` (needed for optimum spacing)
Add class .form-control to all textual `<input>`, `<textarea>`, and `<select>` elements.

```javascript
<form action="/action_page.php">
  <div class="form-group">
    <label for="email">Email address:</label>
    <input type="email" class="form-control" id="email">
  </div>
  <div class="form-group">
    <label for="pwd">Password:</label>
    <input type="password" class="form-control" id="pwd">
  </div>
  <div class="checkbox">
    <label><input type="checkbox"> Remember me</label>
  </div>
  <button type="submit" class="btn btn-default">Submit</button>
</form>
```


### Bootstrap supports the following form controls:

* input
* textarea
* checkbox ( class="checkbox" )
* radio  ( class="radio" )
* select

These input types can initialised under the class form-group or input-group, `<div class="input-group">`
`<div class="form-group">` and writing form-control inside the input tag, (class="form-control" ).


### Bootstrap Media Objects

This is a  really helpful tool. Bootstrap provides an easy way to align media objects (like images or videos) to the left or to the right of some content. This can be used to display blog comments, tweets and so on.

```javascript

<div class="media">
  <div class="media-left media-top">
    <img src="img_avatar1.png" class="media-object" style="width:60px">
  </div>
  <div class="media-body">
    <h4 class="media-heading">Media Top</h4>
    <p>Lorem ipsum...</p>
  </div>
</div>

```


# SASS

* Sass is an extension to CSS

* Sass reduces repetition of CSS and therefore saves time.

With Sass, you can store information in variables, like:

* strings
* numbers
* colors
* booleans
* lists
* nulls

Sass uses the **$** symbol, followed by a name, to declare variables.

>$variablename: value;

```javascript
$myFont: Helvetica, sans-serif;
$myColor: red;
$myFontSize: 18px;
$myWidth: 680px;

body {
  font-family: $myFont;
  font-size: $myFontSize;
  color: $myColor;
}

#container {
  width: $myWidth;
}
```

Main Feautures of SASS

* It allows us to nest css commands. 
```javascript
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

* It has the @import option, to import variable from other files.

```javascript
@import "variables";
@import "colors";
@import "reset";
```

* It has a feauture called @mixin. which allows certain style properties to be used through put the website. it is called by @include. 
```javascript
@mixin important-text {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
}


.danger {
  @include important-text;
  background-color: green;
}

```

* @Extend property, allows us to share a set of CSS properties from one selector to another.

```javascript
.button-basic  {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}

.button-report  {
  @extend .button-basic;
  background-color: red;
}
```





