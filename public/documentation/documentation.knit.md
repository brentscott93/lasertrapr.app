--- 
title: "`{lasertrapr}` Documentation"
author: "Brent Scott"
date: "2021-05-17"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
description: "Documentation for using the lasertrapr app"
---

# Getting Started

`{lasertrapr}` is an R-package/Shiny application built using the [`{golem}`](https://golemverse.org/) framework for automating the analysis of laser trap data. Please note that the app is currently still under development. Users should proceed with caution. 
 
*NOTE: an R-package is denoted by the `{}` braces* 

## Install R & RStudio

`{lasertrapr}` can be launched from am active R-session so before you begin to need to [download and install R](https://cloud.r-project.org/) and [RStudio](https://www.rstudio.com/products/rstudio/download/#download). Both of these are free. RStudio is an IDE (integrated development environment) and is not 100% necessary, but is recommended. Follow the instructions on the respective websites to complete installation. 

Additionally, you will need to install the [R build toolchain](https://r-pkgs.org/setup.html#setup-tools). This allows a user to build a package from source on their own computer. The link provides directions on how to do this on Windows, Mac, and Linux. 

At the moment there is a lot of overheard needed to get the application up and running. Hopefully, in the future a more stable version can be released as a standalone program. 

## Download `{lasertrapr}`

You can download the developers version from Github. 


```r
install.packages("devtools") # i.e. "developer tools"
library(devtools) # loads the package
install_github("brentscott93/lasertrapr") # downloads lasertraor from github
```

Both `{devtools}` and `{lasertrapr}` will install dependencies. Update and install all that they want when prompted. Sometimes package installation can be finicky with R so alternatively you can install `{devtools}` from within the RStudio IDE by navigating to the "Packages" tab in the lower right box and clicking "Install". For some reason this will work if `install.packages()` is being fussy. 

## Launch the App

Once your have successfully installed and built the `{lasertrapr}` package, you are ready for launch:


```r
library(lasertrapr) # load the package and its dependencies
run_app() # this will launch the app GUI in your default web browser
```

Once the initial setup and installation is completed, the above two lines is the only code that will need to be run each time you want to use the app. You can update to the current developers version anytime by re-running `devtools::install_gitub("brentscott93/lasertrapr")`. 



<!--chapter:end:index.Rmd-->

# Introduction {#intro}

You can label chapter and section titles using `{#label}` after them, e.g., we can reference Chapter \@ref(intro). If you do not manually label them, there will be automatic labels anyway, e.g., Chapter \@ref(methods).

Figures and tables with captions will be placed in `figure` and `table` environments, respectively.


```r
par(mar = c(4, 4, .1, .1))
plot(pressure, type = 'b', pch = 19)
```

<div class="figure" style="text-align: center">
<img src="documentation_files/figure-html/nice-fig-1.png" alt="Here is a nice figure!" width="80%" />
<p class="caption">(\#fig:nice-fig)Here is a nice figure!</p>
</div>

Reference a figure by its code chunk label with the `fig:` prefix, e.g., see Figure \@ref(fig:nice-fig). Similarly, you can reference tables generated from `knitr::kable()`, e.g., see Table \@ref(tab:nice-tab).


```r
knitr::kable(
  head(iris, 20), caption = 'Here is a nice table!',
  booktabs = TRUE
)
```



Table: (\#tab:nice-tab)Here is a nice table!

| Sepal.Length| Sepal.Width| Petal.Length| Petal.Width|Species |
|------------:|-----------:|------------:|-----------:|:-------|
|          5.1|         3.5|          1.4|         0.2|setosa  |
|          4.9|         3.0|          1.4|         0.2|setosa  |
|          4.7|         3.2|          1.3|         0.2|setosa  |
|          4.6|         3.1|          1.5|         0.2|setosa  |
|          5.0|         3.6|          1.4|         0.2|setosa  |
|          5.4|         3.9|          1.7|         0.4|setosa  |
|          4.6|         3.4|          1.4|         0.3|setosa  |
|          5.0|         3.4|          1.5|         0.2|setosa  |
|          4.4|         2.9|          1.4|         0.2|setosa  |
|          4.9|         3.1|          1.5|         0.1|setosa  |
|          5.4|         3.7|          1.5|         0.2|setosa  |
|          4.8|         3.4|          1.6|         0.2|setosa  |
|          4.8|         3.0|          1.4|         0.1|setosa  |
|          4.3|         3.0|          1.1|         0.1|setosa  |
|          5.8|         4.0|          1.2|         0.2|setosa  |
|          5.7|         4.4|          1.5|         0.4|setosa  |
|          5.4|         3.9|          1.3|         0.4|setosa  |
|          5.1|         3.5|          1.4|         0.3|setosa  |
|          5.7|         3.8|          1.7|         0.3|setosa  |
|          5.1|         3.8|          1.5|         0.3|setosa  |

You can write citations, too. For example, we are using the **bookdown** package [@R-bookdown] in this sample book, which was built on top of R Markdown and **knitr** [@xie2015].

<!--chapter:end:01-intro.Rmd-->

# Literature

Here is a review of existing methods.

<!--chapter:end:02-literature.Rmd-->

# Methods

We describe our methods in this chapter.

<!--chapter:end:03-method.Rmd-->

# Applications

Some _significant_ applications are demonstrated in this chapter.

## Example one

## Example two

<!--chapter:end:04-application.Rmd-->

# Final Words

We have finished a nice book.

<!--chapter:end:05-summary.Rmd-->


# References {-}


<!--chapter:end:06-references.Rmd-->

