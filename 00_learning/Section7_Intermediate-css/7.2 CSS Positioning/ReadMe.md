# Notes: 

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