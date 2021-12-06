# HTML, CSS and Javascript for Web Developers

# COURSE NOTES

## References

Start `browser-sync`: `browser-sync start --server --directory --files "*"`
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

##CONNECT WITH THE COURSE INSTRUCTOR

Yaakov Chaikin from Johns Hopkins University

[On Facebook](https://www.facebook.com/CourseraWebDev/)

[On Twitter](https://twitter.com/YaakovChaikin)

[On LinkedIn](https://www.linkedin.com/in/yaakovchaikin) (make sure to mention that you are in his 
Coursera class in the invitation to connect!)

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

#### HTML Character Entity References (Lecture 8)

Instead of:
- `<` use `&lt;`
- `>` use `&gt;`
- `&` use `&amp;`
- `©` use `&copy;` (copyright symbol)
- ` ` use `&nbsp;` (not breaking space)
- `"` use `&quot;`

#### Creating Links (Lecture 9)

Using the `target="_blank"` attribute in the `<a>` tag tells the browser to open the link in a new tab.

Use `href` with the `#` to point to `fragment identifiers` (identified by one `id` attribute) in the same page.

`<a>` are both inline and block elements.

#### Displaying Images (Lecture 10)

`<img src="url to the image location (same as href)" width="" height="" alt="alternative text">`

`<img>` are inline elements.

*Always specify the width and height of an image to ensure the visual integrity (layout of the elements)
even if the image has not loaded yet!*

#### Combining CSS Selectors (Lecture 14)

- Element with `class` selector (`selector.class`)
- Child (direct) selector (`selector > selector`)
- Descendent selector (`selector selector`)
- Adjacent selector (`selector + selector`)
- General sibling selector (`selector ~ selector`)

#### Pseudo-Class Selectors (Lecture 15)

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

#### Conflict Resolution (Lectures 16 and 17)

- Origin
- Merge
- Inheritance
- Specificity
    - `style="..."`
    - ID
    - Class, pseudo-class, attribute
    - Number of elements

*Do not use the `!important` attribute as it gives absolute precedence but can cause a mess
in the understanding of the CSS precedence in your code!*

```
p {
    color: green !important;
}
```

#### The Box Model (Lecture 19)

Use `box-sizing: border-box` instead of `box-sizing: content-box` to limit the external size of the
elements. Use it in the `*` (universal selector that selects all elements) selector:

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

#### The background Property (Lecture 20)

```
#bg {
  background: url("yaakov.png") no-repeat right center;
}
```
The url has to be relative to the CSS file.

#### Positioning Elements by Floating (Lecture 21)

- Floating elements can produce very flexible layouts
- Floats are taken out of the normal document flow
- Floats don't have vertical margin collapse
- To resume normal document flow, use the `clear` property

#### Media Queries (Lecture 23)

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

#### Responsive Design (Lecture 24)

12-Column Grid Responsive Layout

Use % to achieve fluid width.

Add the meta tag `viewport` to the HTML to inform the design is responsive and that the mobile devices shouldn't try to
adjust it (zoom).

`<meta name="viewport" content="width=device-width, initial-scale=1">`

#### Introduction to Twitter Bootstrap (Lecture 25)

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

#### The Boostrap Grid System

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
- SIZE: Screen width range identifier (columns will collapse (i.e., stack) below that width,
unless another rule applies)
- SPAN: How many columns an element should span (values 1 through 12)