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
.main p { break-inside: avoid; }
.main blockquote { break-before: avoid; }
Printing and paged media
The specification states that multicolumn elements should not continue on to the next page. It would be very annoying if you had to read down one column, onto the next page and then back to the first page to start reading at the top of the next column!
You can also determine how the content behaves when a page break falls in the middle of a paragraph or other element – just as you can control breaks when the content wraps into new columns. The properties avoid- page and avoid-column give you finer control. If you

are happy for paragraphs to break across columns but not pages, in the example above you could use break- inside: avoid-page rather than just avoid.
Responsive design
The multicolumn layout module is useful for responsive design as the specification means that the columns are responsive by default. As we have seen, the column width setting only sets the most desirable width for the column: the browser is left to work out the actual width.
An image placed inside a column will be constrained by the column width, so the standard method of scaling down an image by using max-width will work within columns. If you do not set max-width: 100% on an image, and the image is wider than the column, then the browser will crop the image. This behaviour is the same for any element within a column that is wider than the current column width.
