---
title: "Publish your project with `workflowr`"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 


- TODO

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Use `workflowr` function `wflow_publish()` to publish your website.  
- List the three steps involved in executing a call to `wflow_publish` function  
- Recognize that "publishing" your website synchronizes html files (ie, those outputted from rendering Rmd files) and the source Rmd files. By itself, it doesn't post your site to the internet.       


::::::::::::::::::::::::::::::::::::::::::::::::



```r
wflow_publish(files = "analysis/*Rmd", # publish all files ending with 'Rmd' in the analysis subdir
    message = "publish initial files" 
)
```


:::::::::::::::::::::::::::::::::::::: challenge

### What do the two arguments, `files` and `message` do and mean in the function `wflow_publish`?    


```r
?wflow_publish
```


```r
wflow_status(".")
```



:::::::::::::: solution

### Understanding `wflow_publish` arguments


```r
?wflow_publish
```

Looking at the help file for the function `wflow_publish`, we see: 

```
Usage:

     wflow_publish(
       files = NULL,
       message = NULL,
       all = FALSE,
       force = FALSE,
       update = FALSE,
       republish = FALSE,
       combine = "or",
       view = getOption("workflowr.view"),
       delete_cache = FALSE,
       seed = 12345,
       verbose = FALSE,
       dry_run = FALSE,
       project = "."
     )
```

and 

```
Arguments:

   files: character (default: NULL). R Markdown files and other files
          to be added and committed with Git (step 1). Any R Markdown
          files will also be built (step 2) and their output HTML and
          figures will be subsequently committed (step 3). Supports
          file globbing. The files are always built in the order they
          are listed.

 message: character (default: NULL). A commit message.
```



:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::



