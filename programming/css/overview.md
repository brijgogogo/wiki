= css =
Cascading Style Sheets
style - an instruction to the browser to modify how it displays something on the page
- formatting, typeface, text color, page layout, animations etc.
cascading - styles can take different routes before they get applied to an element. They come from browser, user, style sheets.


HTML - defines overall structure of the web page
CSS - defines the visual presentation of the web page

== basics ==
* [[selectors]]
* [[units_of_measurements]]
* [[fonts]] (typefaces)
* [[colors]]
* [[images]]
* [[paragraph]]

= Page Flow =
Browser lays out elements in the order in which they appear in the HTML file.
- block-level elements are stacked vertically
- each inline element is rendered from left to right within its parent block element.

# Floating
Browser takes the element out of the usual flow and places it to the left, right and high (depending on value). Rest of the page content flows around the floated element.

float: left|right|none;

When you apply float property to an inline element, browser takes the element out of the normal flow, turns it into a block-level element, and then floats it.

# Clearing
Clearing a floated element means that the browser renders the element after the end of the floated element.
clear: left | right | both | none;

collapsing problem: if all elements of a block-level element are floated, it collapses.

# clearfix hack
.self-clear::after {
  content: ""; // inset an empty string
  display: block; // make it a block
  clear: both; // clear both left and right
}

semantic class name: group (instead of self-clear)

# Drop Cap - big first letter of paragraph
uses pseudo-element
.first-paragraph::first-letter {
  float: left;
  padding-top: .1em;
  padding-right: .1em;
  color: darkred;
  font-size: 5em;
  line-height: .6em;
}

Similar is Raised cap.

# Pull quote - short excerpt from article, that's set off from the regular text.
Draws a visitor in site who might not otherwise read the article.

Gets applied on <span> inside the paragraph.

.pullquote {
  float: right;
  width: 50%;
  margin: 1.25em 0, 1em .25em;
  paddint-top: .5em;
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  font-size: 1.05em;
  font-style:italic;
  color: #666
}


== flavors of css ==
* plain css
* scss
* sass
* less

== css libraries ==
* bootstrap
getbootstrap.com
* font-awesome
fontawesome.com


= Positioning =
position: static | relative | absolute | fixed;
top: measurement | percentage | auto;
right: measurement | percentage | auto;
bottom: measurement | percentage | auto;
left: measurement | percentage | auto;
z-index: integer | auto;

top/right/bottom/left : offset properties

z-index: sets the element's position in the stacking context, which defines how elements are layered "on top" of and "under" one another when they overlap. An element with a higher z-index value appears layered over one with a lower value.

position : static (default) - ignores the offset properties.
position : relative : positions the element offset from its default position while keeping the element's default position within the page flow.
position : absolute - positions elements at a specific place within the nearest ancestor that has a nonsatic position while removing the element from the page flow.
position : fixed: positions the element at a specific place within the browser viewport while removing the element from the page flow.


= CSS Box Model =
- every element is surrounded by an invisible box. There are four parts to each element box:
  - Content
  - Padding : area between content and border
  - Border : runs along the outer edges of the padding area
  - Margin : whitepsace outside borders

# Making good use of whitepace is a key part of any successful layout.

# Width and Height of block-level elements:
- Width of each element box is set to the width of the element's container, which by default is the width of the browser window.
- Height of each element box is set to a value that's tall enough to contain all the element's content.

Inline elements flow with the text, so width and height are ignored. To make them work use:
display: inline-block
To make the element a true block-level element, add: display: block

Width and height can be set using: px, em, rem, vw, wh, percentage or auto (default - browser sets automatically)

Width and height properties are applied to the content area. So actual height = height (of content) + padding + border.

Set box-sizing : border-box; to apply height to elements outer rectangle (border)

* { box-sizing : boder-box } : sets the rule for all elements.
To return to default sizing for an element use:
box-sizing: content-box

# Ideal screen reading length: 50 to 80 characters per line, ideal: 65 (go up and down based on font-size)

max-width
min-width


# padding
padding: value; // applies to all four sides
padding: value1 value2: //value1 to top and bottom, value2 to right and left
padding: value1 value2 value3; // value1 to top, value2 to right and left, value3 to bottom
padding: top right bottom left;

# border
border is optional
border: width style color;
style: dotted, dashed, solid, double, grove, ridge, insert, outset

# margin
margin: top right bottom left

# collapsing margin
when one element's bottom margin meets another element's top margin, the browser doesn't add the two values. It determines which of the two margin values is larger, and it uses that value as the vertical margin between the two elements. It throws out the smaller margin value, thus collapsing the two margins into a single value.

Increase the larger of the two margin values or use padding instead.

Left and right margin never collapse. Also, margin collapse doesn't occur for elements that are floated or positioned absolutely.


https://ishadeed.com/article/overflow-css/
