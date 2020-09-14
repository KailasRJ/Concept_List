# NEOITO TRAINING

# React Concept List

React creates a VIRTUAL DOM in memory.

Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, where it does all the necessary manipulating, before making the changes in the browser DOM.

## Setting up a React Environment

* If you have NPM and Node.js installed, you can create a React application by first installing the create-react-app.

* Install create-react-app by running this command in your terminal:

>C:\Users\Your Name>npm install -g create-react-app

* Then you are able to create a React application, let's create one called myfirstreact.

>C:\Users\Your Name>npx create-react-app myfirstreact

* Run this command to move to the myfirstreact directory:

>C:\Users\Your Name>cd myfirstreact

* Run this command to run the React application myfirstreact:

>C:\Users\Your Name\myfirstreact>npm start

# Modify the React Application
Look in the myfirstreact directory, and you will find a src folder. Inside the src folder there is a file called App.js, open it and modify the html inside App.js

```javascript
import React, { Component } from 'react';

class App extends Component {
  render() {
    return (
      <div className="App">
        <h1>Hello World!</h1>
      </div>
    );
  }
}

export default App;
```

# Elements of react

There are some main concepts that combine to form the react that it it truly is, let's check them out.

* The Render Function

display the specified HTML code inside the specified HTML element.

```javascript
ReactDOM.render(<p>Hello</p>, document.getElementById('root'));
```

The result will be displayed inside

```javascript
<body>

  <div id="root"></div>

</body>
```

* React JSX

JSX allows us to write HTML elements in JavaScript and place them in the DOM

```javascript
const myelement = <h1>I Love JSX!</h1>;

ReactDOM.render(myelement, document.getElementById('root'));
```

* React Components

Components are like functions that return HTML elements.

``` javascript
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```
Here, we created a component called Car.

And this is how you display it in the root id.

```javascript
ReactDOM.render(<Car />, document.getElementById('root'));
```

* Component Constructor

If there is a constructor() function in your component, this function will be called when the component gets initiated.

The constructor function is where you initiate the component's properties.

```javascript
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a {this.state.color} Car!</h2>;
  }
}
```

* props

Another way of handling component properties is by using props.

```javascript
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.color} Car!</h2>;
  }
}

ReactDOM.render(<Car color="red"/>, document.getElementById('root'));
```

* State

React components has a built-in state object.

The state object is where you store property values that belongs to the component.

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
      </div>
    );
  }
}
```

Always use the setState() method to change the state object.

# React Lifecycle

![lifecycle](https://i2.wp.com/programmingwithmosh.com/wp-content/uploads/2018/10/Screen-Shot-2018-10-31-at-1.44.28-PM.png?ssl=1)

>You can think of React lifecycle methods as the series of events that happen from the birth of a React component to its death.

* Mounting – Birth of your component
* Update – Growth of your component
* Unmount – Death of your component

* constructor

The constructor() method is called before anything else, when the component is initiated, and it is the natural place to set up the initial state and other initial values.
```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```


* render()

This is because render() is the only required method within a class component in React.

As the name suggests it handles the rendering of your component to the UI. It happens during the mounting and updating of your component.

```javascript
class Hello extends Component{
   render(){
      return <div>Hello {this.props.name}</div>
   }
}
```
>You cannot modify the component state within the render().

* componentDidMount()

componentDidMount() is called as soon as the component is mounted and ready. This is a good place to initiate API calls, if you need to load data from a remote endpoint.
>You can modify the component state within the componentDidMount(), but use it with caution.

* componentDidUpdate()
This lifecycle method is invoked as soon as the updating happens. The most common use case for the componentDidUpdate() method is updating the DOM in response to prop or state changes.

> You can modify the component state within the componentDidUpdate(), but use it with caution.

```javascript
componentDidUpdate(prevProps) {
 //Typical usage, don't forget to compare the props
 if (this.props.userName !== prevProps.userName) {
   this.fetchData(this.props.userName);
 }
}
```

* componentWillUnmount()

As the name suggests this lifecycle method is called just before the component is unmounted and destroyed. If there are any cleanup actions that you would need to do, this would be the right spot.

```javascript
componentWillUnmount() {
 window.removeEventListener('resize', this.resizeListener)
}
```
>Common cleanup activities performed in this method include, clearing timers, cancelling api calls, or clearing any caches in storage.

## Events

Just like HTML, React can perform actions based on user events.
React has the same events as HTML: click, change, mouseover etc.

>For methods in React, the this keyword should represent the component that owns the method.

You should bind the function into the constructor for it to be available in the shoot function 


```javascript
lass Football extends React.Component {
  constructor(props) {
    super(props)
    this.shoot = this.shoot.bind(this)
  }
  shoot() {
    alert(this);
    /*
    Thanks to the binding in the constructor function,
    the 'this' keyword now refers to the component object
    */
  }
  render() {
    return (
      <button onClick={this.shoot}>Take the shot!</button>
    );
  }
}

ReactDOM.render(<Football />, document.getElementById('root'));
```
## React Forms

In React, form data is usually handled by the components.

When the data is handled by the components, all the data is stored in the component state.

You can control changes by adding event handlers in the onChange attribute:

```javascript
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { username: '' };
  }
  myChangeHandler = (event) => {
    this.setState({username: event.target.value});
  }
  render() {
    return (
      <form>
      <h1>Hello {this.state.username}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        onChange={this.myChangeHandler}
      />
      </form>
    );
  }
}

ReactDOM.render(<MyForm />, document.getElementById('root'));
```

## React CSS

You can create an object containing different styles and then just call when needed inside the return.

```javascript
class MyHeader extends React.Component {
  render() {
    const mystyle = {
      color: "white",
      backgroundColor: "DodgerBlue",
      padding: "10px",
      fontFamily: "Arial"
    };
    return (
      <div>
      <h1 style={mystyle}>Hello Style!</h1>
      <p>Add a little style!</p>
      </div>
    );
  }
}
```

You can also create these styles in the usual way. By creating a style css file and styling a class which is called in the html section.


Creating a style file :


```javascript
.bigblue {
  color: DodgerBlue;
  padding: 40px;
  font-family: Arial;
  text-align: center;
}
```

Calling that style file into a component and exporting that component :

```javascript

import React from 'react';
import ReactDOM from 'react-dom';
import styles from './mystyle.module.css'; 

class Car extends React.Component {
  render() {
    return <h1 className={styles.bigblue}>Hello Car!</h1>;
  }
}

export default Car;
```

Calling that component and rendering it out.:

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import Car from './App.js';

ReactDOM.render(<Car />, document.getElementById('root'));

