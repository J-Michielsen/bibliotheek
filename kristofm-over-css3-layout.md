IT3 - micro-cursus 1: layout

CSS evolve to the increasingly complex language it is today

From the very beginning of CSS, there has been a giant, lay- out-shaped hole at its center.
table
float 'clear'
positioning
hacking our way to layouts with floats
Flexbox came first / upending what we think about layout
Now => grid layout

Multi-column layout

This module is the most mature and has the most browser support of all the modules I will cover in this book so is a great place to start our exploration of all that is new in CSS layout.

Multi-column layout makes it possible to arrange content in columns, in the same way that content flows in a newspaper. You can take a container in your document and state that you want it to be arranged into columns, and the browser will make it so. If you specify the number of columns that you want the content arranged into, the browser will work out the width of each column so that it will fit into the parent box. If you specify a width for the columns then the browser will display as many columns as it is able, maintaining that width for each.

Specifying a column-width means that the browser will fit as many columns into the container as possible, using the specified width as the ideal width. You may notice that when we specify the width for columns we don’t in fact get that exact width. The columns will always be even in the space, so the browser will work out how many columns can fit as close to the specified width as possible. The specification says;

Therefore, when setting the width you should specify the optimal column width, though it may be that the actual width is different – especially in a flexible design.
You can also specify how many columns you want and then let the browser decide how wide they should be, using column-count.

You can also see in my examples that the columns do not butt up against each other: there is a gap between each column. In the multicolumn layout specification this gutter is controlled by the column-gap property. If you set column-gap to zero there will be no space between columns and the text will run together. The specification suggests that user agents use a value of

1em as the default for this property; however, if you want to ensure your gutters are a certain width to line up with a grid, then you should set a value yourself..

Column styling is relatively limited in the current specification // At present you cannot style columns individually. There is no way to set margins and padding on a column, or set the width or background colour of an individual column.

We can, however, use a rule to divide our columns. This is achieved by way of column-rule properties:
• column-rule-style • column-rule-width • column-rule-color
These properties behave in the same way as border- style, border-width and border-color and can also be written as shorthand using the column-rule property:
column-rule: width style color;
The column rule is placed centrally in the area created for the column-gap. To change the space on either side of the rule, adjust the value you used for the column- gap property. If the rule is wider than the available gap then it will start to overlap text in the columns – it does not take up any space itself.

Column span
If you would like an element to span all columns then you can give the property column-span a value of all. In the following example, I want the main h1 heading to span across all columns.
Example 1-5. Causing the h1 to span all columns

Column breaks
When using multicolumn layout you have control over how columns break. This can be useful where there are elements that you would prefer not to end up wrapped into a new column, or when you want to make sure a certain element always starts a column.
Example 1-6. Avoiding breaks inside paragraphs and before blockquotes
.main p { page-break-inside: avoid; }
.main blockquote { page-break-before: avoid; }
Printing and paged media
The specification states that multicolumn elements should not continue on to the next page. It would be very annoying if you had to read down one column, onto the next page and then back to the first page to start reading at the top of the next column!
You can also determine how the content behaves when a page break falls in the middle of a paragraph or other element – just as you can control breaks when the content wraps into new columns. The properties avoid- page and avoid-column give you finer control. If you

are happy for paragraphs to break across columns but not pages, in the example above you could use break- inside: avoid-page rather than just avoid.
Responsive design
The multicolumn layout module is useful for responsive design as the specification means that the columns are responsive by default. As we have seen, the column width setting only sets the most desirable width for the column: the browser is left to work out the actual width.
An image placed inside a column will be constrained by the column width, so the standard method of scaling down an image by using max-width will work within columns. If you do not set max-width: 100% on an image, and the image is wider than the column, then the browser will crop the image. This behaviour is the same for any element within a column that is wider than the current column width.

CSS Flexible Box Layout

The CSS flexible box layout module, commonly referred to as flexbox, gives us a brand new layout mode in CSS – flex layout. It has been designed to make it easier to layout complex applications and webpages. In this section, I take a look at some of the main layout problems flexbox can solve.

Spacing items evenly

Taking a group of items and spacing them along an axis is a task that has traditionally been rather difficult in web design. Floated elements need a width, yet each one might be a different width and getting them all to fit on a single line with equal spacing usually involves some JavaScript. Flexbox makes this task easy. In my markup I have a list that contains my navigation.

Had we set the value of justify-content to space-around then the space would have been added all around each element equally, meaning that instead of being flush to the outside edges of the container, there would be some space before the first and after the last element.

The simple example above uses some default behaviour of flexbox. The items here have been displayed as a row. This is the default behaviour and is equivalent to setting the property flex-direction to row. The flex-direction property can have one of four values: row; row-reverse; column; and column-reverse. These enable you to display the items in a row, or reverse their order in a row; and similarly in a column, or a column with the order reversed. Example 2-3: Setting flex-direction nav ul{ display: flex; justify-content: space-between; flex-direction: row-reverse; }

Equal height columns Another interesting aspect of flexbox is that it enables you to create equal height boxes, even if the content of some boxes is longer than others. The default value of the property align-items is stretch. This stretches each item in the group to the height of the tallest. You can see this in action in our navigation. I've added some text to one of the items making it taller than all of the others, but each item now grows to the height of the tallest item keeping the columns lined up neatly.

The property align-items can also take the following values: • flex-start • flex-end • center • baseline • stretch To understand how these work you need to realise that flexbox has a concept of two axes: the main axis, along which items flow; and the cross-axis. By setting flex-

...


Grid Layout, kortweg "Grid"

proposal by Microsoft in April 2011
De kans is bijzonder groot dat Grid Layout de layout methode is waarop we allen hebben gewacht
defines a two-dimensional grid layout system. Once a grid has been established on a containing element, the children of that element can be placed into slots on a flexible or fixed layout grid. The grid can be redefined using media queries, rendering the source order of the child elements unimportant.

vitally important that we, as developers and designers, get involved early.
Daarom ook nog niet aangeleerd in jaar 1. Maar dit zal snel veranderen.

First, activate Grid by entering the following line in your browser address bar:

chrome://flags/#enable-experimental-web-platform- features

Then, turn on the Enable Experimental Web Platform Features flag and restart Chrome.

De basics

Een grid definiëren

A grid is defined using a new value of the display property, 

display: grid.

Next, I need to describe what the grid looks like. Grids have rows and columns,

grid-template-rows

grid-template-columns

We can sort this out by deliberately positioning our items on the new grid. T

You just need to specify the line where the content will start and the line where it will end.

GRID TERMINOLOGY

Before going any further, let’s take a few moments to understand some of the terminology used when talking about Grid Layout.

Grid lines

Grid lines make up the grid and can be horizontal or vertical. They can be referred to by number, as I have done so far, but they can also be named.

Grid track

A grid track is the space between two grid lines. It can be either horizontal or vertical.

In the examples shown in FIGs 1.1–1.3, we have grid tracks representing content cells and grid tracks representing gutters. As far as the grid is concerned, these are the same thing. So when positioning using numbered lines, remember that the gutter lines exist and be sure to include them when working out where content starts and ends.

Grid cell

A grid cell—the space between four grid lines—is the smallest possible unit on the grid. Conceptually, it is just like a table cell.

Grid area

A grid area is any area of the grid bound by four grid lines. It can contain a number of grid cells.




