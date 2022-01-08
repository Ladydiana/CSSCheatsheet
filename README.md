# CSSCheatsheet

Useful: https://developer.mozilla.org/en-US/docs/Web/CSS

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