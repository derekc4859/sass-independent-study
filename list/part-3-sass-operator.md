# Part 3: SASS Operators and New Tricks

## Applying changes without `sass input.scss output.css`

You can add changes to your SCSS file and apply them to your css file without having to use 
`sass input.scss output.css` repeatedly. Using `sass --watch input.scss:output.css` allows your CSS
file to get the latest changes from your SCSS file automatically. However only one CSS file can get automatic changes
from a SCSS file. If you want a different CSS file to get new changes from another SCSS file, then you will have to stop 
`sass --watch input.scss:output.css` by using `control + C`

NOTE: When using `sass --watch input.scss:output.css`, make sure that the changes you made on your scss file are correct 
since your css file might encounter an error if there is a mistake on your scss file that the css file is getting the changes
from.

#### Example of error

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


## Tips

#### Know when to use `sass --watch input.scss:output.css`


