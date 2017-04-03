# Part 2: SASS Partial Files, Import, Extend/Inheritance

## What is a Partial File?
A Partial Sass file is a file that has small pieces of SCSS. In order to create 
a partial sass file, you put an underscore before you name your file. For 
example: `_partial.scss`

## Importing

You can make a SCSS file from partial SCSS files. To use a partial SCSS file in
another SCSS file, you use `@import` and next to it write the name of the partial
file in single quotes. When a SCSS file that contains `@import` gets turn into a 
CSS file, the CSS file will have the properties of the partial file.

#### Example

##### SCSS
```
@import 'small';

.message {
  border: 4px solid #ccc;
  padding: 10px;
  color: #333;
}
```
##### CSS
```
h3 {
  font-family: "Source Sans Pro", sans-serif;
  color: #34495e; }
  
.message {
  border: 4px solid #ccc;
  padding: 10px;
  color: #333;
}
```
### Why You Should Import In SASS

Importing is beneficial in some situations since you may want a specific scss file to
have attributes of some partial sass files. For instance, say you want two familiar looking
CSS sheets but you want one to have a different looking font for the body, that is when importing
is your best friend. You can import a partial file to one CSS and not the other if you want.

## Extend/Inheritance

In SASS, SCSS selectors can inherit other selector's attributes by using `@extend`. `@extend` allows
you to share properties from one selector to another. When a SCSS turns to a CSS file, the selector
that inherits the properties will be shared with other selectors that have similar properties.

#### Example

##### SCSS
```
.message {
  border: 4px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  @extend .message;
  border-color: green;
}
```
##### CSSS
```
.message, .success {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333; }

.success {
  border-color: green; }
```