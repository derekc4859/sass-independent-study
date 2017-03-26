# Part 1: The Intro

## Why Did I Choose SASS?

I decided to study SASS because I wanted to study something that is balance for me and does not give me much trouble.
Also I always had an interest with CSS and I wanted to improve on my skills. SASS will benefit me in the future as I 
want my websites to have a great layout and not look dated.

## What is SASS?

SASS does not mean being rude to someone. SASS is a scripting language using Ruby to create stylesheets for CSS. 
In a nutshell, SASS is an add-on to CSS, allowing you to use variables, nesting, 
a hierarchy similar to HTML , and inheritance. The syntax in SASS resembles basic CSS,
except there is another syntax for SASS that allows to use syntax like HAML.

#### Example
##### SASS
``` $font-stack:    Helvetica, sans-serif;
$primary-color: #333;
$secondary-color: #7f8c8d;
$font-small:   "Lucida Sans Unicode", "Lucida Grande", sans-serif;

h1 {
   font: 300% $font-stack;
  color: $primary-color;
}

h3 {
  font: 100% $font-small;
  color: $secondary-color;
}
nav {
  ul {
    margin: 1%;
    padding: 1%;
    list-style: none;
    font-family: 'Source Sans Pro', sans-serif;
  }

  li { display: inline-block; }
}

```
##### CSS

```
h1 {
  font: 300% Helvetica, sans-serif;
  color: #333; }

h3 {
  font: 100% "Lucida Sans Unicode", "Lucida Grande", sans-serif;
  color: #7f8c8d; }

nav ul {
  margin: 1%;
  padding: 1%;
  list-style: none;
  font-family: 'Source Sans Pro', sans-serif; }
nav li {
  display: inline-block; }
```
## How to install SASS

In order to install SASS into your workspace terminal , you type in `gem install sass`.
If you are unsure that SASS is installed, type in `sass -v`.
If `sass -v` does not return `Sass 3.4.23 (Selective Steve)`, then SASS is not installed in your
workspace terminal. In case `gem install sass` does not work at all, then try `sudo gem install sass`.

## Saving your SASS file as a CSS file

Once you are done with all of your necessary changes in your SASS file, you can save your changes into
a CSS file by running `sass input.scss output.css` inside of your terminal. Once you did that, you should
see `output.css` in your workspace with all of your changes from your SASS file.

Note: SCSS is another name for a SASS file

## Variables

Unlike CSS, you can use variables in SASS. Variables in SASS can store font-families, sizes, styles, and more.
To make a variable, you add a `$` and name it whatever you like. Variables are beneficial in SASS as there might be
a moment where you want certain elements to have the same properties. For instance, you want your h1, h4, and p tags 
to have the color purple and arial font. With variables, you can make sure that all these tags
have the same properties.

## Tips

#### Workspace is your best friend

If you want to make sure that your CSS file successfully gets your up to date changes from your SCSS file,
put your SCSS file to the left of your workspace and your CSS file to the right of your workspace. That way,
you are able to make sure that your changes are working well on both ends of your files.

#### Be sure to take notes while you are studying on your own

There will always be a moment when you find something that may be helpful in the near future, but you want to make sure
that you don't forget about it. That is why you should consider taking notes while you are studying as it will be a good 
point of reference in case you want to use something that you learned awhile ago.