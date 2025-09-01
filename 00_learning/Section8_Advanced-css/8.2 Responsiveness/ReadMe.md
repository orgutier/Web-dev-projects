# Notes: 

Make websites look good in any screen size

* Website layout
    * Media queries
        ```css
        @media (max-width: 600px) { <-- min-width
            /*CSS for screens below or equal to 600px wide*/
        }
        @media (min-width: 600px) and (max-width:900px) {
            /*Styles for screens less than 600px and greater than 900px*/
        }
        @media screen (orientation: landscape) {
            /*Style if screen is in landscape position*/
        }
        ```
        * Change some CSS based on media size query
        * Useful to fit in phone or computer sizes
    * CSS grid
        * More flexible, uses divs to separate blocs of content in the website
        * Good for 2D layouts
        ```html
        <div class="grid-container">
            <div class="first card"></div>
            <div class="card"></div>
            <div class="card"></div>
            <div class="card"></div>
            <div class="card"></div>
        </div>
        ```
        ```css
        .grid-container {
            display: grid; <-- Display type
            grid-template-columns: 1fr 1fr; <-- 2 separate equally sized fractions
            grid-template-rows: 100px 200px 200px; <-- 3 rows of different sizes
            gap: 30px; <-- Separation within grids e.g. margin
        }

        .first{
            grid-column: span 2; <-- To take 2 spaces instead of one
        }

        .card {
            background-color: blue;
        }
        ```
    * CSS flexbox
        * Good for 1D layouts vertical or horizontal
        ```html
        <div class="flex-container">
            <div class="first card"></div>
            <div class="second card"></div>
            <div class="card"></div>
            <div class="card"></div>
        </div>
        ```
        ```css
        .flex-container{
            display: flex;
        }
        .card {
            background-color: blue;
            border: 30px solid white;
            height: 100px;
            flex: 1; <-- Equal distribution to all, proportional to total width
        }
        .first{
            flex: 2; <-- Twice as big
        }
        .second{
            flex: 0.5 <-- Half as big
        }
        ```
    * External framework e.g. Bootstraps
        * External predefined layout
            * Divides website width in 12 rows, it has predefined class names to give website format
            * This code will create a row array with sized cards as the class name
            ```html
            <div class="container">
                <div class="row">
                    <div class="card col-6">
                        Card
                    </div>
                    <div class="card col-2">
                        Card
                    </div>
                    <div class="card col-4">
                        Card
                    </div>
            </div>
            ```