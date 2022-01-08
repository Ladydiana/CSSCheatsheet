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
	border: thick double #32a1ce; /* First value is the thickness, second - style (none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset), and third - color */
}

.box {
	margin: 10px 50px 20px 0; /* top right bottom left */ /* creates extra space around an element */
	max-height: 100px; /* height | min-height*/
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