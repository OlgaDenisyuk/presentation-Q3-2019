# CSS GRID LAYOUT


Hello! My name is Olga. The title of my presentation is CSS Grid Layout.
In my work I would like to consider the basic consepts  of a technology such as Grid CSS. I also show the differences between Grid and Flexbox, and point out when it is preferable to use a particular technology - Flex or Grid.


### Slide 1
### What is a Grid?

**The CSS Grid Layout Module** - it is a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.


### Slide 2
### Basic concepts

Consider the basic concepts.

**Grid container** - parent element in which the grid is located.

**Grid lines** -  the lines between columns and rows. It is called column lines and row lines respectively. In the picture, lines are marked in red.

**Grid track** - it is a space between any 2 lines on the grid.

**Grid cell** - is a smallest unit of a grid. On the picture cell has an orange color.

**Grid area** - when elements span one or more cells both by row or by column.


### Slide 3
### Display Property

An HTML element becomes a grid container when its display property is set  to grid or inline-grid.
Let's  look at the element with class "wrapper", which contains 5 child elements. Property of this element are set to "display:grid".
All the direct children are now grid items. But in a web browser we won't see any difference in how these items were displayed before. Why? Because grid has created a single column grid for the items.
if we indeed want to see the difference, we can use the Grid Inspector from Firefox's Developer Tools. In Firefox we can see a small icon next to the value grid. Click this and the grid on this element will be overlaid in the browser window.


### Slide 4
### Grid tracks

If we want to see not only rows but also columns of the grid, we can use the following properties:

*"grid-template-columns" which defines the columns of the grid.
*"grid-template-rows" defines the rows of the grid.

Set div property "grid-template-columns" with 3 values equal 300px.
Now we have a grid with 3 column, each of which is equal = 300px and 2 rows.
We can see now that the columns do not occupy the entire width of the parent container.

### Slide 5
### The fr unit

For a uniform distribution of elements in the grid, a unit of length "fr" can be used:

*grid-template-columns:1fr 1fr 1fr;

This record means that the grid has 3 columns of the same width. 
As we remember, with Flex we can't achieve such an accuracy. With Flexbox we use approximate percentages or a calculator function.
Therefore, in these cases it is preferable to use Grid tehnology.
Also "fr" can be mixed with other values.
In this example an element named "Two" is given first and has width equal to 500px.
The element named "One" has width equal to 1 part, and third column has width equal to 2 parts.


### Slide 6
### Repeat()

Notation Repeat()
When we have large grid with many tracks we can use repeat() notation.
We can write this example differently  - with notation repeat().


### Slide 7
### Grid lines

**Grid lines** - the lines between columns and rows. 
Look at the screen. In the grid with 2 rows and 3 columns we have 3 row lines and 4 column lines.


### Slide 8
### Grid area

**Grid area** - rectangle area bounded by 4 greed lines: grid-row-start,grid-column-start,grid-row-end, grid-column-end

Take a look at the picture.
div with class "box1" has area between the following lines: row lines - 1 and 3,
column lines: 1 and 4.

Let's look at the examples and determine what it means.

**First example:**
In right part we can see integer and everything is clear here.

**Second example:**
row 2 - it is grid-row-start
span 4 - it's a keyword with an integer that determines how many columns of the grid an element will span.

**Line name** - specifies the name of the grid item.

To make it clear, consider picture number 2.
On this picture we can see named elements which define layout of the page.

We can use a property "grid-template-areas", which define the structure of our grid.
We see 4 columns and 4 rows. The Header takes 4 columns and 1 row.
Now we can see how easy it is to set the page layout using just 1 property.
Using Flexbox, we couldn't do it so fast.


### Slide 9
### Gutters

Gutters between grid cells can be created using the "column-gap" and "row-gap" properties, or the shorthand gap. Using this style we  set the next gutters and see how it will look in the browser.
Flex uses the property "margin" to set the gutters between the elements. It is not always make sense since at the end we have the gutters not only between elements, but also between elements and parent container.


### Slide 10
### Z-index 

Grid items can occupy the same cell. In this picture you can see this case. Element named "One" overlaps element with content "Two".


### Slide 11
### Grid vs Flexbox

I called it Grid against  Flexbox.  After comparing these two technologies we can come to **conclusion:**
Unlike Flexible Box Layout, which is single-axis-orient, Grid Layout is optimized for 2-dimensional layouts, in which alignment of content is preferable in both dimensions.
If we intend to perform multiple calculations of the element width, then it is better to use Grid CSS. 
Flexbox technology allows you flexibly control layout of items. For example, direction, horizontal and vertical alignment. Where it is necessary to use such properties, Flexbox would be more suitable.




