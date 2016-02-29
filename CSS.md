#CSS

[TOC]

We can give multiple elements the same rules by delitering them with a comma.

##Relative units

- **px** - number of pixels, dependent on screeen resolution.
- **em and ex** - size relative to current font size
- **%** - is a percentage of the page.
- **larger/smaller** - scale up and down from the current font size, usually by a factor of 1.2

##Representing colour

- hex - a hexedecimal colour.
- hex short - #0000FF -> #00F

##Levels of CSS

- external - styling a .css file
- document - placing a style tag
- inline - styling individual elements.

****Note that class selectors are more robust than id selectors.****

###Specificity

However above this there are rules within CSS files that govern how the end result will look:

- If two or more blocks have the same specificity the **last** will take effect.


##The Box Model

![Box Model](box-model.gif)

This is the design layout of HTML elements. Each element is wrapped in a box that looks like the box above.

_But not all elements have these properties, which leads to differences between browsers_

##Animation

