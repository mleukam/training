# Reproducible research #
A collection of training materials and best practices

## Overview ##
*"Someone unfamiliar with your project should be able to look at your computer files and understand in detail what you did and why. This 'someone' could be any of a variety of people: someone who read your published article and wants to try to reproduce your work, a collaborator who wants to understand the details of your experiments, a future student working in your lab who wants to extend your work after you have moved on to a new job, your research advisor, who may be interested in understanding your work or who may be evaluating your research skills. Most commonly, however, that 'someone' is you"* -[William Stafford Noble](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)

A guide to organizing data science projects (updated 2018) can be found [here](https://medium.com/outlier-bio-blog/a-quick-guide-to-organizing-data-science-projects-updated-for-2016-4cbb1e6dac71)

Data science projects should be 
1. Versioned with a version-control system (Github)
2. Built with a build management tool (Snakemake, CWL, or WDL)
3. Deployed with a deployment tool (Docker or Singularity)
4. Shared and documented with a browser-based app (JupyterLab or Rnotebook)

### Version control with Github ###
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
