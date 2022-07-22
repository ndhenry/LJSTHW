# Lesson 5 Notes: Important Attributes
An introduction to the attributes that link HTML and CSS.
## CCS Selectors
Tags, h1, h3, p, can be set with a CSS rule applied to them allowing for control of that whole tag set. The different types of tags are used to more precisely control the flow and revision of the visual style.

### Class
Class is a marker for grouping HTML tags for applied CSS rules.

Uses the `.` for deliniation.

#### Applying a class to an individual tag:
`<button class="sleepy">Rest</button>`

#### Defining rules for a class:
    .sleepy {
        color: gray;
    }

#### Sleepy filtered to button HTML elements:
    button.sleepy {
        color: gray;
    }

### ID
Just like class but has higher priority and thus is meant for more granular use. This is typically for a single item.

Uses `#` for deliniation.

`<button id="thisSleepyGuy">Rest</button>`

    #thisSleepyGuy{
        color: gray;
    }

### Data-*
Used for selecting and setting for code driving. Think tests causing simulated clicks, change modes by scripts, etc.

`<button data-restid="thisSleepyGuy">Rest</button>`

    [data-rest="dark"]{
        --color: #bbb;
        --color-accent: #fff;
        --color-bg: #333;
    }

### Style
Highest priority and thus actually best saved for debugging.
`<button style="color: green">Rest</button>`
