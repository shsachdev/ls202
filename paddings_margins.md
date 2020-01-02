#What is the difference between Padding and Margins?

Both padding and margins surround elements with whitespace. Padding lies inside the border,
while margins lie outside it.

Margins are typically transparent, while the padding is opaque.

Put another way, padding is part of the visible and clickable bounds of an element,
while a margin is spacing between adjacent elements. It's easy to see this with clickable
elements. If you click on the content area or anywhere in the padding or border, the
browser will process the click. If you click on the margin, nothing happens.

As we learned earlier, the browser doesn't use the top and bottom margins and padding
for inline elements for spacing. New developers often forget this, which leads to
headaches as they try to figure out why the margins or padding aren't working the way
they expect. No matter how big the top and bottom margins are on an inline element, they
do not affect the placement of the element's content nor the content surrounding it.
See the example under Borders, Padding, and Inline Elements in The
Visual Formatting Model assignment.

Margin collapse occurs with top and bottom margins, not with left and right margins. Padding does not collapse.
