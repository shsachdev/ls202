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

By default, a `block` element occupies all horizontal space available within its container, with
nothing to the left or right of the `block`.

Most elements are block elements by default. Here are some of the most common:

- section, article, aside, header, footer
- p
- h1 through h6
- blockquote
- ul, ol, dl
- figure and figcaption
- form and fieldset

# Inline Elements

Inline elements provide a small bit of semantic meaning to content; browsers use this to alter the way they display small sections of text, which, in turn, helps the reader spot specific items with ease. For instance, if you want to use bolded text for definitions, you can use the b element to render definitions in boldface. The reader can see at a glance where the definitions are in the document. By default, b is an inline element.

# Inline-Block Elements

inline-block elements are a mixture of both previous types. They act like block elements, except for one significant detail: inline-block elements do not take up an entire row when the width property is less than the available width. Instead, they flow in the same way that text and inline elements flow from one line to the next (see Figures 1 and 2 on the previous page), which lets you place

inline-block elements side-by-side with other inline or inline-block elements.
inline-block elements also differ from inline in that inline-block elements observe the width and height properties. The padding, borders, and margin all work like they do with block elements.
