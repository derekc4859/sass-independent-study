# Part 5: Compass

## Compass
Compass is an add on to SASS that allows you to organize your SCSS and CSS files in seperate folders and, keep track of changes from a specific SCSS file to CSS
When I was using Compass to start creating my app, I spent less time trying to find a file since everything was organized clearly and I was able to look at my changes from 
my CSS file.

### How to install Compass
Before you install compass in your workspace, you first need to install SASS and cd to your project folder. After that, use `gem install compass`. Once you install compass, you will 
get two folders in your project folder. One folder has SCSS files and the other folder has CSS files. 

[Example](../images/example.png "Logo Title Text 1")

### Getting the latest changes from SCSS using Compass
You need to cd into your new CSS folder if you want a CSS file to get the latest changes. When you are in your CSS folder, use `compass watch example.css` to track any SCSS file of the same name 
to give changes to the CSS file.

## Takeaways

### Be careful with syntax

One small syntax can cause an important part of your SCSS file to not function properly. When I was debugging my SCSS file, I had no clue what was the cause of my error. But eventually, I found out that
I was stressing out over a missing semicolon. Because of this event, I learned that when I am debugging, I have to maintain my cool and look for every possible solution to my problem.

