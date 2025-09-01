# Notes: 

# CSS Float
* Wrap text around another element
* Float property
    * Html example
        ```html
        <img ...>
        <p>Text </p>
        ```
    * Css example
        ```css
        img {
            float: right; <-- or left
        }
        ```
* To remove floating elements
    ```css
    footer {
        clear: left; <-- Will remove floating elements in its space
        clear: both; <-- Will remove both left and right elements 
    }
    ```
* Float is not used to layout websites in modern websites
    * Better use
        * Bootstrap
        * Grid