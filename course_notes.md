# HTML, CSS and Javascript for Web Developers

# COURSE NOTES

## References

Start `browser-sync`: `browser-sync start --server --directory --files "**/*"`
(Updates all file changes directly to the browser page)

Use to ask questions and for reference:

- Share HTML, CSS and HTML code with: www.jsfiddle.net
- Good info on CSS and HTML: www.css-tricks.com
- Good ideas on CSS, HTML and Javascript: www.codepen.io

HTML standard: www.w3c.org

Keeps track of HTML, CSS and Javascript evolution, which browser supports which features: www.caniuse.com

Validate HTML: validator.w3.org

Browsers usage statistics: www.w3schools.com/browsers/browsers_stats.asp

Types of HTML content: https://html.spec.whatwg.org/multipage/dom.html#kinds-of-content

Bootstrap: www.getbootstrap.com/getting-started

jQuery: www.jquery.com

Do site Mock-Ups: www.balsamiq.com

Import fonts: www.google.com/fonts

Get temporary image placeholders: www.placehold.it

Ajax Loaders animations (GIFs): www.ajaxloadingimages.net

## CONNECT WITH THE COURSE INSTRUCTOR

Yaakov Chaikin from Johns Hopkins University

[On Facebook](https://www.facebook.com/CourseraWebDev/)

[On Twitter](https://twitter.com/YaakovChaikin)

[On LinkedIn](https://www.linkedin.com/in/yaakovchaikin) (make sure to mention that you are in his Coursera class in the
invitation to connect!)

CHECK OUT HIS SITE: https://ClearlyDecoded.com - You'll find web dev tutorials and other relevant content there.

## Notes

HTML - Hypertext Markup Language

CSS - Cascading Style Sheets

HTML - Strucuture

CSS - Style

Javascript - Behavior

Comment on HTML: `<!-- -->`

We can go to the Network section in the browser Web Developer Tools to set the internet speed
(to simulate different types) of connections.

### HTML Character Entity References (Lecture 8)

Instead of:

- `<` use `&lt;`
- `>` use `&gt;`
- `&` use `&amp;`
- `©` use `&copy;` (copyright symbol)
- ` ` use `&nbsp;` (not breaking space)
- `"` use `&quot;`

### Creating Links (Lecture 9)

Using the `target="_blank"` attribute in the `<a>` tag tells the browser to open the link in a new tab.

Use `href` with the `#` to point to `fragment identifiers` (identified by one `id` attribute) in the same page.

`<a>` are both inline and block elements.

### Displaying Images (Lecture 10)

`<img src="url to the image location (same as href)" width="" height="" alt="alternative text">`

`<img>` are inline elements.

*Always specify the width and height of an image to ensure the visual integrity (layout of the elements)
even if the image has not loaded yet!*

### Combining CSS Selectors (Lecture 14)

- Element with `class` selector (`selector.class`)
- Child (direct) selector (`selector > selector`)
- Descendent selector (`selector selector`)
- Adjacent selector (`selector + selector`)
- General sibling selector (`selector ~ selector`)

### Pseudo-Class Selectors (Lecture 15)

```
selector:pseudo-class {
    ...
}
```

- `:link`
- `:visited`
- `:hover`
- `:active`
- `:nth-child(...)` (we can use `even` and `odd` as values)

### Conflict Resolution (Lectures 16 and 17)

- Origin
- Merge
- Inheritance
- Specificity
    - `style="..."`
    - ID
    - Class, pseudo-class, attribute
    - Number of elements

*Do not use the `!important` attribute as it gives absolute precedence but can cause a mess in the understanding of the
CSS precedence in your code!*

```
p {
    color: green !important;
}
```

### The Box Model (Lecture 19)

Use `box-sizing: border-box` instead of `box-sizing: content-box` to limit the external size of the elements. Use it in
the `*` (universal selector that selects all elements) selector:

```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

Horizontal margins are cumulative (40px and 50px --> 90px) and vertical margins collapse (20px and 30px --> 30px).

The property `overflow` is used to control the behavior of the content that spills over its determined space
(with width and height).

### The background Property (Lecture 20)

```
#bg {
  background: url("yaakov.png") no-repeat right center;
}
```

The url has to be relative to the CSS file.

### Positioning Elements by Floating (Lecture 21)

- Floating elements can produce very flexible layouts
- Floats are taken out of the normal document flow
- Floats don't have vertical margin collapse
- To resume normal document flow, use the `clear` property

### Media Queries (Lecture 23)

Basic syntax of a media query:

- @media (media feature)
- @media (media feature) logical operator (media feature)

*Be careful not to overlap range boundaries!*

Usually, you provide base styling then change and/or add to them in each media query.

```
@media (max-width: 800px) {...}
@media (min-width: 800px) {...}
@media (orientation: portrait) {...}
@media screen {...}
@media print {...}
@media (min-width: 768px) and (max-width: 991px) {...}
```

### Responsive Design (Lecture 24)

12-Column Grid Responsive Layout

Use % to achieve fluid width.

Add the meta tag `viewport` to the HTML to inform the design is responsive and that the mobile devices shouldn't try to
adjust it (zoom).

`<meta name="viewport" content="width=device-width, initial-scale=1">`

### Introduction to Twitter Bootstrap (Lecture 25)

Bootstrap is the most popular HTML, CSS and JS framework for developing responsive mobile first projects on the web.

Mobile First == **plan** mobile from the start

CSS Framework is mobile ready

Setting up Bootstrap:

- Download the compiled Bootstrap version
- Download jQuery and put inside the Bootstrap JS folder

Add `<meta http-equiv="X-UA-Compatible" content="IE=edge">`
to inform the IE browsers to use their latest version of their rendering engine.

Add:

```
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <!-- Our CSS style -->
    <link rel="stylesheet" href="css/styls.css">
  </head>
<body>

  ...

  <!-- jQuery (Bootstrap JS plugins depend on it) -->
  <script src="js/jquery-1.11.3.min.js"></script>
  <script src="js/bootstrap.min.js"></script>
  <!-- Our JS -->
  <script src="js/script.js"></script>
</body>  
```

### The Boostrap Grid System

```
<div class="container">
  <div class="row">
    <div class="col-md-4">Col 1</div>
    ...
  </div>
</div>
```

There is also the class `container-fluid`.

Column classes elements (`col-SIZE-SPAN):

