# CSS Notes

**IMPORTANT `CSS` USES `snake-case`**

For the `margin`, `padding`, and `rem` explanation [click here](##Remove-all-the-default-margin-and-padding:).
## Usage
`style.css` class example:
```css
.blue-text {
    color: blue;
}

#red-text {
    color: red;
}
```
**IMPORTANT DONT FORGET TO ADD "`;`" AFTER EACH PROPERTY**

`index.html` class example:
```html
<div id="red-text" class="blue-text">???</div>
```
Importance: `!important` > inline >`id` > `class` > order

### Attribute Selector
```css
[type='radio'] {
  margin: 20px 0px 20px 0px;
}
```

## Color
**Text Color** is `color`

**Background Color** is `background-color`
```css
.color-class {
    color: green;
    background-color: green;
}
```
Valid color definition :
```css
.color-class {
    color: red; 
    color: #F00;
    color: #FF0000
    color: rgb(255, 0, 0);
    color: hsl(0, 100%, 50%);
    color: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
}
```

## Font Family
for `font-family`, left one has higher priority than the right one. When most left is available, use it.
```css
font-family: Helvetica, sans-serif;
```

## Border
CSS borders have 3 main properties `border-style`, `border-width`, and `border-color`
```css
.thin-red-border {
    border-color: red;
    border-width: 10px;
    border-style: solid;

    /* Additional Border Properties */
    border-radius: 10px;
}
```

Also can be used like this:
```css
.thin-red-border {
    border: 10px solid red;
}
```

Use `border-radius` of `50%` for circular image

```css
.thin-red-border {
    border-radius: 50%;
}
```

## Padding and Margin
Adding minus `margin` will **expand** instead of **shrinking** the element
```css
.red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: -15px;
}
```
Specifying individual properties for both margin and padding:
```css
.red-box {
    /* Other Code */
    padding-top: 40px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 40px;
}
```
### Clockwise Notation
`padding: top right bottom left;`
```css
.red-box {
    /* Other Code */
    padding: 20px 40px 20px 40px;
  }
```
### Remove all the default margin and padding:
```css
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}
```

## Absolute vs Relative Units

default value of browser is `16px`, by setting the default value of the **root** `font-size` will make the use of `rem` responsive
- `px` is absolute
- `em` is based on **current** element `font-size`
- `rem` is based on **root** element `font-size`


By explicitly defining the root `font-size` we can manipulate tht `rem`

`1rem = 10px, 10px/16px = 62.5%`

### Set the default of `1rem` to `10px`
```css
html {
  font-size: 62.5%;
}
```

## Variables
Variables is defined using `--<variable-name> : property`
```css
.penguin {
    --penguin-beak: yellow;
}
```
Variable is called using `var(--<variable-name>, <default>)`
```css
.beak-bottom {
    background: var(--penguin-beak, orange);
}
```
Variable must be placed higher or equal level than the caller
```css
<div class="penguin">
    <div class="beak-bottom"></div>
</div>
```
It is best practice to always include fallback because of compability issues:

```css
.red-box {
    background: red; /*this is the fallback*/
    background: var(--red-color);
}
```

### Root
If you dont want to put `div` on higher level, as mentioned before, use the `:root` psuedo-class
```css
:root {
    --penguin-belly: pink;
}
```