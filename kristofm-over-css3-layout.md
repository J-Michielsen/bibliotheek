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

! uitproberen

Grid gutters

The examples in this little book all achieve gutters by way of a grid track that serves as a gutter between tracks used for con- tent. This is a valid approach, and is, in fact, necessary if you want to create a complex grid using different gutter widths.

As I was preparing this book, a grid-column-gap property was added to the Level 1 specification. This property behaves much like column-gap in multiple-column layouts. Also, for Grid we have grid-row-gap to create spacing between rows. These properties have a shorthand of grid-gap, which allows you to specify both row and column gaps at once.

Because grid-column-gap and grid-row-gap were not implemented in any browser at the time of writing—making it into Chrome Canary at the final moment—I have omitted them from my examples. For simple grids, these properties will serve to reduce the amount of CSS required.

Nog iets zeggen over span?

LINE-BASED PLACEMENT WITH NAMED LINES
Remember: we are naming grid lines, not tracks.

No strange hacks required!
Grid truly allows us to separate document structure from presentation.
create dramatically different
layouts for any viewport or particular use without compromis- ing the document’s structure.

LAYING THINGS OUT ON THE GRID

A THREE-COLUMN LAYOUT USING GRID-TEMPLATE-AREAS

Nested grids and subgrids

Our nested grid in this example is completely independent of the main grid. The container .content is positioned by the main grid, but the child elements are not—they acquire their grid from the way we set up .content.

This means we can’t inherit column widths from the parent, which is a problem if you want to use flexible length units: you’ll find it tricky to get the elements in the nested grid to line up with those in the outer grid.

The specification has a solution for this: the subgrid key- word. If we were to use subgrid, we would use it as a value for the grid property:

.content {

grid: subgrid;

}

This comes in handy particularly when basing our layout on grid systems such as the twelve-column and sixteen-column grids that are currently popular. In most cases, you’ll want the children of nested elements to use the lines of the outer grid rather than implement their own grid.

At the time of writing, however, it looks as if the subgrid keyword will be moved to Level 2 of the specification, and there is currently no browser implementation of this functionality. My concern is that if this doesn’t make it into the specification, authors will flatten their markup structure, removing semantic markup, in order to use Grid.

Note that I used the repeat keyword when setting up this example. This simply saves me from having to write out my gutter and col pattern thirteen times. Between parentheses, I have the number of times that I want the pattern to repeat, followed by the pattern name.

The specification has recently been updated to allow the number of repeats to be auto. This means that a pattern can repeat as many times as the content requires. At the time of writing, this is not implemented in any browser. If it were, then our row pattern could be written as follows:

grid-template-rows:

[row] auto repeat(auto, [gutter] 10px [row] » 60px);


CSS GRIDS AND RESPONSIVE DESIGN

IF YOU’VE MADE IT THIS FAR, you probably already have some idea of how useful CSS Grid Layout will be when working with responsive layouts. Proper separation of document source from presentation is something we have aimed for since the early days of CSS. Whenever I’ve been involved in developing a responsive design, though, I’ve always had to make compro- mises between source order and getting the most desirable layouts for each breakpoint. Grid, along with Flexbox, makes this far more straightforward.

To see how, let’s look at some of the things we created in the last chapter, starting with the three-column layout using grid-template-areas (FIG 2.1).

Redefining grid-template-areas with media queries

Once again, I start by setting up all of my grid areas, for both the main grid and the nested grid on the article, with a class called .content.


