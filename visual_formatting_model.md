# The Visual Formatting Model

When we discussed how the browser lays out elements, our stated assumption was that
all boxes have a `display` property `inline-block`.

Whilst `display` has more than two dozen values, most CSS uses the values `block`,
`inline`, and `inline-block`.

# Block Elements

Block elements appear on almost all web pages: headings, paragraphs, sections, tables, forms, lists,
and more are block elements.

Most `block` elements group one or more elements - some of which may themselves be `block`s - into
areas of the page. For instance, `header` elements group together elements into a page header. We
often call such `block` elements **containers**. The master container (the outermost) is the `body`;
every other element belongs to a container.
