## Lists

HTML has 3 types of lists: unordered, ordered, and description lists

### Unordered lists

* ```<ul>``` unordered list block-level element
* ```<li>``` list items
* by default most browsers add a solid dot list item marker and margin and padding

### Ordered list

* ```<ol>``` ordered list element
* works pretty much similarly to ```<ul>``` but order matters
* by default most browser use numbers as list item markers
* ```start``` attribute on ```<ol>``` element tells where to start counting from (e.g paginated list)
* ```start``` attribute only accepts integers
* ```reversed``` boolean attribute (no value required, present=true) tells if the numbers should be in reverse order
* ```value``` attribute on an individual ```<li>``` within an ```<ol>``` changes its value within the list
* any item appearing after the one with the value is calculated accordingly

### Description lists

* description lists are used to outline multiple terms and their descriptions (e.g. glossary)
* description list block-level element, ```<dl>```
* an item consists of one or more description terms ```<dt>``` followed by one or more descriptions ```<dd>```
* in most browsers by default, the <dl> element will include vertical margins and the <dd> element includes a left margin

### Nesting lists

* always start the new list within an li and should be fine

### List style type

* the ```list-style-type``` property sets the content of a list item marker
* can change both unordedered and ordered list to anything you like
* common values: none, disc, circle, square, decimal, decimal-leading-zero, lower-roman, upper-roman, lower-greek, lower-alpha / lower-latin, upper-alpha / upper-latin

### Image as a list item marker

* set list-style-type to none
* add small backround image (0 50% no-repeat)
* add padding-left to push content right

### list-style-position

* list-style-position property can have values: inside, outside, inherit
* default is outside - no content is wrapped around the marked


### list-style shorthand

* list-style-type followed by list-style-position - space separated

### Horizontally displaying a list

* make ```<li>```s inline-block
* marker is automatically set to none
* single spaces can be removed by adding comment between lis
* inline-block is better than inline as allows specifying margins, paddings

### Floating list

* changing to inline-block or inline removes the marker
* floating keeps to marker
* need to add margin or padding to prevent markers overlapping content
* always clear or contain floats
