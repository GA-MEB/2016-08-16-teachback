[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# CSS

## Objectives

 At the end of this session, you should
 (with the help of a reference, and a little time)
 be able to:

 - Add CSS styling to an HTML page.

 - Write CSS rules that affect the styling of a page.

 - Use CSS specificity and cascading rules to predict how a given element
  should be styled.

 <!-- - Use advanced selectors and pseudo-classes to select groups of elements with
 more granularity. -->

## Prerequisites

 You should already be able to:

 -   Build a static HTML page.

## Writing CSS

### [Read: CSS Fundamentals](./readings/css-fundamentals.md)

### Discuss : CSS Fundamentals

### Watch: Use CSS to Style HTML

<!-- DEMO INSTRUCTIONS -->
<!--
1.  Create a new folder called `webpage`, and create a boilerplate HTML file
    inside of it. Add some <div>, <p>, and <h_> elements.
2.  In that same directory, create a CSS file called `main.css`, and add a link
    element to the HTML in order to load the CSS.
3.  Create an example CSS rule for the <div> elements. Pick any two properties
    to define.
4.  Create another example rule for the <p> elements. Pick two different
    properties from the ones in the first rule.
5.  Create a third rule, applying to <div> elements, but using the same
    properties and values as the second rule.
6.  Demonstrate using a comma in the CSS selector as a way of reducing the
    number of rules required.
7.  Assign some <p> and <div> elements membership in a class; then, define a
    style rule to pply to those elements.
8.  Assign one particular element within that class an ID. Create a style rule
    for that ID, but **don't** overlap with the class rule.
-->

### Do: Use CSS to Style HTML

Take the [provided HTML starter code](./exercises/news-site.html) and add the
following features using CSS styles. You may need to do a little Google
searching to find the answers you're looking for.

> **{Common Pitfalls}** Don't forget to link to your new style sheet
> from the HTML file!

1.  Every article should have a grey (`#DEDEDE`) background color.

2.  The font for all headings (h1, h2, etc) should be "Times New Roman"

3.  Make the font size of all the articles' text content (i.e. not the headings)
    20 pixels.

4.  Center the text in the top-level heading.

### [Read: Mechanics of CSS](./css-mechanics.md)

### Discuss: Mechanics of CSS

### Watch: Override Existing Style Rules

<!-- DEMO INSTRUCTIONS -->
<!--
Go back to the prior example, and show how new style rules can be defined which
override the instructions of the prior rules. Give
-   one example of inheriting properties from a parent element (and/or having
    default values for properties)
-   one example of a class-level instruction overriding a tag-level instruction
-   one example of an ID-level instruction overriding a class-level instruction
-   one example of a class-level instruction overriding an earlier class-level
    instruction
-   one example of a tag-level instruction overriding an earlier tag-level
    instruction
-->

### Do: Predict Styling by Reading CSS

Read through the [blog.html](./exercises/blog.html) and
[blog.css](./exercises/blog.css).

Each bullet point below lists a property for some element or group of elements;
using what you've learned about CSS, write down what you predict the value of
each property will be. When everyone is finished, we'll compare our answers and
then actually load the code to see if we were right.

1.  Font color of items in the first list.
2.  Background colors of the two links in the header.
3.  Background color of the first article.
4.  Background color of the first paragraph in the article.
5.  Font size of list headings.
6.  Background color of the footer.
