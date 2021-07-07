# Introduction to SCSS

> SCSS (Sassy CSS) is CSS on steroids lol

As your web projects expand in size, you'll start to see the advantages that SCSS brings over regular CSS. There are key features that make SCSS significantly better than CSS:

## 1. Variables
SCSS can save you from rewriting a lot of CSS code. Pretend that you are following a color theme, and you want elements to be a specific color [rgb(52, 235, 189)](https://www.color-hex.com/color/34ebbd).

If you're using CSS, you'll have to write this for *every* element. SCSS, though, lets you do this:
```
$myColor = rgb(52, 235, 189);

...

h1 {
    color: $myColor;
}

div {
    color: $myColor;
}
```
There's now a method of using variables natively in CSS (custom properties), but this syntax is slightly easier.

## 2. Nested Elements & Styling
Once your HTML gets complex enough, you'll find yourself doing this a lot:
```
.parent {
    // styles
}
.parent > div {
    // more  styles
}
.parent > div > span {
    // even more styles
}
...
```
**SCSS to the rescue!**
```
.parent {
    // styles
    div {
        // more styles
        span {
            // even more styles
        }
    }
}
```
Not only does this result in less code written, it allows developers to get a sense of HTML structure when styling, which saves you time and removes potential bugs.

## 3. Importing
Nobody wants a CSS file that's 600 lines long. SCSS allows you to split your styling to multiple files without linking files manually. For example, you have a homepage with a special section following a specific color scheme. 

To do this, you can have a separate SCSS files `_colorVariables.scss` to define your color variables and `_section.scss` for styling specifically for that section. The beginning of your `index.scss` can look like this:
```
@import "colorVariables"
@import "section"

// insert styles below
```
Simple, right?

---

[Let's get started with SCSS, shall we?](./SCSS-Setup.md)