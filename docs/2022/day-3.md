# Day Three

## Day Overview

### Lecture 3A: Introduction to Metagenomics

**Instructors**: Christina Warinner

**Abstract**: TBC

### Practical 3B-1: Introduction to R and the tidyverse

**Instructors**: Clemens Schmid and Nikolay Oskolkov

**Abstract**: R is an interpreted programming language with a particular focus on data manipulation and analysis. It is very well established for scientific computing and supported by an active community developing and maintaining a huge ecosystem of software packages for both general and highly derived applications.

In this session we will explore how to use R for a simple, standard data science workflow. We will import, clean, and visualise context and summary data for and from our ancient metagenomics analysis workflow. On the way we will learn about the RStudio integrated development environment, dip into the basic logic and syntax of R and finally write some first useful code within the tidyverse framework for tidy, readable and reproducible data analysis.

This session will be targeted at beginners without much previous experience with R or programming and will kickstart your journey to master this powerful tool.

🛈 This session will be held in parallel to the Introduction to Python and Pandas. Participants can chose which to attend based on their prior experience. We recommend the introduction to R session if you have no experience with neither R nor Python.

### Practical 3B-2: - Introduction to Python and Pandas

**Instructors**: _Maxime Borry_

**Abstract**: While R has traditionally been the language of choice for statistical programming for many years, Python has taken away some of the hegemony thanks to its numerous available libraries for machine and deep learning. With its ever increasing collection of libraries for statistics and bioinformatics, Python has now become one the most used language in the bioinformatics community.

In this tutorial mirroring to the R session, we will learn how to use the Python libraries Pandas for importing, cleaning, and manipulating data tables, and producing simple plots with the Python sister library of ggplot2, plotnine.

We will also get ourselves familiar with the Jupyter notebook environment, often used by many high performance computing clusters as an interactive scripting interface.
This session is meant for participants with a basic experience in R/tidyverse, but assumes no prior knowledge of Python/Jupyter.

🛈 This session will be held in parallel to the Introduction to R. Participants can chose which to attend based on their prior experience. We recommend the introduction to R session if you have no experience with neither R nor Python.

### Practical 3C: Taxonomic Profiling, OTU Tables and Visualisation

**Instructors**: Maxime Borry and Irina Velsko

**Abstract**: TBC

### Roundtable: Taxonomic Classifers

**Chairs**: Irina Velsko and James Fellows Yates

Which taxonomic classifier to pick is a context dependent question. Each classifier will has it's advantages and disadvantages depending on the type of data you have, and what research question you have. In this round table participants can ask for advice as to what to consider when selecting a particular classifier or classifiers for their projects.

## Lecture 3A: Introduction to Metagenomics

### Resources

### Readings

### Questions to think about

### Material

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSX9WVO_QLpx-xvJsaogt27Q3X3WW_wza9HWNuSuvcIWqPjEl_kqQ3Z_X45tbXZkQ7zDDFbCicd8e6h/embed?start=false&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## Software

For today's practical sessions, please activate the `r-python` conda [environment](2022/resources#software-and-data)

```bash
conda activate r-python
```

## Practical 3B-1: Introduction to R and the tidyverse

### Resources & Readings

- Grolemund, G., Wickham, H. 2017. R for Data Science. [Online Version available here](https://r4ds.had.co.nz)
- Chang, W. 2013. R Graphics Cookbook. [Online Version available here](https://r-graphics.org)
- Wickham, H. 2014. Tidy Data. Journal of Statistical Software, 59(10), 1–23. https://doi.org/10.18637/jss.v059.i10

### Material

<iframe src="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/nevrome/spaam_r_tidyverse_intro_2h/main/presentation.pdf&embedded=true" width="960" height="569"></iframe>

<!--The material for this course is available [here](https://github.com/nevrome/spaam_r_tidyverse_intro_2h) with a rendered version of the presentation [here](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/presentation.pdf). -->

## Practical 3B-2: Introduction to Python and Pandas

### Resources

### Readings

### Questions to think about

### Material

<iframe src="assets/slides/2022/3b2-python-pandas/tutorial.slides.html" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## Practical 3C: Taxonomic Profiling, OTU Tables and Visualisation

### Resources

### Readings

### Questions to think about

### Material

This session is run using a Jupyter notebook. This can be found [here](https://github.com/maxibor/microbiome_tutorial). However, it will already be installed on compute nodes during the summer school.
