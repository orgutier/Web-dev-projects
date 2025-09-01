# Notes: 

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