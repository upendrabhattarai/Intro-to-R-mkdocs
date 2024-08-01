# Day 2: In class activities

## Making Custom Functions

Create a function `temp_conv()`, which converts the temperature in Fahrenheit (input) to the temperature in Kelvin (output). 

??? success "Hints"  
    <ul><li>We could perform a two-step calculation: first convert from Fahrenheit to Celsius, and then convert from Celsius to Kelvin.</li><li>The formula for these two calculations are as follows: temp_c = (temp_f - 32) * 5 / 9; temp_k = temp_c + 273.15.</li><li> **To test your function:** </li><li>if your input is 70, the result of `temp_conv(70)` should be 294.2611.</li></ul>



## Nesting Functions

Now we want to round the temperature in Kelvin (output of `temp_conv()`) to a single decimal place. 

??? success "More Hints"
    Use the `round()` function with the newly-created  `temp_conv()` function to achieve this in one line of code. If your input is 70, the output should now be 294.3.


??? warning "Solution"
    **Part 1**
        ```r
            temp_conv <- function(temp_f) {
                temp_c = (temp_f - 32) * 5 / 9
                temp_k = temp_c + 273.15
            return (temp_k)
             }
        ```
    **Part 2**
        ```r
            round(temp_conv(70), digits = 1)

        ```


* * *


!!! quote "Attribution notice"
    * *This lesson has been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*

    * *The materials used in this lesson are adapted from work that is Copyright © Data Carpentry (http://datacarpentry.org/).All Data Carpentry instructional material is made available under the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0).*
