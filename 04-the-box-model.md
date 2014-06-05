### ```display```

* determines how elements are displayed (block, inline and more)
* every element has a default display property value which can be overwritten
* common values are block, inline, inline-block, and none
* ```inline-block```: allow an element to behave as a block-level element (accepting all box model properties) but displayed inline with other elements
* ```none``` completely hides an element and render the page as if that element and nested elements doesn’t exist

### the box model concept

* every element on a page is a rectangular box and may have width, height, padding, borders, and margins
* the core of the box is defined by the width and height of an element
* the width and height of an element may be determined by the display property, by the contents of the element, or by specified width and height properties
* padding and then border expand the dimensions of the box outward from the element’s width and height.
* any margin we have specified will follow the border.
* each part of the box model corresponds to a CSS property: width, height, padding, border, and margin.
* total width = margin-right + border-right + padding-right + width + padding-left + border-left + margin-left
* total height = margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom

### width and height

* every element has default width and height (might be 0px)
* ```width``` and ```height``` may be specified - **but only for non-inline elements**
* **block width**: block-level elements have a default width of 100%, consuming the entire horizontal space available
* **inline width**: inline and inline-block elements expand and contract horizontally to accommodate their content
* **height**: all elements expand and contract vertically to accommodate their content
* inline-level elements cannot have a fixed size, (no width and height is accepted)

### margin and padding

* browsers have their own default margin and padding
* a CSS reset tones the default down to zero and build up our own margin and padding

### margin

* ```margin```: set the amount of space that surrounds an element
* the margin outside of any border and are completely transparent in color
* vertical margins, top and bottom, are not accepted by inline-level elements
* margins work like normal for block and inline-block elements

### padding

* provide spacing directly within an element
* falls inside of an element’s border
* padding works vertically on inline-level elements
* inline vertical padding may blend into the line above or below the given element
* padding works like normal for block and inline-block elements

### margin and padding declaration

* shorthand with 1 value: setting it on all four sides
* shorthand with 2 values: top and bottom first, then left and right
* shorthand with 4 values: top, right, bottom, and left, moving clockwise
* longhand: e.g margin-top, padding-left
* use longhand for 1 or 2 values
* use shorthand for 3 or more

### margin and padding colors

* they are completely transparent and don't accept any color values
* they show the background colors of relative elements (since they're transparent)
* margins - background color of the parent element
* padding - background color of the element the padding is applied to

### borders

* fall between the padding and margin, outline around the element
* has width, style, and color (shorthand order or border-width, etc)
* width, color: standard length and color values
* style: solid, double, dashed, dotted, and none
* indidual borders and properties can also be specified: border-top, border-left-width

### border-radius

* enables rounded corners
* accepts length units: radius by which the corners of an element are to be rounded
* one value shorthand: all corners
* two values shorthand: top-left/bottom-right and top-right/bottom-left
* four values shorthand: clockwise, starting from top-left
* longhand: e.g border-top-right-radius

### box-sizing

* additive by default
* CSS3 introduces ```box-sizing```
* values: content-box, padding-box, and border-box
* content-box: the size of an element begins with the width and height properties, and then any padding, border, or margin property values are added on from there
* padding-box: actual width, height: element width + padding (width 400 + 20 padding will be 400 px wide)
* actual width, height: element width + padding + border (width 400 + 20 padding + 5 px border will be 400 px wide)
* use border-box to make maths simpler (also helps when mixing percentages with px)
* drawback of using box-sizing: older browser don't support it


### vendor prefixes

* browsers gradually began to support different CSS3 properties and values by the way of vendor prefixes (e.g ```-webkit-box-sizing```)
*  as parts of the CSS3 specification are finalized and new browser versions are released, these vendor prefixes become less and less relevant
* Mozilla Firefox: -moz-
* Microsoft Internet Explorer: -ms-
* Webkit (Google Chrome and Apple Safari): -webkit-

### developer tools

- Chrome: Alt+Cmd+I

### universal selector

* universal selector: *  - catch-all to select all elements
* :before and :after pseudo-elements: dynamically generated with CSS





