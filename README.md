# CSSCheatsheet



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