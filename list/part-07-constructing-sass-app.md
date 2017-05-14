## Part 7: Constructing SASS App

### My SASS application idea

My idea of a SASS application is making a website that constructs a webpage layout template.
This will benefit people who are unfamilar with HTML and CSS since it will give them a visual representation of what everything does in their webpage/website
and how you want it to function. All of the HTML tags shown in the template will be color-coded, including the buttons that  add the HTML tags in the page template.

![My current project](../images/PreviewProject.png)

### How the app is created so far
``` SCSS
$TopColor:#2ecc71;
$pseudo-title-color:#a3b8f7;
$pseudo-textbox-color:#f7e9d4;
$pseudo-image-color:#ed9982;
body{
  font-family:'Ubuntu', sans-serif;
}
@function set-notification-text-color($color) { //name of function, what variable it grabs, $color = placeholder name
  @if (lightness($color) > 50) {
    @return #000000; // If background color is light, return dark to $color
  } @else {
    @return #ffffff; // Else, return light color to $color
  }
}

.selection{
    border: none;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    opacity: 1.0;
    background-color:#d0f2ef;
}

%pseudo-position{
  padding: 16px 16px;
  margin: 8px auto;
}
.pseudo-title{
  background-color: $pseudo-title-color;
  color: set-notification-text-color($pseudo-title-color);
  @extend %pseudo-position;
}
.pseudo-textbox{
  background-color:$pseudo-textbox-color;
  color: set-notification-text-color($pseudo-textbox-color);
   @extend %pseudo-position;
}
.pseudo-image {
  background-color:$pseudo-image-color;
  color: set-notification-text-color($pseudo-image-color);
   @extend %pseudo-position;
}
```

For now, all of the colors for my project are in different variable just for quick referencing such as the color for image and textbox.
Every tag in my HTML matches with their corresponding class in SCSS , for example H1 having the pseudo-title class. In terms of looks and postion, 
every pseudo class has the same position since they all get their attributes from `%pseudo-position`.

### Internal Questions

#### How would I apply SASS to my app?

I will use SASS to help create the visualizations of my page template application such as the text and the color for specific tags. Additionally, SASS will help me organize my app
so that every element of my page has the proper CSS attributes from SASS. 

#### Is my idea of an app possible to create?

As of now, I am having no trouble with making my app idea into a reality. However, I am aware that there will be roadblocks up ahead in the future. For instance, I am still trying to 
figure out how to update the webpage when the user clicks on a button to add an HTML tag on their template. I am currently looking for a solution to this issue in case it becomes troubling
for me to figure out.

### Takeaways

#### Try to make something that is doable and not difficult for you to do

When planning out my project, I try to understand all of the possible challenges that I might run into and whether or not I am determine to find the solutions. Try to create something that suits you
and does not cause much stress as sometimes you need to start with something that is in your level of committing to it.