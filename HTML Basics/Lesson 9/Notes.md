# Lesson 9: Custom Tags
Just tags that aren't from the standard naming. Makes them tags, elements, in the DOC with no special formatting. Rather useful. Can use "-" character even though standard tags never will.

## Pros
1. Far easier to read truly semantic HTML that visually and linguistically matches what you mean. If a tag represents a person, you write person not div that has a class of person.
2. Far simpler CSS rules that don't require as much specificity hacking and follow the true spirit of CSS's design.
3. Less convoluted structure to support layout and design.
4. More flexible design systems. If you want to rework the design you shouldn't need to rework the HTML with custom tags. With div class you almost always have to restructure the HTML for new layouts and designs.

## Cons
1. More likely to accidentally use a tag that already exists in the standard. It's a minor annoyance but you may decide to write `<marquee>` without knowing that already exists. If you do, just change the name or add a dash.
2. More difficult to target a specific element, but in reality you have this problem with div.class and need to use id markers or data-* for both anyway.
3. Not the popular way to do things, despite being easier, so you may run into weirdos who hate you for writing HTML this way.

## Using div for Everything Instead
This appears to be a common use. Does inherit formatting and layout. Its formatting uses autofill so it is a dynamic formatted element. Be cautious.