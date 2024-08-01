
</center>
<style>h1 {text-align: center;}</style>
<h1><b>Workshop Schedule</b></h1>
</center>


***


## **Day-1**
<div class="center-table" markdown>

| **Lesson**                                        | **Overview** | **Instructor** | **Time** |
|:---------------------------------------------------|:-------------|:-------------|:-------------|
|[1. Workshop Introduction](./01_intro_to_R_workshop_all.pdf){ .md-button .md-button--primary} | Welcome and housekeeping | Will | 10:00-10:30 |
|[2. Intro to R and RStudio](./02_introR-R-and-RStudio.md){ .md-button .md-button--primary} | Introduction to R and RStudio| Noor | 10:30-11:45 |
|[3. Self learning materials](#before-the-next-class){ .md-button .md-button--primary} |Overview of self-learning materials | Will | 11:45-12:00 |

</div>


### **Before the next class** 
Work through the exercises below and copy over your solutions using the submit link.

If you get stuck due to an error while running code in the lesson, [email us](hbctraining@hsph.harvard.edu)

<div class="grid cards" markdown>

- [__R Syntax and Data Structure__](../exercises/r_syntax_and_data_structures.md)
    
    ??? info "About data types and data structure"
        In order to utilize R effectively, you will need to understand what types of data you can use in R and also how you can store data in "objects" or "variables".

        This lesson will cover:

        - Assigning a value to a object

        - What types of information can you store in R

        - What are the different objects that you can use to store data in R

- [__Functions and Arguments__](../exercises/functions_and_arguments.md)

    ??? info "Functions and Arguments in R"
        Functions are the basic "commands" used in R to get something done. To use functions (denoted by function_name followed by "()"), one has to enter some information within the parenthesis and optionally some arguments to change the default behavior of a function.

        You can also create your own functions! When you want to perform a task or a series of tasks more than once, creating a custom function is the best way to go.

        In this lesson you will explore:

        - Using built-in functions

        - Creating your own custom functions

- [__Reading in and inspecting data__](../exercises/reading_in_and_data_inspection.md)

    ??? info "Read and inspect data structures in R"
        When using R, it is almost a certainty that you will have to bring data into the R environment.

        In this lesson you will learn:

        - Reading different types (formats) of data

        - Inspecting the contents and structure of the dataset once you have read it in

- [__Submit here__](https://docs.google.com/forms/d/e/1FAIpQLSfL04I7TVfs5At3n7OCLBieUsJ8nxZgjbO6mQQwCzKoBG1iLA/viewform)
    
    !!! success "Submit a day before the next class."

</div>


## **Day-2**
<div class="center-table" markdown>

| **Lesson**                                        | **Overview** | **Instructor** | **Time** |
|:---------------------------------------------------|:-------------|:-------------|:-------------|
|[4. Review self-learning](#before-the-next-class #1){ .md-button .md-button--primary } | Questions about self-learning| All | 10:00-10:50 |
|[5. In-class exercises ](./05_in_class_exercises.md){ .md-button .md-button--primary } | Use and customize function and arguments| Noor | 10:50-11:15 |
|[6. Data Wrangling](./06_data_wrangling.md){ .md-button .md-button--primary} |Subsetting Vectors and Factors | Will | 11:15-12:00 |

</div>


### **Before the next class** 
Work through the exercises below and copy over your solutions using the submit link.

If you get stuck due to an error while running code in the lesson, [email us](hbctraining@hsph.harvard.edu)

<div class="grid cards" markdown>

- [__Packages and libraries__](./homeworks/packages_and_libraries.md)
    
    ??? info "Installing and loading packages in R"
        Base R is incredibly powerful, but it cannot do everything. R has been built to encourage community involvement in expanding functionality. Thousands of supplemental add-ons, also called "packages" have been contributed by the community. Each package comprises of several functions that enable users to perform their desired analysis.

        This lesson will cover:

        - Descriptions of package repositories

        - Installing a package
        
        - Loading a package
        
        - Accessing the documention for your installed packages and getting help

- [__Data wrangling: data frames, matrics and lists__](./exercise/07_introR-data-wrangling2.md)

    ??? info "Subset, merge, and create new datasets"
        In class we covered data wrangling (extracting/subsetting) information from single-dimensional objects (vectors, factors). The next step is to learn how to wrangle data in two-dimensional objects.

        This lesson will cover:
        
        - Examining and extracting values from two-dimensional data structures using indices, row names, or column names
        
        - Retreiving information from lists

- [__The %in% operator__](./exercise/08_identifying-matching-elements.md)

    ??? info "`%in%` operator, `any` and `all` functions"
        Very often you will have to compare two vectors to figure out if, and which, values are common between them. The %in% operator can be used for this purpose.

        This lesson will cover:
        
        - Implementing the %in% operator to evaluate two vectors
        
        - Distinguishing %in% from == and other logical operators
        
        - Using any() and all() functions

- [__Reordering and matching__](./exercise/09_reordering-to-match-datasets.md)

    ??? info "Ordering of vectors and data frames"
        Sometimes you will want to rearrange values within a vector (row names or column names). The match() function can be very powerful for this task.

        This lesson will cover:

        - Maunually rearranging values within a vector

        - Implementing the match() function to automatically rearrange the values within a vector

- [__Data frame for plotting__](./exercise/10_setting_up_to_plot.md)

    ??? info "Learn about `map()` function for iterative tasks"
        We will be starting with visualization in the next class. To set up for this, you need to create a new metadata data frame with information from the counts data frame. You will need to use a function over every column within the counts data frame iteratively. You could do that manually, but it is error-prone; the map() family of functions makes this more efficient.

        This lesson will cover:
        
        - Utilizing map_dbl() to take the average of every column in a data frame
        
        - Briefly discuss other functions within the map() family of functions
        
        - Create a new data frame for plotting

- [__Submit here__](https://docs.google.com/forms/d/e/1FAIpQLSegEjBKDkK4TB7uhNfcBl6633hasPrGsYDnFuH683blpZNtfg/viewform)
    
    !!! success "Submit a day before the next class."

</div>




* * *

## **Day-3**
<div class="center-table" markdown>

| **Lesson**                                        | **Overview** | **Instructor** | **Time** |
|:---------------------------------------------------|:-------------|:-------------|:-------------|
|[7. Review self-learning](#before-the-next-class #2){ .md-button .md-button--primary } | Questions about self-learning| All | 10:00-10:35 |
|[8. In-class exercises ](./08_in_class_exercises.md){ .md-button .md-button--primary } | Customizing functions and arguments| Will | 10:50-11:15 |
|[9. Plotting with ggplot2](./09_plotting_with_ggplot2.md){ .md-button .md-button--primary} | ggplot2 for data visualization | Noor | 11:15-12:00 |

</div>


### **Before the next class** 
Work through the exercises below and copy over your solutions using the submit link.

If you get stuck due to an error while running code in the lesson, [email us](hbctraining@hsph.harvard.edu)

<div class="grid cards" markdown>

- [__Custom functions for plots__](./exercise/11b_Custom_Functions_ggplot2.md)
    
    ??? info "Consistent formats for plotting"
        When creating your plots in ggplot2 you may want to have consistent formatting (using theme() functions) across your plots, e.g. if you are generating plots for a manuscript.

        This lesson will cover:
        
        - Developing a custom function for creating consistently formatted plots

- [__Boxplot with ggplot2__](./exercise/12_boxplot_exercise.md)

    ??? info "Customizing barplots with ggplot2"
        Previously, you created a scatterplot using ggplot2. However, ggplot2 can be used to create a very wide variety of plots. One of the other frequently used plots you can create with ggplot2 is a barplot.

        This lesson will cover:
        
        - Creating and customizing a barplot using ggplot2  

- [__Exporting files and plots__](./exercise/13_exporting_data_and_plots.md)

    ??? info "Writing files and plots in different formats"
        Now that you have completed some analysis in R, you will need to eventually export that work out of R/RStudio. R provides lots of flexibility in what and how you export your data and plots.

        This lesson will cover:
        
        - Exporting your figures from R using a variety of file formats
        
        - Writing your data from R to a file

- [__Finding help__](./exercise/14_finding_help.md)

    ??? info "How to best look for help"
        Hopefully, this course has given you the basic tools you need to be successful when using R. However, it would be impossible to cover every aspect of R and you will need to be able to troubleshoot future issues as they arise.

        This lesson will cover:
        
        - Suggestions for how to best ask for help
        
        - Where to look for help

- [__Tidyverse__](./exercise/15_tidyverse.md)

    ??? info "Data wrangling within Tidyverse"
        The Tidyverse suite of integrated packages are designed to work together to make common data science operations more user friendly. Tidyverse is becoming increasingly prevalent and it is necessary that R users are conversant in the basics of Tidyverse. We have already used two Tidyverse packages in this workshop (ggplot2 and purrr) and in this lesson we will learn some key features from a few additional packages that make up Tidyverse.

        This lesson will cover:
    
        - Usage of pipes for connecting together multiple commands
    
        - Tibbles for two-dimensional data storage
    
        - Data wrangling within Tidyverse

- [__Submit here__](https://docs.google.com/forms/d/e/1FAIpQLSdelYtXxCGQZOWd2T28REjU5NC_NS4n-HZte8OEgFXS6Q5wcA/viewform)
    
    !!! success "Submit a day before the next class."

</div>


* * *

## **Day-4**
<div class="center-table" markdown>

| **Lesson**                                        | **Overview** | **Instructor** | **Time** |
|:---------------------------------------------------|:-------------|:-------------|:-------------|
|[10. Review self-learning](#before-the-next-class #3){ .md-button .md-button--primary } | Questions about self-learning| All | 10:00-10:35 |
|[11. In-class exercises ](./lessons/11_in_class_exercises.md){ .md-button .md-button--primary } | In class exercises| Will | 10:50-11:15 |
|[12. Discussion](./lessons/discussion.md){ .md-button .md-button--primary} | Q&A | Noor | 11:15 - 11:45 |
|[13. Wrap Up](./lessons/R_workshop_wrapup_all.pdf){ .md-button .md-button--primary} | Wrap up and checking out| Noor | 11:45 - 12:00 |

</div>


### **Additional exercises and answer keys**

<div class="grid cards" markdown>

- [__Final Exercises__](./exercise/Intro_to_R_hw.md)

- [__Answer Keys__](./activities/day1_hw_answer-key.R)


</div>


### **Additional resources**


<div class="grid cards" markdown>

- __Building on the basic R knowledge__
    - [DGE workshop](https://hbctraining.github.io/DGE_workshop_salmon/)
    - [Single-cell RNA-seq workshop](https://hbctraining.github.io/scRNA-seq/)
    - [RMarkdown](https://hbctraining.github.io/Training-modules/Rmarkdown/)
    - [Functional analysis](https://hbctraining.github.io/Training-modules/DGE-functional-analysis/)
    - [More ggplot2](https://hbctraining.github.io/publication_perfect/)
    - [ggplot2 cookbook](http://www.cookbook-r.com/Graphs/)
    - [Running R and Rstudio on O2](https://harvardmed.atlassian.net/wiki/spaces/O2/pages/1623425967/RStudio+on+O2)

- __Resources__
    - [Online learning resources](https://hbctraining.github.io/bioinformatics_online/lists/online_trainings.html)
    - [All hbctraining materials](https://hbctraining.github.io/main)
  
    __Cheatsheets__

    - [base R cheatsheet](https://github.com/hbctraining/Intro-to-R-flipped/blob/master/cheatsheets/base-r.pdf)
    - [RStudio cheatsheet](https://github.com/hbctraining/Intro-to-R-flipped/blob/master/cheatsheets/rstudio-ide.pdf)
    - [ggplot2 cheatsheet](https://github.com/hbctraining/Intro-to-R-flipped/blob/master/cheatsheets/data-visualization-2.1.pdf)

</div>

* * * 


!!!quote "Citation"    
    * *To cite material from this course in your publications, please use:*

        **Meeta Mistry, Mary Piper, Jihe Liu, & Radhika Khetani. (2021, May 5). hbctraining/Intro-to-R-flipped: R workshop first release. Zenodo. https://doi.org/10.5281/zenodo.4739342**

    * A lot of time and effort went into the preparation of these materials. Citations help us understand the needs of the community, gain recognition for our work, and attract further funding to support our teaching activities. Thank you for citing this material if it helped you in your data analysis.

!!!quote "Attribution notice"
    * *These materials have been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*

    * *Some materials used in these lessons were derived from work that is Copyright © [Data Carpentry](http://datacarpentry.org/). All Data Carpentry instructional material is made available under the [Creative Commons Attribution license (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)*
