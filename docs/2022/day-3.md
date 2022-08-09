# Day Three

## Lecture 3A: Introduction to Metagenomics

**Instructors**: Christina Warinner

**Abstract**: This lecture introduces you to the basics of metagenomics, with an emphasis on tools and approaches that are used to study ancient metagenomes. We begin by covering the basic terminology used in metagenomics and microbiome research and discuss how the field has changed over time. We examine the species concept for microbes and challenges that arise in classifying microbial species with respect to taxonomy and phylogeny. We then proceed to taxonomic profiling and discuss the pros and cons of different taxonomic profilers. Afterwards, we explain how to estimate preservation in ancient metagenomic samples and how to clean up your datasets and remove contaminants. Finally, we discuss strategies for exploring and comparing the ecological diversity in your samples, including different strategies for data normalization, distance calculation, and ordination.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSX9WVO_QLpx-xvJsaogt27Q3X3WW_wza9HWNuSuvcIWqPjEl_kqQ3Z_X45tbXZkQ7zDDFbCicd8e6h/embed?start=false&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3a-intro-to-metagenomics/SPAAM%20Summer%20School%202022%20-%203A%20-%20Intro%20to%20Metagenomics.pdf).

### Resources

### Readings

- Breitwieser, F. P., Baker, D. N., & Salzberg, S. L. (2018). KrakenUniq: confident and fast metagenomics classification using unique k-mer counts. Genome Biology, 19(1), 1-10.
- Davis, N. M., Proctor, D. M., Holmes, S. P., Relman, D. A., & Callahan, B. J. (2018). Simple statistical identification and removal of contaminant sequences in marker-gene and metagenomics data.- Microbiome, 6(1), 1-14.
- Fellows Yates, J. A., Lamnidis, T. C., Borry, M., Valtueña, A. A., Fagernäs, Z., Clayton, S., ... & Peltzer, A. (2021). Reproducible, portable, and efficient ancient genome reconstruction with nf-core/- eager. PeerJ, 9, e10947.
- Huson, D. H., Auch, A. F., Qi, J., & Schuster, S. C. (2007). MEGAN analysis of metagenomic data. Genome Research, 17(3), 377-386.
- Knights, D., Kuczynski, J., Charlson, E.S., Zaneveld, J., Mozer, M.C., Collman, R.G., Bushman, F.D., Knight, R. and Kelley, S.T., 2011. Bayesian community-wide culture-independent microbial source - tracking. Nature Methods, 8(9), pp.761-763.
- Mann, A.E., Yates, J.A.F., Fagernäs, Z., Austin, R.M., Nelson, E.A. and Hofman, C.A., 2020. Do I have something in my teeth? The trouble with genetic analyses of diet from archaeological dental - calculus. Quaternary International.
- Marchesi, J. R., & Ravel, J. (2015). The vocabulary of microbiome research: a proposal. Microbiome, 3(1), 1-3.
- Pasolli, E., De Filippis, F., Mauriello, I. E., Cumbo, F., Walsh, A. M., Leech, J., ... & Ercolini, D. (2020). Large-scale genome-wide analysis links lactic acid bacteria from food with the gut - microbiome. Nature Communications, 11(1), 1-12.
- Segata, N., Waldron, L., Ballarini, A., Narasimhan, V., Jousson, O., & Huttenhower, C. (2012). Metagenomic microbial community profiling using unique clade-specific marker genes. Nature Methods, 9(8), - 811-814.
- Vågene, Å. J., Herbig, A., Campana, M. G., Robles García, N. M., Warinner, C., Sabin, S., ... & Krause, J. (2018). Salmonella enterica genomes from victims of a major sixteenth-century epidemic in - Mexico. Nature Ecology & Evolution, 2(3), 520-528.
- Warinner, C., Herbig, A., Mann, A., Yates, J. A. F., Weiβ, C. L., Burbano, H. A., ... & Krause, J. (2017). A robust framework for microbial archaeology. Annual review of genomics and human genetics,- 18, 321.
- Wood, D. E., Lu, J., & Langmead, B. (2019). Improved metagenomic analysis with Kraken 2. Genome Biology, 20(1), 1-13.

### Questions to think about

- What is a metagenome? a microbiota? a microbiome?
- What is ancient metagenomics?
- What challenges do DNA degradation and sample decay pose for ancient metagenomics
- How do you find out “who’s there” in your samples?
- How do alignment based and k-mer based taxonomic profilers differ? What are the advantages and disadvantages of each?
- Why does database selection matter?
- How do you estimate the preservation and integrity of your ancient metagenome?
- What are tools you can use to identify poorly preserved samples and remove contaminant taxa?
- What aspects of diversity are important in investigating microbial communities?
- Which distance metrics are commonly used to compare the beta-diversity of microbial communities and why? What are some advantages and disadvantages to these different approaches?

