# Part 3: SASS Operators and New Tricks

## Applying Changes Without `sass input.scss output.css`

You can add changes to your SCSS file and apply them to your css file without having to use 
`sass input.scss output.css` repeatedly. Using `sass --watch input.scss:output.css` allows your CSS
file to get the latest changes from your SCSS file automatically. However only one CSS file can get automatic changes
from a SCSS file. If you want a different CSS file to get new changes from another SCSS file, then you will have to stop 
`sass --watch input.scss:output.css` by using `control + C`

### Warning
When using `sass --watch input.scss:output.css`, make sure that the changes you made on your SCSS file are correct 
since your CSS file might encounter an error if there is a mistake on your scss file that the CSS file is getting the changes
from.

#### Example of Error

SCSS
```SCSS
@import 'small';

.message {
  border: (12px - 2px) solid #ccc;
  padding: 20px;
  color: #333;
}

.success {
  @extend .message;
  border-color:
}
```

CSS
```CSS
/*
Error: Invalid CSS after "  border-color:": expected expression (e.g. 1px, bold), was "}"
        on line 12 of style.scss

7: }
8: 
9: .success {
10:   @extend .message;
11:   border-color: 
12: }
13: 
14: $container-width: 100%;
15: 
16: .container {
17:   width: $container-width;

Backtrace:
style.scss:12
/usr/local/rvm/gems/ruby-2.3.0/gems/sass-3.4.23/lib/sass/scss/parser.rb:1207:in `expected'
```

Notice how the CSS file detects that the SCSS file did not determine what border-color to use. This causes the CSS file to 
encounter an error as the file does not know what border-color to use. Luckily the CSS file knows what line in the SCSS file is
the cause of the error.

## Operators

In SCSS files, you can use operators such as adding and multiplying in order to fix up properties that use px(pixels) or percentages. Operators are
useful as you can use them simultaneously with variables and thus not having to write the same number of pixels repetitively.
By the way, SASS is compatible with Bootstrap, allowing you to have multiple ways to format your webpage. 

### When To Use Operators
An example of when to use operators is, say
you want your border to have 20px but you also want your padding to have 5px and your font size to be 10px. Using operators and variables, you first make
a variable that has 20px and then you use it for all other attributes using px. For example, 20px / 4px is 5px for the padding, and 20px / 2px is 10px for
the font size.

#### Example
SCSS
```SCSS
.message {
  border: (12px - 2px) solid #ccc;
  padding: 20px;
  color: #333;
}

$container-width: 100%;

.container {
  width: $container-width;
}

.col-lg-4 {
  width: $container-width / 4;
}
```

CSS
```CSS
.message {
  border: 10px solid #ccc;
  padding: 20px;
  color: #333; }

.container {
  width: 100%; }

.col-lg-4 {
  width: 25%; }
```
## Tips

#### Know when to use `sass --watch input.scss:output.css`
There are times when you either need `sass input.scss output.css` or `sass --watch input.scss:output.css` in order for your CSS file to get changes
from your SCSS file. Use `sass input.scss output.css` if you are adding minor changes to your SCSS file and, use `sass --watch input.scss:output.css` if
you are planning on making major changes to your file that requires time.