- SIZE: Screen width range identifier (columns will collapse (i.e., stack) below that width, unless another rule
  applies)
- SPAN: How many columns an element should span (values 1 through 12)

### Visit with the Client (Lecture 27)

*Google for "web development client questionnaire"!*

- Bring examples of other sites to help client figure out what they want
- Encourage client to use less information
- Client should invest in the project
- Client should have one person as the decider
- Limit the number of revisions
- Involve others to help you produce a great product

### Design Overview (Lecture 28)

Site to do Mock-Ups of the site to be built: www.balsamiq.com

Import fonts: www.google.com/fonts

### Coding Basics of Navbar Header (Lecture 30)

Consult the documentation of Bootstrap to know with classes and containers to use.

*We can add images via CSS with the `background-img` property.*

### Coding Nav Menu Buttons (Lecture 31)

Bootstrap comes with a selection of predefined Glyphicons.

We can set a `<a href="tel:410-602-5008>410-602-5008</a>` so it activates the phone when the user is visiting the page
on a cell phone and clicks on the `a` tag phone number.

### Fixing Navbar Layout, Text, and Dropdown Menus (Lecture 33)

Adjustable font-size:

```
  font-size: 5vw; /* 1vw = 1% of viewport width */
```

### Coding the Jumbotron (Lecture 34)

Jumbotron is the Bootstrap term for the big image in the center of the page.

### Coding Navigation Tiles (Lecture 35)

To get the map with the address of the location, go to Google Maps and go to "Share or embed map". Copy the link and
the `iframe` (Embed map option). Adjust height and width of the `iframe`.

### Where to Place Javascript Code (Lecture 40)

- At the `<head>` or the `<body>`, inside an `<script>` tag
- Inside an external file: `<script src="js/script.js"></script>`

### Defining Variables, Function and Scope (Lecture 41)

**Javascript is always executed sequentially!**

`var a = 1;`

No types are declared:

- JS is dynamically typed language
- Same variable can hold different types during the life of the execution

`function a () {...}`

`var a = function () {...}`

`a();`

All legal:

```
function compare (x, y) {
  return x > y;
};
var a = compare(4, 5);
compare(4, "a");
compare();
```

In the last call of `compare()`, the syntax is legal because the arguments of a function are optional in JS.

In JS there are two Scopes: Global and Function (aka lexical).

- Global: Variable and functions defined here are available everywhere
- Function: Variables and functions defined here are available only within this function

Scope chain:

- Everything is executed in an *Execution Context*
- Function invocation creates a new *Execution Context*
- Each *Execution Context* has:
    - Its own *Variable Environment*
    - Special `this` object
    - Reference to its *Outer Environment*
- Global scope does not have an *Outer Environment* as it's the most outer environment there is

