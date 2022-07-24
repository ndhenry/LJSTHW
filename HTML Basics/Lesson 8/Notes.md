# Lesson 8: Forms

## Standard Login
    <form>
        <input type="text" name="name">
        <input type="password" name="password">
        <input type="submit" value="Login">
    </form>

## Labels
Two ways of labeling, with the first being the most common.

    <form>
        <label for="name">Username:</label>
        <input id="name" type="text" name="name">

        <label>Password:
            <input type="password" name="password">
        </label>

        <input type="submit" value="Login">
    </form>

## Placeholders
"It's debatable if placeholder is an "alternative" to labels, or if you should use both. Minimalists prefer only placeholders, and maximalists prefer full labels, but put the formatting for a field in the placeholder. For example, you might label a field as "SSN" and then set the placeholder="###-##-###"."

    <form>
        <input placeholder="Username" type="text" name="name">

        <input placeholder="Password" type="password" name="password">

        <input type="submit" value="Login">
    </form>

## Inputs
* [Input Type Reference Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
* [Input Atrributes Reference Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attributes)

### Input Types
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

### Input Attributes
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

## Actions / Methods

    <form action="/login" method="POST">
        <input placeholder="Username" type="text" name="name">

        <input placeholder="Password" type="password" name="password">

        <input type="submit" value="Login">
    </form>

 Key is the action and method. Action telling where to complete the submit (server location: /login). Method telling how to do it (HTTP POST method versus say GET).