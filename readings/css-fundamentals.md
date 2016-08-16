[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Using CSS to Style HTML

## The Ascendence of Style Rules

Let's start off with a little history.

Back in the earliest days of web development, web pages were restricted to text
(though images would follow soon). The only styling was the styling
that came pre-built with different HTML elements. If you wanted to customize
that at all, you needed to use style-related HTML elements, such as `<b>`
(bold). In May of 1996, HTML 3.2 was released, which for the first time allowed
things like fonts, colors and backgrounds to be defined, using a 'style'
attribute.

CSS entered the scene in December of that year. Its chief advantage was that it
allowed for the separation of content from design. This separation is useful for
several reasons, including:

1.  Having separate files for content and style make it easier to view the raw
    content.

2.  Debugging an issue with your page became simpler, since if it was a style
    issue, you would often only need to look at the CSS file.

3.  Since HTML files needed to reference the CSS files they wanted, they could
    all reference the same file, allowing a developer to control all styling on
    a site from a _single document_.

## Adding CSS to an HTML File

HTML files can reference CSS stylesheets using a special HTML element called a
`<link>`. This tag usually goes in the `<head>` section of the HTML page, and
contains a link to the CSS file that you want to reference.

e.g.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Example Page</title>
    <link rel='stylesheet' type='text/css' href='stylesheets/main.css'>
  </head>
  <body>
    <!-- ... -->
  </body>
</html>
```

You can also load more than one stylesheet - the browser treats this as if you'd
written one giant CSS file, with the content from the first CSS file on top.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Example Page</title>
    <link rel='stylesheet' type='text/css' href='stylesheets/main.css'>
    <link rel='stylesheet' type='text/css' href='stylesheets/special-extra-styling.css'>
  </head>
  <body>
    <!-- ... -->
  </body>
</html>
```

The ordering for these files matters, and the reason for this has to do with the
way that CSS calculates how to style each element, which is what we'll be
looking at next.

## CSS Basics

CSS provides a system for defining rules on how to style the elements in a page.
The syntax for these rules is

```css
selector {
  property: value;
  property: value;
}
```

`selector` is a reference to an element or group of elements;
each `property` is a style property like `background-color`, `font-size`, etc;
each `value` will depend on the property being defineed, but could be something
like a number of pixels, a color, or a specific font family.

Here's some actual CSS code. The `div` selector below will select every `<div>`
element in the HTML page, and the `p` selector will do the same for `<p>`
elements.

```css
/* Rule 1 */
div {
  color: red;
}
/* Rule 2*/
p {
  font-size: 20px;
  color: blue;
}
```

In addition to selecting every element of a particular type, CSS allows us to
define select custom groups of elements called _classes_. You can indicate that
an HTML element is a member of a particular class by setting its `class`
property. You can add that element to as many classes as you want in this way.

```html
<div class="column middle-column"> <!-- ... --> </div>
<!-- This div element now belongs to the 'column' and 'middle-column' classes. -->
```

The selector for a class is `.`, followed by the name of the class. For example,

```css
.middle-column {
  width: 300px;
}
```

Finally, you can also assign a special name, or _ID_, for one particular
HTML element by setting its `id` property. IDs are intended to be unique --
an ID refers to only one element, and an element has only one ID.

```html
<div class="column middle-column" id='special-column'> <!-- ... --> </div>
```

The selector for an ID is `#`, followed by the ID name.

```css
#special-column {
  background-color: yellow;
}
```

Between classes and IDs, it's generally preferred to use classes for styling;
the reason for this has to do with the mechanics of CSS, which we'll look at in
the next reading.

[< Back](../README.md)
