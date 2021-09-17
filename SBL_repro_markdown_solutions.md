Let’s get reproducible\!
================
Helena Hartmann
23.09.2021

## GitHub Documents

This is an R Markdown format used for publishing markdown documents to
GitHub. When you click the **Knit** button all R code chunks are run and
a markdown file (.md) suitable for publishing to GitHub is generated.

The repository to this file can be found
[here](https://github.com/helenahartmann/git_md_intro).

## Exercises

1.  Edit the title of your header to change the title of your document.
    Add yourself as an author by adding ‘author: “Your Name”’ to the
    header in an extra line. Add today’s date by adding ‘date:
    “23.09.2021”’ in an extra line. KNIT that document\! What happens?
    -\> md file is created, window opens

2.  Change the output from “github\_document” to “pdf\_document”, knit
    and see what happens. Change it back to github\_document afterwards.
    -\> pdf opens

3.  Rename the chunks you have to something that makes more sense than
    chunkname1, chunkname2 etc.

4.  Have a look at the chunk named data – why doesn’t it appear in the
    formatted file? How can we change that? -\> change include to TRUE

5.  Add some text to your document and change the formatting using
    *single asterisk* for italic or **double asterisk** for bold text.

6.  Let’s load some data about penguins\! Add a new chunk by clicking
    the *Insert Chunk* button on the toolbar or by pressing
    *Ctrl+Alt+I*. Now we are going to save that as a csv file.

7.  Check out the knitted output for the plot chunk. Now add ‘,
    echo=FALSE’ to the chunk producing the plot, knit it and see what
    changes.

## Including a chunk

``` r
# This is a code chunk. because we set the chunk options to include = FALSE, this chunk will not show up in our formatted output document of choice. Change this to TRUE to show the chunk.

knitr::opts_chunk$set(echo = TRUE)
# this option will set to show code and output for all chunks

2 + 3
```

    ## [1] 5

## Including Text

You can include text just by writing in the file and using *RMarkdown*
to edit the **formatting**. You can also include inline code:

The mean speed of cars in the cars dataset is 15.4 and the mean distance
is 42.98. The dataset has 50 observations.

## Including Code

You can include R code in the document as follows:

``` r
# change the chunkname above
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Loading and displaying data

You can load some data about penguins.

``` r
# load some data
install.packages("palmerpenguins")
```

    ## Installing package into '/home/hartmann/R/x86_64-pc-linux-gnu-library/3.6'
    ## (as 'lib' is unspecified)

``` r
library(palmerpenguins)
data = penguins

# Let's look at it
head(data)
```

    ##   species    island bill_length_mm bill_depth_mm flipper_length_mm body_mass_g
    ## 1  Adelie Torgersen           39.1          18.7               181        3750
    ## 2  Adelie Torgersen           39.5          17.4               186        3800
    ## 3  Adelie Torgersen           40.3          18.0               195        3250
    ## 4  Adelie Torgersen             NA            NA                NA          NA
    ## 5  Adelie Torgersen           36.7          19.3               193        3450
    ## 6  Adelie Torgersen           39.3          20.6               190        3650
    ##      sex year
    ## 1   male 2007
    ## 2 female 2007
    ## 3 female 2007
    ## 4   <NA> 2007
    ## 5 female 2007
    ## 6   male 2007

``` r
table(data$species)
```

    ## 
    ##    Adelie Chinstrap    Gentoo 
    ##       152        68       124

``` r
# Now we want to save it as a csv file
write.csv(data,'penguin_data.csv')
```

## Including Plots

You can also embed plots, for example:

![](SBL_repro_markdown_solutions_files/figure-gfm/plot-1.png)<!-- -->

## Sources

#### More information

Find some more information on RMarkdown and RNotebooks under [this
link](https://argoshare.is.ed.ac.uk/healthyr_book/chap12-h1.html).

#### Cheatsheets

Some cheatsheets can be found
[here](https://raw.githubusercontent.com/rstudio/cheatsheets/master/rmarkdown-2.0.pdf)
and
[here](www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf).