## Software

For today's practical sessions, please [activate](2022/resources#software-and-data) the `r-python` conda [environment](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day3.yml).

```bash
conda activate r-python
```

## Practical 3B-1: Introduction to R and the tidyverse

**Instructors**: Clemens Schmid and Nikolay Oskolkov

**Abstract**: R is an interpreted programming language with a particular focus on data manipulation and analysis. It is very well established for scientific computing and supported by an active community developing and maintaining a huge ecosystem of software packages for both general and highly derived applications.

In this session we will explore how to use R for a simple, standard data science workflow. We will import, clean, and visualise context and summary data for and from our ancient metagenomics analysis workflow. On the way we will learn about the RStudio integrated development environment, dip into the basic logic and syntax of R and finally write some first useful code within the tidyverse framework for tidy, readable and reproducible data analysis.

This session will be targeted at beginners without much previous experience with R or programming and will kickstart your journey to master this powerful tool.

🛈 This session will be held in parallel to the Introduction to Python and Pandas. Participants can chose which to attend based on their prior experience. We recommend the introduction to R session if you have no experience with neither R nor Python.

### Material

<iframe src="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/nevrome/spaam_r_tidyverse_intro_2h/main/presentation.pdf&embedded=true" width="960" height="569"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/presentation.pdf).

### Resources & Readings

- Grolemund, G., Wickham, H. 2017. R for Data Science. [Online Version available here](https://r4ds.had.co.nz)
- Chang, W. 2013. R Graphics Cookbook. [Online Version available here](https://r-graphics.org)
- Wickham, H. 2014. Tidy Data. Journal of Statistical Software, 59(10), 1–23. https://doi.org/10.18637/jss.v059.i10

## Practical 3B-2: Introduction to Python and Pandas

**Instructors**: _Maxime Borry_

**Abstract**: While R has traditionally been the language of choice for statistical programming for many years, Python has taken away some of the hegemony thanks to its numerous available libraries for machine and deep learning. With its ever increasing collection of libraries for statistics and bioinformatics, Python has now become one the most used language in the bioinformatics community.

In this tutorial mirroring to the R session, we will learn how to use the Python libraries Pandas for importing, cleaning, and manipulating data tables, and producing simple plots with the Python sister library of ggplot2, plotnine.

We will also get ourselves familiar with the Jupyter notebook environment, often used by many high performance computing clusters as an interactive scripting interface.
This session is meant for participants with a basic experience in R/tidyverse, but assumes no prior knowledge of Python/Jupyter.

🛈 This session will be held in parallel to the Introduction to R. Participants can chose which to attend based on their prior experience. We recommend the introduction to R session if you have no experience with neither R nor Python.

### Slides

<iframe src="assets/slides/2022/3b2-python-pandas/tutorial.slides.html" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/SPAAM%20Summer%20School%202022%20-%203B2%20-%20Intro%20to%20Python%20and%20Pandas.pdf).

This session is run using a Jupyter notebook. This can be found [here](https://github.com/maxibor/intro-to-pandas-plotnine). However, it will already be installed on compute nodes during the summer school.

### Resources

### Readings

### Questions to think about

## Practical 3C: Taxonomic Profiling, OTU Tables and Visualisation

**Instructors**: Maxime Borry and Irina Velsko

**Abstract**: TBC

### Slides

<iframe src="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/SPAAM-community/wss-summer-school/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/SPAAM%20Summer%20School%202022%20-%203C%20-%20Intro%20to%20microbial%20ecology%20for%20ancient%20DNA.pdf?embedded=true" width="960" height="569"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/SPAAM%20Summer%20School%202022%20-%203C%20-%20Intro%20to%20microbial%20ecology%20for%20ancient%20DNA.pdf).

This session is run using a Jupyter notebook. This can be found [here](https://github.com/maxibor/microbiome_tutorial). However, it will already be installed on compute nodes during the summer school.

### Resources

### Readings

### Questions to think about

### Roundtable: Taxonomic Classifers

**Chairs**: Irina Velsko and James Fellows Yates

Which taxonomic classifier to pick is a context dependent question. Each classifier will has it's advantages and disadvantages depending on the type of data you have, and what research question you have. In this round table participants can ask for advice as to what to consider when selecting a particular classifier or classifiers for their projects.