Referenced (not defined) variable will be searched for in its current scope first. If not found, the Outer Reference
will be searched. If not found, the Outer Reference's Outer Reference will be searched, etc. This will keep going until
the Global scope. If not found in Global scope, variable is undefined.

### Javascript Types (Lecture 42)

Javascript defines 7 built-in types: Object and 6 Primitives

Object is a collection of name/value pairs. Person Object:

```
firstName: "Yaakov",
lastName: "Chaikin",
social: {
          linkedin: "yaakovchaikin",
          twitter: "yaakovchaikin",
          facebook: "CourseraWebDev"
        }
```

Primitive type represents a *single*, *immutable* value

- Single value, i.e., <ins>*not*</ins> an object
- Immutable means once it's set, it can't be changed
    - Value becomes read-only
    - You can create another value based on an existing one

Primitive Type: Boolean (2 values: `true` or `false`)

Primitive Type: Undefined. Undefined signifies that no value has ever been set (1 value: `undefined`). You *can* set a
variable to `undefined` but you *should NEVER do it*

Primitive Type: Null. Signifies lack of value (1 value: `null`)

Primitive Type: Number. Number is the only numeric type in Javascript. Always represented under the hood as
double-precision 64-bit floating point. JS does *not* have an integer type. Integers are a subset of double instead of a
separate data type

Primitive Type: String. String is sequence of characters used to represent text

Primitive Type: Symbol. Symbol is new to ES6. Not covered in this class. ES6 was released in 2015

### Common Language Constructs (Lecture 43)

String concatenation:

```
var string = "Hello";
string += " World!";
```

Regular math operators: `+`, `-`, `*`, `/`

```
(5 + 4) / 3;
undefined / 5; // NaN
```

Equality:

```
var x = 4, y = 4, z = "4";
x == y; // true
x == z; // true (because of type coercion)
```

Strict Equality:

```
var x = 4, y = 4, z = "4";
x == y; // true
x == z; // false (use strict equality to avoid type coercion)
```

Boolean `false` equivalents: `null`, `undefined`, `""`, `0`, `NaN`

Boolean `true` equivalents: `"hello"`, `1`, `-1`, `"false"`

### Handling Default Values (Lecture 44)

Two ways of handling it:

- With `if`:

```
function orderChickenWith(sideDish) {
  if (sideDish === undefined) {
    sideDish = "whatever!";
  }
  console.log("Chicken wiht " + sideDish);
}
```

- With shortcut (returns the first element that was coerced to `true`):

```
function orderChickenWith(sideDish) {
  sideDish = sideDish || "whatever!";
  console.log("Chicken wiht " + sideDish);
}
```

### Creating Objects Using 'new Object()' Syntax (Lecture 45 part 1)

```
var company = new Object();
company.name = "Facebook";
console.log(company.name); // Facebook
console.log(company["name"]); // Facebook
var stockPropName = "stock of company";
company[stockPropName] = 110;
console.log(company[stockPropName]); // 110
```

### Creating Objects Using Object Literal Syntax (Lecture 45 part 2)

Better way to create an object:

```
var facebook = {
  name: "Facebook";
  ceo: {
    firstName: "Mark",
    favColor: "blue"
  }
  "stock of company": 110
};
```

### Functions Explained (Lecture 46)

Function are First-Class Data Types. Functions ARE objects

```
function multiply(x, y) {
  return x * y;
}
multiply.version = "v.1.0.0";

// Function factory
function makeMultiplier(multiplier) {
  var myFunc = function (x) {
    return multiplier * x;
  };
  
  return myFunc;
}

var multiplyBy3 = makeMultiplier(3);
console.log(multiplyBy3(10)); // 30
var doubleAll = makeMultiplier(2);
console.log(doubleAll(100)); // 200

// Passing functions as arguments
function doOperationOn(x, operation) {
  return operation(x);
}

var result = doOperationOn(5, multiplyBy3);
console.log(result); // 15
```

### Passing Variables by Value vs by Reference (Lecture 47)

In Javascript, primitives are passed/copied by value, objects are passed/copied by reference

### Function Constructors, Prototype, and the `this` Keyword (Lecture 48)

Functions constructors (class) have capital names by convention. We HAVE to use the `new` keyword to call the
constructors otherwise they are simple functions

```
// Function constructors
function Circle (radius) {
  this.radius = radius;
}
// This is the way to create "static" constructor (class) methods. Create it outside the constructor
Circle.prototype.getArea = function () {
  return Math.PI * Math.pow(this.radius, 2);
};

var myCircle = new Circle(10); // new Object();
console.log(myCircle); // Circle {radius: 10}
console.log(myCircle.getArea()); // 314.159...
```

