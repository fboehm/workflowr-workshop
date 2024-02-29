---
title: "Build & publish website with `workflowr` functions"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 


- How do I assemble my Rmd files (*which contain my R code for the analysis*) into a website with results?   

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Use `workflowr` R function `wflow_build` to render Rmd files and build your website.  
- Use `workflowr` R function `wflow_status` to check status of your newly built (local, not on the internet) website.   


::::::::::::::::::::::::::::::::::::::::::::::::


```r
wflow_status()
```



```r
# from within the 'root' directory of your new project
wflow_build()
```

## Download a Rmd file


```r
download.file(url = "https://github.com/fboehm/sharing/blob/main/initial-analysis.Rmd", 
  destfile = "analysis/initial-analysis.Rmd"
)
```

## Check status again



```r
wflow_status()
```

:::::::::::::::::::::::::::::::::::::: challenge

### How does the output of `wflow_status` change after adding a new Rmd file to the "analysis" subdirectory? 


First, look at the output of `wflow_status`. Run it again if you lost its output.  
Then, create a new Rmd file called "preliminary-statistical-modeling.Rmd" and save it in your analysis subdirectory.  
Run `wflow_status` again and compare the new output with the current output.







:::::::::::::: solution

### `wflow_status()` output before adding preliminary-statistical-modeling.Rmd:

```
Status of 3 Rmd files

Totals:
 3 Unpublished

The following Rmd files require attention:

Unp analysis/about.Rmd
Unp analysis/index.Rmd
Unp analysis/license.Rmd

Key: Unp = Unpublished

The current Git status is: working directory clean

To publish your changes as part of your website, use `wflow_publish()`.
To commit your changes without publishing them yet, use
`wflow_git_commit()`.
```



### `wflow_status()` after adding preliminary-statistical-modeling.Rmd to analysis subdirectory:

```
Status of 3 Rmd files

Totals:
 3 Unpublished

The following Rmd files require attention:

Unp analysis/about.Rmd
Unp analysis/index.Rmd
Unp analysis/license.Rmd

Key: Unp = Unpublished

The current Git status is: working directory clean

To publish your changes as part of your website, use `wflow_publish()`.
To commit your changes without publishing them yet, use
`wflow_git_commit()`.
> wflow_status()
Status of 4 Rmd files

Totals:
 3 Unpublished
 1 Scratch

The following Rmd files require attention:

Unp analysis/about.Rmd
Unp analysis/index.Rmd
Unp analysis/license.Rmd
Scr analysis/preliminary-statistical-modeling.Rmd

Key: Unp = Unpublished, Scr = Scratch (Untracked)

The current Git status is:

    status substatus                                          file
 untracked untracked analysis/preliminary-statistical-modeling.Rmd

To publish your changes as part of your website, use `wflow_publish()`.
To commit your changes without publishing them yet, use
`wflow_git_commit()`.
```






:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::




