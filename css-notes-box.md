# CSS Notes

**IMPORTANT `CSS` USES `snake-case`**

## Default Value
```css
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
}

body {
    background-color: black;
    color: white;
    font-family: monospace;
}
```
- the `*` selector is used to remove all the `margin` and `padding`
- the `html` selector is used to set the default `rem` value
- the `body` selector is used to set the default value of other properties

### Disclaimer
- `*` selector: do not modify any properties
- `html` selector: **only** modify the `font-size` here
- `body` selector: add any default value here instead. Such as `padding`, `margin`, etc.

## Position
### Relative
By using `position: relative;` we can use 4 extra properties:

- `top`
- `right`
- `bottom`
- `left`

Relative positioning **doesn't break** the normal flow of document
```css
.relative-position {
  position: relative;
  bottom: 10px;
}
```
By using `bottom: 10px;`, it is similar to `margin-bottom: 10px;`, but instead of appending the element, it moves the element instead.

### Absolute
When the element is setted as `position: absolute;`, we can use similar properties such as `position: relative;`:

- `top`
- `right`
- `bottom`
- `left`

Absolute positioning **break** the normal flow of document. Which will cause the other element to ignore this element.

```css
.absolute-parent {
  position: relative;
}

.absolute-position {
  position: absolute;
  bottom: 10px;
}
```
Absolute will always stays relatively to the parent

### Fixed
`position: fixed;` is **exactly the same** as `position: absolute;` but the only difference is a Fixed element **wont move** even when the **user scrolls**.

It also have 4 extra properties

- `top`
- `right`
- `bottom`
- `left`

Fixed usually used by `<nav></nav>`
```css
.fixed-position {
  position: fixed;
  left: 0px;
  top: 0px;
}
```

### Float
Floating elements are removed from the normal flow of a document and pushed to either the `left` or `right` of their containing parent element.

```css
.left-float {
  float: left;
  width: 50%;
}
.right-float {
  float: right;
  width: 40%;
}
```

### Center Element Horizontally
```css
.center-element {
  margin: 0 auto;
}
```

## Transform
You can use transform like this
```css
.transform-this {
  transform: scale(2) skewX(24deg);
}
```
You can also use it with `:hover` pseudo-class
```css
.transform-this:hover {
  transform: scale(3);
}

```

## Card
```css
.card {
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
  border: 1px solid #ccc;
  border-radius: 5px;
}
```

## Text modification
`text-transform`, to modify text into `uppercase`, `lowercase`, or `capitalize`
```css
.change-text {
  text-transform: capitalize;
}
```
## Pseudo-class
### Anchor tag
```css
a:hover {
  color: red;
}
```
