Let’s get reproducible!
================
Helena Hartmann
04.08.2021

## GitHub Documents

This is an R Markdown format used for publishing markdown documents to
GitHub. When you click the **Knit** button all R code chunks are run and
a markdown file (.md) suitable for publishing to GitHub is generated.

## Exercises

1.  Edit the title of your header to change the title of your document.
    Add yourself as an author by adding ‘author: “Your Name”’ to the
    header in an extra line. Add today’s date by adding ‘date: “Date”’
    in an extra line.
2.  Rename the second and third chunk to something that makes more sense
    than chunkname1 and chunkname2.
3.  Add some text to your document and change the formatting using *…*
    for italic or **…** for bold text.
4.  Check out the knitted output for the plot chunk. Now add ‘,
    echo=FALSE’ to the chunk producing the plot, knit it and see what
    changes.
5.  Add a new chunk by clicking the *Insert Chunk* button on the toolbar
    or by pressing *Ctrl+Alt+I*.

## Including a chunk

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

## Including Plots

You can also embed plots, for example:

``` r
# change the chunkname above
# add ', echo=FALSE' to the chunk options above and see what changes in your output when you knit
plot(pressure)
```

![](SBL_repro_markdown_files/figure-gfm/chunkname2-1.png)<!-- -->

## Sources

#### More information

Find some more information on RMarkdown and RNotebooks under [this
link](https://argoshare.is.ed.ac.uk/healthyr_book/chap12-h1.html).

#### Cheatsheets

Some cheatsheets can be found
[here](https://raw.githubusercontent.com/rstudio/cheatsheets/master/rmarkdown-2.0.pdf)
and
[here](www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf).
