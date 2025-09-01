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

* Combination of CSS selectors
    * Group
        ```css
        h1, h2 { <-- Will apply to both h1 and h2 selectors
            color: blue;
        }
        ```
    * Child
        ```css
        .selector > h2 { <-- Will applies to the direct child of .selector with h2 element
            color: red;
        }
        ```
    * Descendant
        ```css
        .a-class p { <-- Will select paragraphs inside a-class classes at any depth
            color: orange;
        }
        ```
    * Chaining
        ```css
        h1.a-class#an-id { <-- Will apply to all elements that contain all listed selectors
            color: purple;
        }
        ```
        * Elements first then ids and classes
    * Combine combiners
        ```css
        #c .a.b{ <-- Will apply to elements with a and b class decendants of c id
            color: blue;
        }
        ```

* Types of positioning
    * Static
        * html default "floating", one after the other
        ```css
        .element {position: static;}
        ```
    * Relative
        * Relative position to the static one
        ```css
        .element {position: relative;left: 50px;}
        ```
    * Absolute
        * Relative position to the nearest positioned ancestor or the web screen if not ancestor is defined
        ```css
        .element {position: absolute;left: 50px;}
        ```
    * z-index
        * What goes on top of which
            * The highest goes above 
            * Starts from 0 as default
            * If you define position as absolute, it will be in "another layer" (top)
        ```css
        .element {z-index: 2;}
        ```
    * Fixed
        * Fixed relative to browser window not considering scrolling
        ```css
        .element {position: fixed;left: 50px;}
        ```