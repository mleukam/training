
# Data Analysis #

> “The combination of some data and an aching desire for an answer does not ensure that a reasonable answercan be extracted from a given body of data”*
> - John Tukey

The recomended tools for a biomedical researcher first starting data analysis are Linux/shell and R. These will be sufficient the nearly all the current workflows in experimental data analysis and bioinformatics.

## Getting started in R ##
R is a programming language that is a preferred outlet for statisticians and data analysts to publish tools for manipulating, testing, and plotting data. 

**First set up your computer.** Both downloads are free and open-source software.

 * [Download R from CRAN](https://cran.r-project.org/): this contains the interpreter and a few core libraries
 * [Download RStudio](https://www.rstudio.com/products/rstudio/download/): this is an integrated development environment that contains a text editor for typing R code, a console to type code interactively to the interpreter, a file management window, and other utilities.

**Learning the basics.** First you need to learn how to assign variables and call functions. Also need to learn what kinds of data can be stored in R (characters, integers, decimal numbers, boolean operators, factors) and basic manipulation of data structures (vector, list, matrix, data frame, tibble).

 * [Datacamp introduction to R](https://www.datacamp.com/courses/free-introduction-to-r)
 * Built in interactive R tutorial called Swirl (google this for current instructions)
 
 **Tidy data.** In order to analyze data, you will spend most of your time cleaning and formatting data. The Tidyverse is a collection of packages for importing, summarizing, cleaning, merging, formatting, and most importantly plotting data. Hadley Wickham was the author or driving force behind all of these packages, and his introductary book is the best source for learning and reference.

 * [R for Data Science](https://r4ds.had.co.nz/): free and open online; buy a paper copy only if you like

The best way to practice is to get some data you want analyzed and figure out how to do it. Use Google liberally. Install and try out some packages. The help function in RStudio and Stack Overflow will be your friend.

## Recommended beginner workflow in R:

 * Make a folder for your projects in your file manager
 * Open RStudio and go to File --> New Project and choose "make a project in a new folder." Choose your project folder for the parent.
 * Once in your project, go to File --> new File and choose R notebook. Inside the notebook, write the date you started and the purpose of what you are doing. Then start adding code blocks. Best practice is to always start with a blank environment, so the first line of scripts is usually `rm(list = ls())`.
 * [A pitch for R notebooks](https://rviews.rstudio.com/2017/03/15/why-i-love-r-notebooks/)
 * [Details about R notebooks](https://bookdown.org/yihui/rmarkdown/notebook.html)
 * Eventually you will be doing all of your analyses with version control using tools like `git` and `workflowr`. As you get started though, just save all your R notebooks in a subfolder of your project folder (I usually call this `analysis`). Save your input data in a subfolder named `data` and your output datasets in `output`.

## Moving and storing big data
Large datasets are often stored on institional servers, and if heavy computational lifting is required, are analyzed on high-performance computing clusters. The operating system for the servers and HPC is Linux. One typically interacts with Linux via a command line terminal window, which is a native program on a Mac (called terminal). Windows users can use Windows Subsystem for Linux [(WSL)](https://docs.microsoft.com/en-us/windows/wsl/install-win10). Command line is also called Unix command line, Shell, or BASH, among other things. While these all technically different things, for our initial purposes they can be taken to be the same.

You can go really far in command line with a handful of commands.
A single online course should be enough to get started. [This is an example from Datacamp](https://www.datacamp.com/courses/introduction-to-shell-for-data-science).

You can also access the terminal from the RStudio console by turning on this option in your preferences.

# Bioinformatics Learning #

 * [Rosalind problems](http://rosalind.info/problems/locations/)
 * [Biostar handbook](https://www.biostarhandbook.com/)
 * [Introduction to the bioconductor family of R packages](https://www.bioconductor.org/help/course-materials/2016/BiocIntro-May/)

# Reproducible research #

## Overview ##
> "Someone unfamiliar with your project should be able to look at your computer files and understand in detail what you did and why. This 'someone' could be any of a variety of people: someone who read your published article and wants to try to reproduce your work, a collaborator who wants to understand the details of your experiments, a future student working in your lab who wants to extend your work after you have moved on to a new job, your research advisor, who may be interested in understanding your work or who may be evaluating your research skills. Most commonly, however, that 'someone' is you"
> -[William Stafford Noble](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)

A guide to organizing data science projects (updated 2018) can be found [here](https://medium.com/outlier-bio-blog/a-quick-guide-to-organizing-data-science-projects-updated-for-2016-4cbb1e6dac71)

Bioinformatics projects should be 
1. Versioned with a version-control system (Github)
2. Built with a build management tool (Nextflow, Snakemake, CWL, or WDL)
3. Deployed with a deployment tool (Docker or Singularity)
4. Shared and documented with a browser-based app (Project Wiki, JupyterLab or WorkflowR)

### Version control with Git using GitHub ###
* Github tutorial
* Github tips

### Build management with Snakemake ###
Snakemake follows the GNU Make paradigm: workflows are defined in terms of rules that define how to create output files from input files. Dependencies between the rules are determined automatically, creating a DAG (directed acyclic graph) of jobs that can be automatically parallelized. Snakemake sets itself apart from existing text-based workflow systems in the following way. Hooking into the Python interpreter, Snakemake offers a definition language that is an extension of Python with syntax to define rules and workflow specific properties. This allows to combine the flexibility of a plain scripting language with a pythonic workflow definition. The Python language is known to be concise yet readable and can appear almost like pseudo-code. The syntactic extensions provided by Snakemake maintain this property for the definition of the workflow. Further, Snakemake’s scheduling algorithm can be constrained by priorities, provided cores and customizable resources and it provides a generic support for distributed computing (e.g., cluster or batch systems). Hence, a Snakemake workflow scales without modification from single core workstations and multi-core servers to cluster or batch systems.

Here is a detailed [tutorial](https://snakemake.readthedocs.io/en/stable/tutorial/tutorial.html)

### Deployment tools ###

### Documentation and sharing ###
* JupyterLab [tutorial](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)
* Open Science Foundation [link](https://osf.io/)
* Archive utility

## File organization ##
A suggested file structure for data science projects:

![picture alt](http://journals.plos.org/ploscompbiol/article/figure/image?size=large&id=10.1371/journal.pcbi.1000424.g001 "Source is Noble 2009 PLOS Computational Biology")

## Workflow ##
