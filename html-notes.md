# HTML Notes

## Basic
`<img src="#" alt="#">` is a self-closing tag, alt must be filled unless it is a decorative image

` <a href >???</a>` The `???` inside the anchor tag can be text, image or anything

```html
<a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>
```
anchor can be used to navigate to element id by using `#any-id-here`

`target="_blank" ` this causes the linked document to open in a new window tab.

## Form
`<input type="text" placeholder="Input here!">` input element are self-closing

```html
<form action="/url-where-you-want-to-submit-form-data">???</form>
```
The `???` usually is the input of the form `<form><input></form>`
```html
<button type="submit">Button Name</button>
```
Use `<button>` on the last element of a form
```html
<input type="text" required>
```
Use the `required` attribute to make the text input as required.

## Common Input Types
**REMEMBER `<input>` IS SELF CLOSING TAG**
### Text
```html
<input type="text" placeholder="Your placeholder here!">
```
### Radio
```html
<label for="indoor-outdoor"> 
  <input type="radio" value="indoor" name="indoor-outdoor">Indoor 
</label>

<label for="indoor-outdoor"> 
  <input type="radio" value="outdoor" name="indoor-outdoor">Outdoor 
</label>
```
Same `name` attribute means one group

`for` attribute of `label` must be the same with the `name` attribute of radio input for best practices. 

### Checkbox
Forms use checkboxes on multiple answers.
#### Checkbox best practice : 
```html
<label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>
```
`for` attribute of `label` must be the same with the `id` attribute of `checkbox` input for best practices. 

### Checkbox and Radio Similarity
```html
<input type="radio" name="test-name" checked>
```
Use the `checked` attribute to set default value

## IMPORTANT
**When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type `radio` and `checkbox` report their values from the `value` attribute.**