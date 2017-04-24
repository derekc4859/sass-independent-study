# Part 4: SASS Functions

## Functions

As I have been searching on Google for more things to learn about SASS, I stumbled upon SASS functions and how they function(no pun intended).
First of all, SASS functions are not like Ruby and Javascript functions as they do not need a name and are just used to change color styles such as 
lighten a color, or changing the saturation of a color.

## How do functions function?

In SASS, you use a function by determining what color aspect do you want to change such as `saturate()` or `darken()`. After that, you add the hex color code
(Personally, I prefer using variable as it keeps track of the hex code) and the amount of color that you want to change in percentage. There are some functions
that do not require a percentage. When the file is carried over to CSS, the function will change into a hex code.

### Example
Note: Notice the hex code number

SCSS
```SCSS
.darkness{
  $boxcolor: #9276e0;
  background: darken($boxcolor, 30%);
}
```
CSS
```CSS
.darkness {
  background: #42239a; }
```

#### Darken() and Lighten()
The darken function makes a color darker while the lighten function does the opposite.

#### Saturate() and Desaturate()
The saturate function makes a color more saturate and the desaturate function makes color
dull
### Why would functions be beneficial?
There are certain situations where you need a background to have the same color but with different shading. 
Sometimes you would need a color to be consistent but at the same time, make it unique without having to use too many colors.
## Tips

### Do Not Neglect the Color Picker
I would use the color picker on Google to make sure what colors to try out and see what is the color of the hex code that the function gave
to me. As you start using more functions, use the color picker as your companion as you can use it to determine what colors to use.