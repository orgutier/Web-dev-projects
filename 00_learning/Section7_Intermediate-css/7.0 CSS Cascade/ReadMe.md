# Notes: 

* Cascading Style Sheets
* What happens when you target an element by more than one style?
    * Cascade to know what is applied and what doesn't
    * Order of importance
    * Levels of styles to be applied
        1. External -> Applied in external css
        2. Internal -> Applied in style element
        3. In line -> Applied in the element
    * Four raw categories to determine importance
        1. Position
            * The lowest one (last) is applied
                ```css
                li {
                    color: red;
                    color: blue; <-- This is applied
                }
                ```
        2. Specificity ordered by most important last
            * The lowest one (last) is applied
                ```css
                li {color: blue;} <-- By element
                .first-class {color: red;} <-- By class
                .first-li[draggable] {color: purple;} <-- By attribute
                #first-id {color:orange;} <-- By id
                ```
        3. Type
            1. The lowest one (last) is applied
                ```html
                <link rel="stylesheet" href="./style.css" /> <-- External
                <style> </style> <-- Internal
                <h1 style=" "> Hello </h1> <-- Inline
                ```
        4. Importance
            * The lowest one (last) is applied
                ```css
                li {
                    color: red;
                    color: green !important; <-- This is applied
                }
                ```
    * Extra tip, you can add multiple classes to the same element with a space
        ```html
        <h1 class="a-class b-class"> Hello </h1> <-- class a-class and b-class