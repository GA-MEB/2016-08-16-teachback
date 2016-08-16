[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# CSS Mechanics

## Resolving Conflicts

One of the core problems of defining a system of rules is determining how to
resolve situations where the rules (inevitably) disagree. Consider the example
below.

```css
/* Rule 1 */
div {
  color: red;
}
/* Rule 2*/
p, div {
  font-size: 20px;
  color: blue;
}
```

The second style rule is being applied to all `<p>` elements _and_ all `<div>`
elements. Since the two rules prescribe different styles for `<div>`
elements, what does the browser do?

CSS has three guiding rules for handling these kinds of conflicts.

### 'Play Nice'

The first guiding rule can be thought of as the 'play nice' rule -- all
properties whose values are _not_ in conflict get applied normally.
In the example above, even through rules 1 and 2
disagree about the color of the text, they don't disagree about the font size,
so we can say with certainty that the text will have a font-size of `20px`
(20 pixels).

In cases where properties's values are not defined by _any_ rules, they will
will _inherit_ properties from their parent elements. For instance, if we write
the following CSS rule:

```css
body {
  background-color: teal;
}
```

all elements inside the body will inherit a teal background color, unless
another style rule explocitly says otherwise.

If the parent element doesn't define values for those properties either, the
element will just take on their default properties (for instance large text for
`<h1>` elements).

### 'Specificity'

The second rule is the 'specificity' rule. CSS has an algorithm to calculate a
'specificity value' for a given selector; the rule whose selector has a higher
specificity value gets to decide the value of a contested property.

We won't get into the full technical definition of specificity right now, but a
good short-hand summary of the algorithm is:

- Class selectors are more specific than tag-name selectors.
- ID selectors are more specific than class selectors.

This means that if a class rule and an ID rule are both applied to an element,
and they disagree about the value a property should have, the ID rule is the one
that is followed.

### 'Cascading'

This rule is part of what gives CSS its name. Cascading means that if you have
two rules of _equal specificity_ (for instance, two class rules applied to the
same element), the rule that comes later on (i.e. lower down) in the file is the
one that's applied.

> One way to think of it is to imagine all of the rules being applied in order
> from the top of the file to the bottom; the lower rule has the "last word".

This is why, when we load CSS files in our HTML, the order of our `<link>`
elements is important -- CSS files added lower down in the HTML get loaded
'later' the files added higher up, allowing them to potentially override style
rules from the other files.

### Summary

Although there's more to learn about CSS (for instance, more complex kinds of
selectors, or the nuances of how specificty works), these three rules are enough
to almost completely describe how CSS behaves.

[< Back](../README.md)
