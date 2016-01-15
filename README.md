CSS Preprocessors overview
==========================
1. SASS
2. LESS
3. Stylus

File Extensions
---------------------
1. SASS -> .scss
2. LESS -> .less
3. Stylus -> .styl

Features
---------------------
1. Variables
    * Variable name in
        - SASS start with $
        - LESS start with @
	    - Stylus start with nothing
    * Value assignment of variable in
        - SASS is done with :
        - LESS is done with :
        - Stylus is done with = 
    * SASS
    ```scss
    $font-size: 16px;
    ```
    * LESS
    ```less
    @font-size: 16px;
    ```
    * Stylus
    ```styl
    font-size = 16px
    ```

2. Nesting
    * Nesting helps in maintaining visual hierarchy when child selectors are involved.

3. Mixins
    * Mixin is a function which takes arguments
        * Mixin is defined as 
            * SASS
            ```scss
            @mixin mixin-name ($parameter) {
	                …
            }
            ```
            * LESS
            ```less
            .mixin-name (@parameter) {
                	…
            }
            ```
            * Stylus
            ```styl
            mixin-name (parameter)
	            …
            ```

4. Extends / Inheritance
    * Share definition with selectors
    * Extends are defined as
        * SASS
        ```scss
        css-selector {
		    @extend .extend-name;
		            …
        }
        ```
        * LESS
        ```less
        css-selector {
		    &:extend(.extend-name);
		            …
        }
        ```
        * Stylus
        ```styl
        css-selector
	        @extend . extend-name
	   ```

5. Color Operations
    * Various color functions exist in all 3 css pre-processors

6. If/Else Statements
    * SASS and Stylus support if/else
    * LESS use CSS Guards
        * SASS
        ```scss
        @if condition {
	        …
        }
        @else {
	        …
        }
        ```
        * Stylus
        ```styl
        if condition
    	    …
        else
    	    …
        ```
        * LESS (http://lesscss.org/features/#css-guards-feature)
        ```less
        button when (@my-option = true) {
            color: white;
        }
        ```
        
7. Loops
    * Used for iteration
    * SASS and Stylus support loops
    * LESS use CSS Guards and mixins
        * SASS
        ```scss
        @for $i from 1px to 3px {
	        …
        }
        ```
        * Stylus
        ```styl
        for i in (1..3)
            ...
        ```
        * LESS (http://lesscss.org/features/#loops-feature)
        ```less
        .loop(@counter) when (@counter > 0) { 
            .loop((@counter - 1)); // next iteration 
            width: (10px * @counter); // code for each iteration 
        } 
        div { 
            .loop(5); // launch the loop 
        }
        ```
        
8. Math
    * Support complex math functions such as ceiling, rounding, min, max

9. Imports
    * Used to increase maintainability
        * SASS
        ```scss
        @import "filname";
        ```
        * LESS
        ```less
        @import "filename"
        ```
        * Stylus
        ```styl
        @import "filename"
        ```