### Object Literals and the `this` Keyword (Lecture 49)

```
// Object literals and `this`
var literalCircle = { // new Object();
  radius: 10,
  
  getArea: function () {
    return Math.PI * Math.pow(this.radius, 2);
  };
}

console.log(literalCircle.getArea()); // 314.159...

// JS bug where the `this` inside a function inside and object function refers to the
// Global context and not the object context.
// To fix it we replace `this` by `self` in the inner functions
var literalCircle = { // new Object();
  radius: 10,
  
  getArea: function () {
    var self = this;
    console.log(this); // Object {radius: 10}
    
    var increaseRadius = function () {
      self.radius = 20;
    };
    increaseRadius();
    console.log(this.radius) // 20
    
    return Math.PI * Math.pow(this.radius, 2);
  }
}

console.log(literalCircle.getArea()); // 1256.637...
```

### Arrays (Lecture 50)

```
// Arrays
var array = new Array();
array[0] = "Yaakov";
array[1] = 2;
array[2] = function (name) {
  console.log("Hello " + name);
}
array[3] = {course: "HTML, CSS & JS"};

// Short hand array creation
var names = [
  {name: "Yaakov"},
  "John",
  2
];
```

### Closures (Lecture 51)

```
// Closures
function makeMultiplier (multiplier) {
  return (
    funtion (x) {
      return multiplier * x;
    }
  );
}
```

### Fake Namespaces (Lecture 52 part 1)

When importing from multiple scripts (JS files), create objects related to each namespace with its own names to be
called in the global scope to avoid variable overriding.

### Immediately Invoked Function Expressions (IIFEs) (Lecture 52 part 2)

Question 1

Immediately Invoked Function Expressions are usually used to place code into its own execution context not to conflict
with the global scope.

```
// Immediately Invoked Function Expressions IIFE
(function () {
  console.log("Hello Coursera!");
})();
```

### DOM Manipulation (Lecture 53)

```
console.log(document.getElementById("title"));
console.log(document instanceof HTMLDocument);
document.getElementById("content").textContent = "Content";
document.getElementById("content").innerHTML = "<h2>Content</h2>";
document.querySelector("#title");
document.querySelector("h1");
```

### Handling Events (Lecture 54)

```
// Unobstrusive event binding
document.querySelector("button").addEventListener("click", sayHello) // `sayHello` is a function;
document.querySelector("button").onclick = sayHello;
```

### The `event` Argument (Lecture 55)

Is passed to the function with every event listener. Has many properties that can be exploited.

### HTTP Basics (lecture 56)

HyperText Transfer Protocol

URN: Uniform Resource Name. Example: "HTML/CSS/Javascript/Web Developers/Yaakov/Chaikin"
URI: Uniform Resource Identifier. Example: "/official_web_site/index.html"
URL: Uniform Resource Locator. Example: "http:://www.mysite.com/official_web_site/index.html"

#### HTTP Request Structure (GET)

GET /index.html?firstName=Yaakov HTTP/1.1

Method: GET
URI String: /index.html
Query String: ?firstName=Yaakov
HTTP Version: HTTP/1.1

#### HTTP Request Structure (POST)

POST /index.html HTTP/1.1
HOST: coursera.org
Accept-Charset: utf-8
firstName=Yaakov...
...
...

Request Headers:
HOST: coursera.org
Accept-Charset: utf-8

Message Body:
firstName=Yaakov...
...
...

#### HTTP Response Structure

HTTP/1.1 200 OK

HTTP Version: HTTP/1.1
Response Status Code: 200
English phrase describing status code: OK

HTTP/1.1 200 OK
Date: Tue, 11 Aug 2004 19:00:01 GMT
Content-Type: text/html
<html>
<body>
<h1>Secret to gaining weight REVEALED!</h1>
<p>Develop Coursera courses after work at night while eating sweets to keep yourself awake!</p>
</body>
</html>

Some Response Status Code

- 200 OK
- 404 Not Fount
- 403 Forbidden
- 500 Internal Server Error

### Ajax Basics

Asynchronous Javascript And XML

### Processing JSON

JavaScript Object Notation

Convert from json string to object:
`var obj = JSON.parse(jsonString);`

Convert from object to json string:
`var str = JSON.stringify(obj);`

### Dynamically Loading Home View (Lecture 60)

On the Chrome Developer Tools, at the Network tab, we can select XHR to see just the AJAX requests.

### Dynamically Loading Menu Categories View (Lecture 61)

CORS: Cross-origin Resource Sharing
