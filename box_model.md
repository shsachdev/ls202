Word processing software ordinarily outputs one character at a time, moving from left to right.
As each line fills with words, the word processor automatically wraps down to the next line and
starts adding characters to the beginning of a new line.

Your browser works in much the same way to render HTML pages: it displays "words" one at a time
horizontally until it encounters a "word" that doesn't fit. At this point, the browser starts a new
**line** - one or more "words" at the same horizontal level in the current container element.

We put "words" in quotes since a browser must deal with more than words: web pages have images,
media players, containers (which we'll discuss later), and other kinds of objects. For simplicity and clarity,
we'll call these objects **elements** instead of words.

As the browser renders a document, it processes one element at a time. The browser determines how much horizontal
and vertical space -- a rectangle or box -- it needs to draw the item. It uses the browser defaults and your CSS
to calculate the required dimensions. If there's enough horizontal space remaining on the current line, the browser
places the element there; otherwise, it starts a new line. Each line uses enough vertical space to contain all its
rectangles. This process repeats for every box on the page.

The most important takeaways from this description of the rendering process are:

- Every element requires a box-shaped segment of the page.
- Every character of text content also needs a boxed portion of the page.
- The browser calculates the dimensions of that box by using the browser defaults and CSS.

We use the term **CSS box model** or **box model** to describe how the browser calculates
the box size for any given element.

#Widths and Heights

See LS Box Model lecture 1.

#Box Properties

Every element box has the following properties (the browser may ignore some of them):

- The **width** and **height** define how much horizontal and vertical space it needs
for the *content area* of the box, which may or may not include the padding and borders.
In most cases, the browser can determine the width and height automatically.

- The **padding** is an area that surrounds the content area of the box and separates the content
from its border. It is typically opaque and hides anything that it overlays.

- The **border** is a boundary that surrounds the padding.

- The **margin** is a transparent area that lies outside the border and supplies separation
between the elements.

- The **display** property determines how the browser lays out an element relative to its neighbors.
