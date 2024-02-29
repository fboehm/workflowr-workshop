---
title: "Using `wflow_publish` to 'publish' locally your website"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 


- How do I synchronize outputted htmls and source Rmds for my whole website?  

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Use `workflowr` function `wflow_publish()` to publish your website.  
- Recognize that "publishing" your website synchronizes html files (ie, those outputted from rendering Rmd files) and the source Rmd files. By itself, it doesn't post your site to the internet.       


::::::::::::::::::::::::::::::::::::::::::::::::

## `workflowr` & "publishing" analysis website  

- `wflow_publish` to synchronize outputted htmls and source Rmds  


```r
wflow_publish(files = "analysis/*.Rmd",
    message = "feat: rendered all Rmds to htmls for website" # fred likes informative git commit messages... but also try to not write too much
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





