HTML gives content structure and meaning by defining that content as, for example,
headings, paragraphs, or images. CSS is a presentation language created to style the
appearance of content - using, for example, fonts or colors.

The two languages - HTML and CSS - are independent of one another and should remain
that way. CSS should not be written inside of an HTML document and vice versa.

As a rule, HTML will always represent content, and CSS will always represent the appearance
of that content.

The 3 common HTML terms you should begin with are *elements*, *tags*, and *attributes*.

There are also a few common CSS terms to familiarize yourself with. These terms include
selectors, properties, and values.

HTML provides three ways to identify certain elements: classes, ids, and names.
Any element can use a class or id attribute, and a variety of elements can use the name attribute.

The `Class` attribute identifies a set of page elements that you wish to style consistently.
For instance, if you want to display a list of students, but highlight students who serve as
Teaching Assistants, you can apply a class of `teaching-assistant` to each TA's data:

```html
<table>
  <tbody>
    <tr class="teaching-assistant">
      <td>Elizabeth</td>
      <td>JS230</td>
    </tr>
  </tbody>
</table>
```

- Use the `class` attribute to assign a class or classes to an element.
- Any number of elements may belong to the same class.
- Any element can belong to one or more classes. List all the names separated
by spaces in the `class` attribute, e.g, `class="executive management full-time"`
- Prefer semantic class names; they should provide meaning. For instance, use `teaching-assistant`
rather than `yellow-background`.
- Use CSS class selectors (`.classname`) to select elements by class, e.g., `.teaching-assistant`.
- Class selectors have lower CSS specificity than ID selectors (an ID selector overrides a class selector),
but higher than tag name selectors.

# IDs

The `ID` attribute applies a unique identification string to a single element, such as a headline; no other
`id` attributes on the page should have the same ID.

```html
<h1>This is a plain h1 heading</h1>
<h1 id="headline">This is my headline</h1>
```
You can now give it some styling that is unique to it:

```css
#headline {
  color: red;
  font-size: 48px;
}
```
