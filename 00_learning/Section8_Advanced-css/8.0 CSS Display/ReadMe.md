# Notes: 

# CSS Display

* Span element
    ```html
    <p>Hello <span> World </span>!</p>
    ```
    * Span is set to display type inline
    * Inline display
        * Inline types will fill the space to the right
        * Heigh is not settable, only width 
        ```css
        h2{
            display: inline;
        }
        ```
    * Block type will display the full sized block
        ```css
        h2{
            display: block;
        }
        ```
    * inline-block
        * You can set both height and width
        ```css
        h2{
            display: inline-block;
        }
        ```
    * None will disappear elements
        ```css
        h2{
            display: none;
        }
        ```