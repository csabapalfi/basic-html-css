## Positioning with Floats

* the float property allows us to take an element, remove it from the normal flow of a page
* and position it to the left or right of its parent element
* all other elements on the page will then flow around the floated element
* used on multiple elements: creating a layout by floating elements directly next to or opposite each other
* multi-column layouts can be created

### floating in practice

* common float values are: ```left``` and ```right```
* floated elements will float all the way to the edge of its parent element
* no parent: floated element floats to the edge of the page
* floated element width defaults to the width of the content within it
* use the ```width``` property to specify width
* use ```margin``` to prevent elements touching each other
* floated inline elements change their display value to block and accept width, height

### clearing & containing floats

* floats have pitfalls, originally for wrapping content around images and not layout
* styles next to a parent of a floated element might break
* margin and padding can blend into a floated element
* unwanted content can wrap around floated content

### clearing floats
* to prevent unwanted content from wrapping around floated elements, we need to clear, or contain, those floats
* clearing floats returns the page to its normal flow
* ```clear``` property, values: ```left```, ```right```, ```both```
*  left clear left floats, right clear right floats, both clears both sides
* clear property applied on an element after floated elements to return the page to it's normal flow

### containing floats (clearfix)

* effects similar to clearing (return to normal flow) but also makes sure styles are rendered correctly
* to contain floats, the floated elements must have a parent (container)
* the flow of the document will remain unaffected outside of the container
* containing everything within element with class group:

```css
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
```
*  :before and :after pseudo-elements
* dynamically generated elements above and below the element with the class of group
* with no content but styles to clear floats
* also known as clearfix but the class group better represents the content

### keep track of float and always clear/contain them

### positioning with inline-block

* ```display: inline-block```: placing elements next to one another within a line
* but also accepts width, height, padding, border, margin ... (as opposed to inline)
* taking full advantage of the box model without having to worry about clearing any floats


### inline block vs spaces

* inline-block elements are displayed on the same line, they also include a single space between them
* low tech, simple solution: no space between start and end tags
* another low tech solution: start HTML comment after end tag, close comment before start tag

### Creating a reusable layout

* best to write modular styles that may be reused elsewhere
* floats vs inline-block is open to debate
* one approach:  inline-block elements to create the grid—or layout—of
* and float to wrap around content (as originally intended)
* new CSS specs: watch out for ```flex-``` and ```grid-``` based properties—that

### Uniquely Positioning Elements

* precisely positioning elements: floats or inline-block might not do the job
* typically, most positioning can be handled without the use of the position property and box offset properties, but in certain cases they can be extremely helpful
* can use the ```position``` property with box offset properties
* position: how an element is positioned on a page, if it appears in the normal flow of the document
* box offset properties moving elements to ```top right bottom``` or  ```left```
* default position value is ```static```
* ```static``` means the element appears in the normal flow and doesn't accept box offset properties
* other position values are: relative and absolute

### ```position: relative```

* element appears within the normal flow a page
* leaving space for an element as intended
* also allows an element’s display position to be modified with the box offset properties
* box offset properties identify where an element will be moved from given its original position (left: 20px - pushes element to the right by 20px)

### ```position: absolute```

* element does not appear within the normal flow a page
* original space and position of the element is not preserved
* elements are moved in relation to their closest relatively positioned parent element
* should a relatively positioned parent element not exist, the element will be positioned in relation to the <body> element



