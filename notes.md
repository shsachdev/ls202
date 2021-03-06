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

- Use the `ID` attribute to assign an ID to an element.
- Each ID on a page must be unique.
- Each element can have one ID or none.
- Use semantic ID names; they should provide meaning. For instance, use an ID name
of `headline` rather than `big-font`.
- Use CSS ID selectors (`#idname`) to select elements by ID.
- ID selectors have higher CSS specificity than class selectors (an ID selector can override a class selector.)

# Names

The `name` attribute ties form elements to data on the server - it typically does not play a role in styling.

When you submit a form, the browser sends the form data to the server using name/value pairs in which each name
comes from the associated `name` attribute. For instance:

```html
<form method="get" action="#">
  <label for="first-name-field">First name:</label>
  <input type="text" name="first-name" id="first-name-field" />

  <label for="last-name-field">Last name:</label>
  <input type="text" name="last-name" id="last-name-field" />

  <input type="submit" value="search" />
</form>
```

When you submit this form, the browser constructs a query string that looks like this:

```
first-name=Joe&last-name=Jones
```
Note that the browser does not send the `id` attribute value to the server.

- Use the `name` attribute to assign a name to a form data element that the server can use to obtain the value.
- Not all tags accept the name `name` attribute; it applies to input controls in forms. Some other elements have a
name attribute, too, but with a different meaning.
- Always use a `name` attribute on form elements that accept it.
- Each name in a form should be unique to that form except for radio buttons and checkboxes that belong to a single group.
- Use descriptive `name` values, not semantic. For instance, use `name="last-name"` instead of `name="input-field"`.
- Avoid trying to select elements in CSS by using the `name` attribute.


# Some notes on CSS

There are three main ways to use CSS in a web page: inline, internal, and external.

- **Inline** CSS uses `style` attribute on individual HTML tags.
- **Internal** CSS uses the `style` element to store all of the CSS in one place in the file.
- **External** CSS stores the CSS in a file that is separate from the HTML file.
