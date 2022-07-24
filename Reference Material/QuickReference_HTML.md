# HTML Quick Reference
## Resources
Mozilla's [HTML main reference](https://developer.mozilla.org/en-US/docs/Web/HTML)\
Mozilla's [Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)\
Mozilla's [Attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)\
Mozilla's [Event reference](https://developer.mozilla.org/en-US/docs/Web/Events)\
Mozilla's [Input Type Reference Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)\
Mozilla's [Input Atrributes Reference Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attributes)\
[Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)

## Void Elements
[TBS reference on void elements]\
Void elements are types of tags that have no children\
End tag may be assumed or included via an end slash in the first tag

### Common void tags
* br      =   produces a line break in text (carriage-return)
* hr      =   represents a thematic break between * paragraph-level elements: for example, a change of scene in a story, or a shift oftopic within a section
* img     =   embeds an image into the document.
* input   =   used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and user agent. The `<input>` element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.
* link    =   specifies relationships between the current document and an external resource. This element is most commonly used to link to CSS, but is also used to establish site icons (both "favicon" style icons and icons for the home screen and apps on mobile devices) among other things.
* meta    =   represents Metadata that cannot be represented by other HTML meta-related elements, like base, link, script, style ortitle

## Custom Tags
Tags that aren't from the standard naming. Makes them tags, elements, in the DOC with no special formatting. Rather useful. Can use "-" character even though standard tags never will.

### Pros
1. Far easier to read truly semantic HTML that visually and linguistically matches what you mean. If a tag represents a person, you write person not div that has a class of person.
2. Far simpler CSS rules that don't require as much specificity hacking and follow the true spirit of CSS's design.
3. Less convoluted structure to support layout and design.
4. More flexible design systems. If you want to rework the design you shouldn't need to rework the HTML with custom tags. With div class you almost always have to restructure the HTML for new layouts and designs.

### Cons
1. More likely to accidentally use a tag that already exists in the standard. It's a minor annoyance but you may decide to write `<marquee>` without knowing that already exists. If you do, just change the name or add a dash.
2. More difficult to target a specific element, but in reality you have this problem with div.class and need to use id markers or data-* for both anyway.
3. Not the popular way to do things, despite being easier, so you may run into weirdos who hate you for writing HTML this way.

## Attributes
Mozilla's list: https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes


### Common Attributes:
* alt         =   alt text if image can't be viewed
* disabled    =   Indicates whether the user can interact with the element.
* download    =   Indicates that the hyperlink is to be used for downloading a resource.
* hidden      =   Prevents rendering of given element, while * keeping child elements, e.g. script elements, active.
* href        =   "Hyper reference", the URL of a linked resource
* id          =   UID of item, Often used with CSS to style a specific element. The value of this attribute must be unique.
* class       =   A group concept often used with CSS to style elements with common properties
* rel         =   Specifies the relationship of the target object to the link object
* src         =   Source location, the URL of the embeddable content
* style       =   Defines CSS styles which will override styles previously set
* data        =   NOT data-*. Specifies the URL of the resource
* type        =   Defines the type of an element

### Common Form Attributes:
* accept          =   List of types the server accepts, typically a file type
* accept-charset  =   List of supported character sets (charset)
* action          =   The URI of a program that processes the information submitted via the form
* auto-complete   =   Indicates whether controls in this form can by default have their values automatically completed by the browser
* checked         =   Indicates whether the element should be checked on page load (think checkbox)
* for             =   Describes elements which belongs to this one
* form            =   Indicates the form that is the owner of the element
* tabindex        =   Global, overrides the browser's default tab order and follows the one specified instead
* type            =   Defines the type of an element

### Banished Attributes as of HTML5:
* align       =   Specifies the horizontal alignment of the element
* background  =   Use CSS "background-image" instead
* bgcolor     =   Use CSS "background-color" instead
* border      =   Use CSS "border" instead
* color       =   Use CSS "color" instead
* height      =   In some cases, use CSS "height" instead
* manifest    =   This attribute is obsolete, use `<link * rel="manifest">` instead
* width       =   In some cases use CSS "width" instead

## Common Use Cases
### Tables

    <table>
        <thead>
            <tr>
            <th>Name</th>
            <th>Color</th>
            <tr>
        </thead>
        <tbody>
            <tr><td>Apple</td><td>Red</td></tr>
            <tr><td>Mango</td><td>Orange</td></tr>
            <tr><td>Strawberry</td><td>Red</td></tr>
            <tr><td>Pitaya</td><td>Magenta</td></tr>
        </tbody>
    </table>
    
* `<table>` -- This starts a table off and contains all of the other tags.
* `<thead>` -- Starts the header row, which can contain labels for each column.
* `<tr>` -- Defines a row.
* `<td>` -- Defines one column of a row.
* `<th>` -- Defines a table column heading.
* `<tbody>` -- Configures the body of the table, and usually comes after thead.
* `<tfoot>` -- If there's a header, there's a footer.

### Forms
Basic Example:

    <form action="/login" method="POST">
        <input placeholder="Username" type="text" name="name">

        <input placeholder="Password" type="password" name="password">

        <input type="submit" value="Login">
    </form>

Most Used Types:
* button
* checkbox
* color
* email
* file
* hidden
* number
* password
* radio
* range
* reset
* search
* submit
* text

Most Uses:
* type
* value
* required
* readonly
* placeholder
* checked
* disabled
* name
* autocomplete

Avoid for CSS Instead:
* width
* size
* height

Be Careful due to Validation without Feedback
* pattern
* step
* min
* minlength
* max
* maxlength

Careful / Really Justify Use:
* autofocus
* capture
* list