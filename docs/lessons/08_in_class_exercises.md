# Day 3: In class activities

## Reading in and inspecting data
- Download the data and place the file into the `data` directory.

|Data | Download link |
|:------|:--------|
|Animal data |[Right click & Save link as...](https://raw.githubusercontent.com/hbctraining/Intro-to-R-flipped/master/data/animals.csv){ .md-button}|

!!!question "Exercise"
    - Read the `.csv` file into your environment and assign it to a variable called `animals`. **Be sure to check that your row names are the different animals.**
    - Check to make sure that `animals` is a dataframe.
    - How many rows are in the `animals` dataframe? How many columns?


## Data wrangling

!!!question "Exercise"
    1. Extract the `speed` value of 40 km/h from the `animals` dataframe.
    2. Return the rows with animals that are the `color` Tan.
    3. Return the rows with animals that have `speed` greater than 50 km/h and output only the `color` column. Keep the output as a data frame.  
    4. Change the color of "Grey" to "Gray". 
    5. Create a list called `animals_list` in which the first element contains the speed column of the `animals` dataframe and the second element contains the color column of the `animals` dataframe. 
    6. Give each element of your list the appropriate name (i.e speed and color).

## The `%in%` operator, reordering and matching

In your environment you should have a dataframe called `proj_summary` which contains quality metric information for an RNA-seq dataset. We have obtained batch information for the control samples in this dataset. 

!!!question "Exercise"
    1. **Copy and paste the code below to create a dataframe of control samples with the associated batch information**
        ```r
        ctrl_samples <- data.frame(row.names = c("sample3", "sample10", "sample8", "sample4", "sample15"), date = c("01/13/2018", "03/15/2018", "01/13/2018", "09/20/2018","03/15/2018"))
        ```
    2. How many of the `ctrl_samples` are also in the `proj_summary` dataframe? Use the `%in%` operator to compare sample names. <br>

    3. Keep only the rows in `proj_summary` which correspond to those in `ctrl_samples`. Do this with the %in% operator. Save it to a variable called `proj_summary_ctrl`.<br>

    4. We would like to add in the batch information for the samples in `proj_summary_ctrl`. Find the rows that match in `ctrl_samples`.<br>

    5. Use `cbind()` to add a column called `batch` to the `proj_summary_ctrl` dataframe. Assign this new dataframe back to `proj_summary_ctrl`.


    ???warning "Solution"

        ```r
        ## Reading in and inspecting data

        # 2. Read the csv file into your environment and assign it to a variable called `animals`. Be sure to check that your row names are the different animals.
        animals <- read.csv("data/animals.csv")

        # 3. Check to make sure that `animals` is a dataframe.
        class(animals)

        # 4. How many rows are in the `animals` dataframe? How many columns?
        nrow(animals)
        ncol(animals)

        ## Data wrangling

        # 1. Extract the `speed` value of 40 km/h from the `animals` dataframe.
        animals[1,1]
        animals[which(animals$speed == 40), 1]
        animals[which(animals$speed == 40), "speed"]
        animals$speed[which(animals$speed == 40)]

        # 2. Return the rows with animals that are the `color` Tan.
        animals[c(2,5),]
        animals[which(animals$color == "Tan"),]

        # 3. Return the rows with animals that have `speed` greater than 50 km/h and output only the `color` column. Keep the output as a data frame.  
        animals[which(animals$speed > 50), "color", drop =F]

        # 4. Change the color of "Grey" to "Gray". 
        animals$color[which(animals$color == "Grey")] <- "Gray"
        animals[which(animals$color == "Grey"), "color"] <- "Gray"

        # 5. Create a list called `animals_list` in which the first element contains the speed column of the `animals` dataframe and the second element contains the color column of the `animals` dataframe. 
        animals_list <- list(animals$speed, animals$color)

        # 6. Give each element of your list the appropriate name (i.e speed and color).
        names(animals_list) <- colnames(animals)

        ## The %in% operator, reordering and matching

        # 2. How many of the control samples are also in the `proj_summary` dataframe? Use the %in% operator to check.
        length(which(rownames(ctrl_samples) %in% rownames(proj_summary)))

        # 3. Keep only the rows in `proj_summary` which correspond to control samples. Do this with the %in% operator. Save it to a variable called `proj_summary_ctrl`.
        proj_summary_ctrl <- proj_summary[which(rownames(proj_summary) %in% rownames(ctrl_samples)),]


        # 4. We would like to add in the batch information for the samples in `proj_summary_ctrl`. Find the rows that match in `ctrl_samples`.
        m <- match(rownames(proj_summary_ctrl), rownames(ctrl_samples))

        # 5. Use `cbind()` to add a column called `batch` to the `proj_summary_ctrl` dataframe. Assign this new dataframe back to `proj_summary_ctrl`.
        proj_summary_ctrl <- cbind(proj_summary_ctrl, batch=ctrl_samples[m,])
        ```

## BONUS: Using `map_lgl()`

!!!question "Exercise"
    1. Subset `proj_summary` to keep only the "high" and "low" samples based on the treament column. Save the new dataframe to a variable called `proj_summary_noctl`.
    2. Further, subset the dataframe to remove the non-numeric columns "Quality_format", and "treatment". Try to do this using the `map_lgl()` function in addition to `is.numeric()`. Save the new dataframe back to `proj_summary_noctl`.


    ???warning "Solution"

        ```r
        ## BONUS: Using `map_lgl()` 
        # 1. Subset `proj_summary` to keep only the "high" and "low" samples based on the treament column. Save the new dataframe to a variable called `proj_summary_noctl`
    
        proj_summary_noctl <- proj_summary[which(proj_summary$treatment != "control"),]

        # 2. Further subset the dataframe to remove the non-numeric columns "Quality_format", and "treatment". Try to do this using the `map()` function in addition to `is.numeric()`. Save the new dataframe back to `proj_summary_noctl`

        keep <- map_lgl(proj_summary_noctl, is.numeric)
        proj_summary_noctl <- proj_summary_noctl[,keep]
        ```


* * *


!!! quote "Attribution notice"
    * *This lesson has been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*

    * *The materials used in this lesson are adapted from work that is Copyright © Data Carpentry (http://datacarpentry.org/).All Data Carpentry instructional material is made available under the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0).*
