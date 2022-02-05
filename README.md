# CSSCheatsheet

Useful: https://developer.mozilla.org/en-US/docs/Web/CSS

- [Selectors](#selectors)
    + [Class](#class)
    + [Element](#element)
    + [ID](#id)
    + [Pseudo-class](#pseudo-class)
- [Precedence Rule](#precedence-rule)
- [Typographic HTML/CSS](#typographic-HTML--CSS)
- [Colors](#colors)
    + [Font color](#font-color)
    + [Background color](#background-color)
    + [Gradient](#gradient)
- [Text Styles](#text-styles)
- [Box](#box)
- [List](#list)
- [Cursor](#cursor)
- [Layout](#layout)
- [Variables](#variables)
- [Media Queries](#media-queries)


--------------------------------


# Selectors

### Class
```css
/* All elements with class="headers" */
.headers {
  margin: 10px;
}

/* All <form> elements with class="text1" */
form.text1 {
  margin: 5px;
}

/* <input> elements with type="text" or "email" */
input[type="text"],
input[type="email"] {
  border: 2px solid #000;
  margin: 0 0 1em 0;
  padding: 10px;
  width: 100%;
}

/* All <li> elements with a class list that includes both "text1" and "size1" */
/* For example, class="text1 size1 color1" */
form.text1.size1 {
  font-size: 14px;
}

```

### Element
```css
a {
  color: red;
}

h2 {
  text-align: center;
  font-size: 16px;
  color: blue;
}

```

### ID
```css
#subscribe-button {
  color: blue;
  border: white 1px solid;
}
```

### Pseudo-class
/* All buttons on hovering */
```css
button:hover {
  color: grey;
}
```

# Precedence Rule
```css
The Cascade: 
#id				beats 
.className		beats 
element (e.g. DIV).
```

# Typographic HTML/CSS
DIVs are like paragraphs (take whole width available to them). This is driven by the style property display, value block default for DIVs  and P, H1, etc
```css 
display:block  is default style for DIV 
```
SPANs are like words (take only width necessary, and flow to the next line if there’s no space). 
```css 
display:inline ``` is default style for SPANs 

```css 
display:inline-block ``` is like inline but allows setting of height and width (unlike display:inline). So we can get “taller words” in the “text line”. 
Example: 
```css display:inline-block; height:100px; ```
```css display:none  ``` hides the element, with all its children
```css float:left    float:right```  styles are used especially with images to allow them to float at the side while the text flows around them, like in a newspaper (typographic).
```


# Colors

### Font color
```css
h1 {
  color: #ffffff;
}

h2 {
  color: #f0abcb;
}

h3 {
  color: rgba(100, 200, 100, 0.5);
}

h4 {
  color: violet;
}
```

### Background color
```css
.header {
  background: grey;
}
```

### Gradient
```css
.header {
  background: linear-gradient(#ffffff, #f0abcb);
}
```

# Text Styles

```css
h1 {
	text-align: center; /* left / right / center / justify / initial / inherit */
	text-transform: uppercase; /* none / capitalize / uppercase/ lowercase / initial / inherit */
	text-decoration: overline; /* none / underline / line-through / overline / inherit */
	font-style: oblique 40deg; /* normal / italic / oblique / initial / inherit */
	font-weight: 700; /* normal / bold / bolder / lighter / initial / inherit / 100 / 200 / 300 / 400 / 500 / 600 / 700 / 800 / 900 */
}

body {
	font-size: 12px;
	font-family: serif;
	line-height: 32px; /* normal / 1.5 multiplied / 3em / 32% / inherit / initial / revert / unset */
}
```

# Box
```css
.header {
	border: thick double #32a1ce; /* First value is the thickness, second - style (none / hidden / dotted / dashed / solid / double / groove / ridge / inset / outset), and third - color */
}

.box {
	margin: 10px 50px 20px 0; /* top right bottom left */ /* creates extra space around an element */
	max-height: 100px; /* height / min-height*/
}

.box2 {
	padding: 1em; /* creates extra space within an element */
	width: 75%; /* auto / % / length (px/em) / max-content / min-content / fit-content / inherit / initial / revert / unset */
}

```

# List
```css
ul {
	list-style: georgian inside url('/media/examples/rocket.svg');
	padding: 0;
	margin: 0;
}
```

# Cursor
```css
button:hover {
	cursor: pointer; /* auto / default / none / context-menu / help / pointer / progress / wait / cell / crosshair / text / vertical-text / alias / copy / move / no-drop / not-allowed / e-resize / n-resize / ne-resize / nw-resize / s-resize / se-resize / sw-resize / w-resize / ew-resize / ns-resize / nesw-resize / nwse-resize / col-resize / row-resize / all-scroll / zoom-in / zoom-out / grab / grabbing */
}
```

# Layout
```css
img {
  display: block; /* block - invisible line before and after */
  position: relative; /* static / relative / fixed / absolute / sticky */
  top: 40px; left: 40px;
}
```

# Variables
```css
:root {
  --main-bg-color: pink;
}

element {
  background-color: var(--main-bg-color);
}
```

# Media Queries
/* used to conditionally apply styles depending on device */
```css
@media (hover: hover) { ... } /* when the primary input can hover */
@media (max-width: 12450px) { ... } /*  if the browser's viewport width is equal to or narrower than 12450px */
@media (color) { ... } /* apply to any device with a color screen */
@media speech and (aspect-ratio: 11/5) { ... } 
@media (min-width: 30em) and (orientation: landscape) { ... } /* (AND) landscape-oriented devices with a width of at least 30 ems */
@media (min-height: 680px), screen and (orientation: portrait) { ... } /* (OR)  device has a minimum height of 680px or is a screen device in portrait mode */
@media not (all and (monochrome)) { ... }
@media only screen and (color) { ... } /* prevents older browsers that do not support media queries with media features from applying the given styles */
``` 