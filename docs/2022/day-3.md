# Day Three

## Lecture 3A: Introduction to Metagenomics

**Instructors**: Christina Warinner

**Abstract**: This lecture introduces you to the basics of metagenomics, with an emphasis on tools and approaches that are used to study ancient metagenomes. We begin by covering the basic terminology used in metagenomics and microbiome research and discuss how the field has changed over time. We examine the species concept for microbes and challenges that arise in classifying microbial species with respect to taxonomy and phylogeny. We then proceed to taxonomic profiling and discuss the pros and cons of different taxonomic profilers. Afterwards, we explain how to estimate preservation in ancient metagenomic samples and how to clean up your datasets and remove contaminants. Finally, we discuss strategies for exploring and comparing the ecological diversity in your samples, including different strategies for data normalization, distance calculation, and ordination.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSX9WVO_QLpx-xvJsaogt27Q3X3WW_wza9HWNuSuvcIWqPjEl_kqQ3Z_X45tbXZkQ7zDDFbCicd8e6h/embed?start=false&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3a-intro-to-metagenomics/SPAAM%20Summer%20School%202022%20-%203A%20-%20Intro%20to%20Metagenomics.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/O5IE5wgckLw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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

### Slides

<iframe src="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/nevrome/spaam_r_tidyverse_intro_2h/main/presentation.pdf&embedded=true" width="960" height="569"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/presentation.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/b32FRYWwSrg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>
        <div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### A crash course on R for data analysis

##### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.6983148](https://doi.org/10.5281/zenodo.6983148). See instructions on page.

##### Getting started for this workshop

- Activate the relevant conda environment (don't forget to deactivate it later!)

  ```bash
  conda activate r-python
  ```

- Navigate to

  ```bash
  /<path>/<to>/3b-1-introduction-to-r-and-the-tidyverse/spaam_r_tidyverse_intro_2h
  ```

- Pull the latest changes in this Git repository

  ```bash
  git pull
  ```

- Open RStudio
- Load the project with `File > Open Project...`
- Open the file `presentation.Rmd` in RStudio

##### Table of Contents

- The working environment
- Loading data into tibbles
- Plotting data in tibbles
- Conditional queries on tibbles
- Transforming and manipulating tibbles
- Combining tibbles with join operations

##### The working environment

###### R, RStudio and the tidyverse

- R is a fully featured programming language, but it excels as an environment for (statistical) data analysis ([https://www.r-project.org](https://www.r-project.org))

- RStudio is an integrated development environment (IDE) for R (and other languages): ([https://www.rstudio.com/products/rstudio](https://www.rstudio.com/products/rstudio))

- The tidyverse is a collection of R packages with well-designed and consistent interfaces for the main steps of data analysis: loading, transforming and plotting data ([https://www.tidyverse.org](https://www.tidyverse.org))
  - This introduction works with tidyverse ~v1.3.0
  - We will learn about `readr`, `tibble`, `ggplot2`, `dplyr`, `magrittr` and `tidyr`
  - `forcats` will be briefly mentioned
  - `purrr` and `stringr` are left out

##### Loading data into tibbles

###### Reading data with readr

- With R we usually operate on data in our computer's memory
- The tidyverse provides the package `readr` to read data from text files into the memory
- `readr` can read from our file system or the internet
- It provides functions to read data in almost any (text) format:

  ```r
  readr::read_csv()   # .csv files
  readr::read_tsv()   # .tsv files
  readr::read_delim() # tabular files with an arbitrary separator
  readr::read_fwf()   # fixed width files
  readr::read_lines() # read linewise to parse yourself
  ```

- `readr` automatically detects column types -- but you can also define them manually

###### How does the interface of `read_csv` work

- We can learn more about a function with `?`. To open a help file: `?readr::read_csv`
- `readr::read_csv` has many options to specify how to read a text file

  ```r
  read_csv(
  file,                      # The path to the file we want to read
  col_names = TRUE,          # Are there column names?
  col_types = NULL,          # Which types do the columns have? NULL -> auto
  locale = default_locale(), # How is information encoded in this file?
  na = c("", "NA"),          # Which values mean "no data"
  trim_ws = TRUE,            # Should superfluous white-spaces be removed?
  skip = 0,                  # Skip X lines at the beginning of the file
  n_max = Inf,               # Only read X lines
  skip_empty_rows = TRUE,    # Should empty lines be ignored?
  comment = "",              # Should comment lines be ignored?
  name_repair = "unique",    # How should "broken" column names be fixed
  ...
  )
  ```

###### What does `readr` produce? The `tibble`

```r
sample_table_path <- "/vol/volume/3b-1-introduction-to-r-and-the-tidyverse/ancientmetagenome-hostassociated_samples.tsv"
sample_table_url <-
"https://raw.githubusercontent.com/SPAAM-community/AncientMetagenomeDir/b187df6ebd23dfeb42935fd5020cb615ead3f164/
ancientmetagenome-hostassociated/samples/ancientmetagenome-hostassociated_samples.tsv"
```

```r
samples <- readr::read_tsv(sample_table_url)
```

- The `tibble` is a "data frame", a tabular data structure with rows and columns
- Unlike a simple array, each column can have another data type

```r
print(samples, n = 3)
```

###### How to look at a `tibble`

```r
samples          # Typing the name of an object will print it to the console
str(samples)     # A structural overview of an object
summary(samples) # A human-readable summary of an object
View(samples)    # RStudio's interactive data browser
```

- R provides a very flexible indexing operation for `data.frame`s and `tibble`s

  ```r
  samples[1,1]                         # Access the first row and column
  samples[1,]                          # Access the first row
  samples[,1]                          # Access the first column
  samples[c(1,2,3),c(2,3,4)]           # Access values from rows and columns
  samples[,-c(1,2)]                    # Remove the first two columns
  samples[,c("site_name", "material")] # Columns can be selected by name
  ```

- `tibble`s are mutable data structures, so their content can be overwritten

  ```r
  samples[1,1] <- "Cheesecake2015"     # replace the first value in the first column
  ```

##### Plotting data in `tibble`s

###### `ggplot2` and the "grammar of graphics"

- `ggplot2` offers an unusual, but powerful and logical interface
- The following example describes a stacked bar chart

  ```r
  library(ggplot2) # Loading a library to use its functions without ::

  ggplot(          # Every plot starts with a call to the ggplot() function
  data = samples # This function can also take the input tibble
  ) +              # The plot consists of functions linked with +
  geom_bar(        # "geoms" define the plot layers we want to draw
  mapping = aes( # The aes() function maps variables to visual properties
      x = publication_year, # publication_year -> x-axis
      fill = community_type # community_type -> fill color
  )
  )
  ```

- `geom_*`: data + geometry (bars) + statistical transformation (sum)

###### `ggplot2` and the "grammar of graphics"

- This is the plot described above: number of samples per community type through time

  ```r
  ggplot(samples) +
  geom_bar(aes(x = publication_year, fill = community_type))
  ```

###### `ggplot2` features many geoms

![figures/geom_cheatsheet.png](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/geom_cheatsheet.png)(){width=55%}

- RStudio shares helpful cheatsheets for the tidyverse and beyond: [https://www.rstudio.com/resources/cheatsheets](https://www.rstudio.com/resources/cheatsheets)

###### `scale`s control the behaviour of visual elements

- Another plot: Boxplots of sample age through time

  ```r
  ggplot(samples) +
  geom_boxplot(aes(x = as.factor(publication_year), y = sample_age))
  ```

- This is not well readable, because extreme outliers dictate the scale

###### `scale`s control the behaviour of visual elements

- We can change the **scale** of different visual elements - e.g. the y-axis

  ```r
  ggplot(samples) +
  geom_boxplot(aes(x = as.factor(publication_year), y = sample_age)) +
  scale_y_log10()
  ```

- The log-scale improves readability

###### `scale`s control the behaviour of visual elements

- (Fill) color is a visual element of the plot and its scaling can be adjusted

  ```r
  ggplot(samples) +
  geom_boxplot(aes(x = as.factor(publication_year), y = sample_age,
                  fill = as.factor(publication_year))) +
  scale_y_log10() + scale_fill_viridis_d(option = "C")
  ```

###### Defining plot matrices via `facet`s

- Splitting up the plot by categories into **facets** is another way to visualize more variables at once

  ```r
  ggplot(samples) +
  geom_count(aes(x = as.factor(publication_year), y = material)) +
  facet_wrap(~archive)
  ```

- Unfortunately the x-axis became unreadable

###### Setting purely aesthetic settings with `theme`

- Aesthetic changes like this can be applied as part of the `theme`

  ```r
  ggplot(samples) +
  geom_count(aes(x = as.factor(publication_year), y = material)) +
  facet_wrap(~archive) +
  theme(axis.text.x = element_text(angle = 45, hjust = 1, vjust = 1))
  ```

###### Exercise 1

1. Look at the `mtcars` dataset and read up on the meaning of its variables

   ```r

   ```

2. Visualize the relationship between _Gross horsepower_ and _1/4 mile time_

   ```r

   ```

3. Integrate the _Number of cylinders_ into your plot

   ```r

   ```

###### Possible solutions 1

1. Look at the `mtcars` dataset and read up on the meaning of its variables

   ```r
   ?mtcars
   ```

2. Visualize the relationship between _Gross horsepower_ and _1/4 mile time_

   ```r
   ggplot(mtcars) + geom_point(aes(x = hp, y = qsec))
   ```

3. Integrate the _Number of cylinders_ into your plot

   ```r
   ggplot(mtcars) + geom_point(aes(x = hp, y = qsec, color = as.factor(cyl)))
   ```

##### Conditional queries on tibbles

###### Selecting columns and filtering rows with `select` and `filter`

- The `dplyr` package includes powerful functions to subset data in tibbles based on conditions
- `dplyr::select` allows to select columns

  ```r
  dplyr::select(samples, project_name, sample_age)   # reduce to two columns
  dplyr::select(samples, -project_name, -sample_age) # remove two columns
  ```

- `dplyr::filter` allows for conditional filtering of rows

  ```r
  dplyr::filter(samples, publication_year == 2014)  # samples published in 2014
  dplyr::filter(samples, publication_year == 2014 |
                      publication_year == 2018)  # samples from 2015 OR 2018
  dplyr::filter(samples, publication_year %in% c(2014, 2018)) # match operator: %in%
  dplyr::filter(samples, sample_host == "Homo sapiens" &
                      community_type == "oral")  # oral samples from modern humans
  ```

###### Chaining functions together with the pipe `%>%`

- The pipe `%>%` in the `magrittr` package is a clever infix operator to chain data and operations

  ```r
  library(magrittr)
  samples %>% dplyr::filter(publication_year == 2014)
  ```

- It forwards the LHS as the first argument of the function appearing on the RHS
- That allows for sequences of functions ("tidyverse style")

  ```r
  samples %>%
  dplyr::select(sample_host, community_type) %>%
  dplyr::filter(sample_host == "Homo sapiens" & community_type == "oral") %>%
  nrow() # count the rows
  ```

- `magrittr` also offers some more operators, among which the extraction `%$%` is particularly useful

  ```r
  samples %>%
  dplyr::filter(material == "tooth") %$%
  sample_age %>% # extract the sample_age column as a vector
  max()          # get the maximum of said vector
  ```

###### Summary statistics in `base` R

- Summarising and counting data is indispensable and R offers all operations you would expect in its `base` package

  ```r
  nrow(samples)              # number of rows in a tibble
  length(samples$site_name)  # length/size of a vector
  unique(samples$material)   # unique elements of a vector
  min(samples$sample_age)    # minimum
  max(samples$sample_age)    # maximum
  mean(samples$sample_age)   # mean
  median(samples$sample_age) # median
  var(samples$sample_age)    # variance
  sd(samples$sample_age)     # standard deviation
  quantile(samples$sample_age, probs = 0.75) # sample quantiles for the given probs
  ```

- many of these functions can ignore missing values with an option `na.rm = TRUE`

###### Group-wise summaries with `group_by` and `summarise`

- These summary statistics are particular useful when applied to conditional subsets of a dataset
- `dplyr` allows such summary operations with a combination of `group_by` and `summarise`

  ```r
  samples %>%
  dplyr::group_by(material) %>%  # group the tibble by the material column
  dplyr::summarise(
      min_age = min(sample_age),   # a new column: min age for each group
      median_age = median(sample_age), # a new column: median age for each group
      max_age = max(sample_age)    # a new column: max age for each group
  )
  ```

- grouping can be applied across multiple columns

  ```r
  samples %>%
  dplyr::group_by(material, sample_host) %>% # group by material and host
  dplyr::summarise(
      n = dplyr::n(),  # a new column: number of samples for each group
      .groups = "drop" # drop the grouping after this summary operation
  )
  ```

###### Sorting and slicing tibbles with `arrange` and `slice`

- `dplyr` allows to `arrange` tibbles by one or multiple columns

  ```r
  samples %>% dplyr::arrange(publication_year)        # sort by publication year
  samples %>% dplyr::arrange(publication_year,
                          sample_age)              # ... and sample age
  samples %>% dplyr::arrange(dplyr::desc(sample_age)) # sort descending on sample age
  ```

- Sorting also works within groups and can be paired with `slice` to extract extreme values per group

  ```r
  samples %>%
  dplyr::group_by(publication_year) %>%       # group by publication year
  dplyr::arrange(dplyr::desc(sample_age)) %>% # sort by age within (!) groups
  dplyr::slice_head(n = 2) %>%                # keep the first two samples per group
  dplyr::ungroup()                            # remove the still lingering grouping
  ```

- Slicing is also the relevant operation to take random samples from the observations in a tibble

  ```r
  samples %>% dplyr::slice_sample(n = 20)
  ```

###### Exercise 2

1. Determine the number of cars with four _forward gears_ (`gear`) in the `mtcars` dataset

   ```r

   ```

2. Determine the mean _1/4 mile time_ (`qsec`) per _Number of cylinders_ (`cyl`) group

   ```r

   ```

3. Identify the least efficient cars for both _transmission types_ (`am`)

   ```r

   ```

###### Possible solutions 2

1. Determine the number of cars with four _forward gears_ (`gear`) in the `mtcars` dataset

   ```r
   mtcars %>% dplyr::filter(gear == 4) %>% nrow()
   ```

2. Determine the mean _1/4 mile time_ (`qsec`) per _Number of cylinders_ (`cyl`) group

   ```r
   mtcars %>% dplyr::group_by(cyl) %>% dplyr::summarise(qsec_mean = mean(qsec))
   ```

3. Identify the least efficient cars for both _transmission types_ (`am`)

   ```r
   #mtcars3 <- tibble::rownames_to_column(mtcars, var = "car") %>% tibble::as_tibble()
   mtcars %>% dplyr::group_by(am) %>% dplyr::arrange(mpg) %>% dplyr::slice_head()
   ```

##### Transforming and manipulating tibbles

###### Renaming and reordering columns and values with `rename`, `relocate` and `recode`

- Columns in tibbles can be renamed with `dplyr::rename` and reordered with `dplyr::relocate`

  ```r
  samples %>% dplyr::rename(country = geo_loc_name) # rename a column
  samples %>% dplyr::relocate(site_name, .before = project_name) # reorder columns
  ```

- Values in columns can also be changed with `dplyr::recode`

  ```r
  samples$sample_host %>% dplyr::recode(`Homo sapiens` = "modern human")
  ```

- R supports explicitly ordinal data with `factor`s, which can be reordered as well
- `factor`s can be handeld more easily with the `forcats` package

  ```r
  ggplot(samples) + geom_bar(aes(x = community_type)) # bars are alphabetically ordered
  sa2 <- samples
  sa2$cto <- forcats::fct_reorder(sa2$community_type, sa2$community_type, length)
  # fct_reorder: reorder the input factor by a summary statistic on an other vector
  ggplot(sa2) + geom_bar(aes(x = community_type)) # bars are ordered by size
  ```

###### Adding columns to tibbles with `mutate` and `transmute`

- A common application of data manipulation is adding derived columns. `dplyr` offers that with `mutate`

  ```r
  samples %>%
  dplyr::mutate(                                               # add a column that
      archive_summary = paste0(archive, ": ", archive_accession) # combines two other
  ) %$% archive_summary                                        # columns
  ```

- `dplyr::transmute` removes all columns but the newly created ones

  ```r
  samples %>%
  dplyr::transmute(
      sample_name = tolower(sample_name), # overwrite this columns
      publication_doi                     # select this column
  )
  ```

- `tibble::add_column` behaves as `dplyr::mutate`, but gives more control over column position

  ```r
  samples %>% tibble::add_column(., id = 1:nrow(.), .before = "project_name")
  ```

###### Conditional operations with `ifelse` and `case_when`

- `ifelse` allows to implement conditional `mutate` operations, that consider information from other columns, but that gets cumbersome easily

  ```r
  samples %>% dplyr::mutate(hemi = ifelse(latitude >= 0, "North", "South")) %$% hemi

  samples %>% dplyr::mutate(
  hemi = ifelse(is.na(latitude), "unknown", ifelse(latitude >= 0, "North", "South"))
  ) %$% hemi
  ```

- `dplyr::case_when` is a much more readable solution for this application

  ```r
  samples %>% dplyr::mutate(
  hemi = dplyr::case_when(
      latitude >= 0 ~ "North",
      latitude < 0  ~ "South",
      TRUE          ~ "unknown" # TRUE catches all remaining cases
  )
  ) %$% hemi
  ```

###### Long and wide data formats

- For different applications or to simplify certain analysis or plotting operations data often has to be transformed from a **wide** to a **long** format or vice versa

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/pivot_longer_wider.png)

- A table in **wide** format has N key columns and N value columns
- A table in **long** format has N key columns, one descriptor column and one value column

###### A wide dataset

```r
carsales <- tibble::tribble(
  ~brand, ~`2014`, ~`2015`, ~`2016`, ~`2017`,
  "BMW",  20,      25,      30,      45,
  "VW",   67,      40,     120,      55
)

carsales
```

- Wide format becomes a problem, when the columns are semantically identical. This dataset is in wide format and we can not easily plot it
- We generally prefer data in long format, although it is more verbose with more duplication. "Long" format data is more "tidy"

###### Making a wide dataset long with `pivot_longer`

```r
carsales_long <- carsales %>% tidyr::pivot_longer(
  cols = tidyselect::num_range("", range = 2014:2017), # set of columns to transform
  names_to = "year",            # the name of the descriptor column we want
  names_transform = as.integer, # a transformation function to apply to the names
  values_to = "sales"           # the name of the value column we want
)

carsales_long
```

###### Making a long dataset wide with `pivot_wider`

```r
carsales_wide <- carsales_long %>% tidyr::pivot_wider(
  id_cols = "brand",  # the set of id columns that should not be changed
  names_from = year,  # the descriptor column with the names of the new columns
  values_from = sales # the value column from which the values should be extracted
)

carsales_wide
```

- Applications of wide datasets are adjacency matrices to represent graphs, covariance matrices or other pairwise statistics
- When data gets big, then wide formats can be significantly more efficient (e.g. for spatial data)

###### Exercise 3

1. Move the column `gear` to the first position of the mtcars dataset

   ```r

   ```

2. Make a new dataset `mtcars2` with the column `mpg` and an additional column `am_v`, which encodes the _transmission type_ (`am`) as either `"manual"` or `"automatic"`

   ```r

   ```

3. Count the number of cars per _transmission type_ (`am_v`) and _number of gears_ (`gear`). Then transform the result to a wide format, with one column per _transmission type_.

   ```r

   ```

###### Possible solutions 3

1. Move the column `gear` to the first position of the mtcars dataset

   ```r
   mtcars %>% dplyr::relocate(gear, .before = mpg)
   ```

2. Make a new dataset `mtcars2` with the column `gear` and an additional column `am_v`, which encodes the _transmission type_ (`am`) as either `"manual"` or `"automatic"`

   ```r
   mtcars2 <- mtcars %>% dplyr::mutate(
   gear, am_v = dplyr::case_when(am == 0 ~ "automatic", am == 1 ~ "manual")
   )
   ```

3. Count the number of cars in `mtcars2` per _transmission type_ (`am_v`) and _number of gears_ (`gear`). Then transform the result to a wide format, with one column per _transmission type_.

   ```r
   mtcars2 %>% dplyr::group_by(am_v, gear) %>% dplyr::tally() %>%
   tidyr::pivot_wider(names_from = am_v, values_from = n)
   ```

##### Combining tibbles with join operations

###### Types of joins

Joins combine two datasets x and y based on key columns

- Mutating joins add columns from one dataset to the other
  - Left join: Take observations from x and add fitting information from y
  - Right join: Take observations from y and add fitting information from x
  - Inner join: Join the overlapping observations from x and y
  - Full join: Join all observations from x and y, even if information is missing
- Filtering joins remove observations from x based on their presence in y
  - Semi join: Keep every observation in x that is in y
  - Anti join: Keep every observation in x that is not in y

###### A second dataset

```r
library_table_path <- "/vol/volume/3b-1-introduction-to-r-and-the-tidyverse/ancientmetagenome-hostassociated_libraries.tsv"
library_table_url <-
"https://raw.githubusercontent.com/SPAAM-community/AncientMetagenomeDir/b187df6ebd23dfeb42935fd5020cb615ead3f164/
ancientmetagenome-hostassociated/libraries/ancientmetagenome-hostassociated_libraries.tsv"

libraries <- readr::read_tsv(library_table_url)
print(libraries, n = 3)
```

###### Meaningful subsets

```r
samsub <- samples %>% dplyr::select(project_name, sample_name, sample_age)
libsub <- libraries %>% dplyr::select(project_name, sample_name, library_name, read_count)
```

```r
print(samsub, n = 3)
print(libsub, n = 3)
```

###### Left join

Take observations from x and add fitting information from y

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/left_join.png)

```r
left <- dplyr::left_join(
x = samsub,                           # 1060 observations
y = libsub,                           # 1657 observations
by = c("project_name", "sample_name") # the key columns by which to join
)

print(left, n = 1)
```

- Left joins are the most common join operation: Add information from another dataset

###### Right join

Take observations from y and add fitting information from x

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/right_join.png)

```r
right <- dplyr::right_join(
  x = samsub,                           # 1060 observations
  y = libsub,                           # 1657 observations
  by = c("project_name", "sample_name")
)

print(right, n = 1)
```

- Right joins are almost identical to left joins -- only x and y have reversed roles

###### Inner join

Join the overlapping observations from x and y

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/inner_join.png)

```r
inner <- dplyr::inner_join(
x = samsub,                           # 1060 observations
y = libsub,                           # 1657 observations
by = c("project_name", "sample_name")
)

print(inner, n = 1)
```

- Inner joins are a fast and easy way to check, to which degree two dataset overlap

###### Full join

Join all observations from x and y, even if information is missing

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/left_join.png/full_join.png)

```r
full <- dplyr::full_join(
  x = samsub,                           # 1060 observations
  y = libsub,                           # 1657 observations
  by = c("project_name", "sample_name")
)

print(full, n = 1)
```

- Full joins allow to preserve every bit of information

###### Semi join

Keep every observation in x that is in y

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/semi_join.png)

```r
semi <- dplyr::semi_join(
  x = samsub,                           # 1060 observations
  y = libsub,                           # 1657 observations
  by = c("project_name", "sample_name")
)
```

```r
print(semi, n = 1)
```

- Semi joins are underused operations to filter datasets

###### Anti join

Keep every observation in x that is not in y

![](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/figures/anti_join.png)

```r
anti <- dplyr::anti_join(
  x = samsub,                           # 1060 observations
  y = libsub,                           # 1657 observations
  by = c("project_name", "sample_name")
)
```

```r
print(anti, n = 1)
```

- Anti joins allow to quickly specify incomplete datasets and missing information

###### Exercise 4

Consider the following additional dataset:

```r
gear_opinions <- tibble::tibble(gear = c(3, 5), opinion = c("boring", "wow"))
```

1. Add my opinions about gears to the `mtcars` dataset

   ```r

   ```

2. Remove all cars from the dataset for which I don't have an opinion

   ```r

   ```

###### Possible Solutions 4

1. Add my opinions about gears to the `mtcars` dataset

   ```r
   dplyr::left_join(mtcars, gear_opinions, by = "gear")
   ```

2. Remove all cars from the dataset for which I don't have an opinion

   ```r
   dplyr::anti_join(mtcars, gear_opinions, by = "gear")
   ```

</div>

</details>

---

### Resources & Readings

- Grolemund, G., Wickham, H. 2017. R for Data Science. [Online Version available here](https://r4ds.had.co.nz)
- Chang, W. 2013. R Graphics Cookbook. [Online Version available here](https://r-graphics.org)
- Wickham, H. 2014. Tidy Data. Journal of Statistical Software, 59(10), 1–23. [https://doi.org/10.18637/jss.v059.i10](https://doi.org/10.18637/jss.v059.i10)

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

<iframe width="560" height="630" src="https://www.youtube.com/embed/V_EKs_zlO1w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>
        <div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

> ⚠️ We highly recommend viewing this walkthrough via the Jupyter notebook above!
> The output of commands on the website for this walkthrough are displayed in their
> own code blocks - be wary of what you copy-paste!

```python
from IPython.core.display import SVG
```

#### Introduction to data manipulation in Python with Pandas and visulization with plotnine

Maxime Borry  
SPAAM Summer School 2022

```python
SVG(filename='img/whoami.svg')
```

![svg](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/tutorial_files/tutorial_2_0.svg)

Over the last few years, Python has gained an immense amount of popularity thanks to its numerous libraries in the field of machine learning, statistical data analysis, and bioinformatics. While a few years ago, it was often necessary to go back to R for performing routine data manipulation and analysis tasks, nowadays Python has a vast ecosystem of libraries for doing just that.

Today, we will do a quick introduction of the most popular libraries for data analysis:

- [pandas](https://pandas.pydata.org/), for reading and manipulation tabular data
- [plotnine](https://plotnine.readthedocs.io/), the Python clone of ggplot2

#### Overview:

- 0 - Foreword, working in a jupyter environment
- 1 - Loading required libraries
- 2 - Foreword on Pandas
- 3 - Reading data with Pandas
- 4 - Dealing with missing data
- 5 - Computing basic statistics
- 6 - Filtering
- 8 - GroupBy operations
- 9 - Joining different tables
- 10 - Visualization with Plotnine

##### 0 - Foreword, working in a jupyter environment

###### This is a markdown cell

With some features of the markdown syntax, such as:

- **bold** `**bold**`
- _italic_ `*italic*`
- `inline code`

```
`inline code`
```

- [links](https://www.google.com/) `[links](https://www.google.com/)`

- Images  
  ![](https://maximeborry.com/authors/maxime/avatar_hu4dc3c23d5a8c195732bbca11d7ce61be_114670_270x270_fill_lanczos_center_2.png)  
  `![](https://maximeborry.com/authors/maxime/avatar_hu4dc3c23d5a8c195732bbca11d7ce61be_114670_270x270_fill_lanczos_center_2.png)`

- Latex code $ y = ax + b$  
  `$y = ax + b$`

```python
print("This is a code cell in Python")
```

    This is a code cell in Python

```python
! echo "This is code cell in bash"
```

    This is code cell in bash

```bash
%%bash

echo "This a multiline code cell"
echo "in bash"
```

    This a multiline code cell
    in bash

##### 1 - Loading required libraries

```python
import pandas as pd
import numpy as np
from plotnine import *
```

```python
pd.__version__
```

    '1.4.3'

```python
np.__version__
```

    '1.23.1'

```python
! conda list | grep plotnine
```

    plotnine                  0.9.0              pyhd8ed1ab_0    conda-forge

##### 2 - Foreword on Pandas

###### Pandas terminology

![](https://pandas.pydata.org/docs/_images/01_table_dataframe.svg)

![](https://pandas.pydata.org/docs/_images/01_table_series.svg)

The pandas getting started tutorial: [pandas.pydata.org/docs/getting_started](https://pandas.pydata.org/docs/getting_started/index.html#)

##### 3 - Reading data with Pandas

```python
sample_table_url = "https://raw.githubusercontent.com/SPAAM-community/AncientMetagenomeDir/b187df6ebd23dfeb42935fd5020cb615ead3f164/
ancientmetagenome-hostassociated/samples/ancientmetagenome-hostassociated_samples.tsv"
library_table_url = "https://raw.githubusercontent.com/SPAAM-community/AncientMetagenomeDir/b187df6ebd23dfeb42935fd5020cb615ead3f164/
ancientmetagenome-hostassociated/libraries/ancientmetagenome-hostassociated_libraries.tsv"
```

Getting help in Python

```python
help(pd.read_csv)
```

    Help on function read_csv in module pandas.io.parsers.readers:

    read_csv(filepath_or_buffer: 'FilePath | ReadCsvBuffer[bytes] | ReadCsvBuffer[str]',
    sep=<no_default>, delimiter=None, header='infer', names=<no_default>, index_col=None,
    usecols=None, squeeze=None, prefix=<no_default>, mangle_dupe_cols=True,
    dtype: 'DtypeArg | None' = None, engine: 'CSVEngine | None' = None, converters=None,
    true_values=None, false_values=None, skipinitialspace=False, skiprows=None, skipfooter=0,
    nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False,
    skip_blank_lines=True, parse_dates=None, infer_datetime_format=False, keep_date_col=False,
     date_parser=None, dayfirst=False, cache_dates=True, iterator=False, chunksize=None,
     compression: 'CompressionOptions' = 'infer', thousands=None, decimal: 'str' = '.',
     lineterminator=None, quotechar='"', quoting=0, doublequote=True, escapechar=None,
     comment=None, encoding=None, encoding_errors: 'str | None' = 'strict', dialect=None,
     error_bad_lines=None, warn_bad_lines=None, on_bad_lines=None, delim_whitespace=False,
     low_memory=True, memory_map=False, float_precision=None, storage_options: 'StorageOptions' = None)
        Read a comma-separated values (csv) file into DataFrame.

        Also supports optionally iterating or breaking of the file
        into chunks.

        Additional help can be found in the online docs for
        `IO Tools <https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html>`_.

        Parameters
        ----------
        filepath_or_buffer : str, path object or file-like object
            Any valid string path is acceptable. The string could be a URL. Valid
            URL schemes include http, ftp, s3, gs, and file. For file URLs, a host is
            expected. A local file could be: file://localhost/path/to/table.csv.

            If you want to pass in a path object, pandas accepts any ``os.PathLike``.

            By file-like object, we refer to objects with a ``read()`` method, such as
            a file handle (e.g. via builtin ``open`` function) or ``StringIO``.
        sep : str, default ','
            Delimiter to use. If sep is None, the C engine cannot automatically detect
            the separator, but the Python parsing engine can, meaning the latter will
            be used and automatically detect the separator by Python's builtin sniffer
            tool, ``csv.Sniffer``. In addition, separators longer than 1 character and
            different from ``'\s+'`` will be interpreted as regular expressions and
            will also force the use of the Python parsing engine. Note that regex
            delimiters are prone to ignoring quoted data. Regex example: ``'\r\t'``.
        delimiter : str, default ``None``
            Alias for sep.
        header : int, list of int, None, default 'infer'
            Row number(s) to use as the column names, and the start of the
            data.  Default behavior is to infer the column names: if no names
            are passed the behavior is identical to ``header=0`` and column
            names are inferred from the first line of the file, if column
            names are passed explicitly then the behavior is identical to
            ``header=None``. Explicitly pass ``header=0`` to be able to
            replace existing names. The header can be a list of integers that
            specify row locations for a multi-index on the columns
            e.g. [0,1,3]. Intervening rows that are not specified will be
            skipped (e.g. 2 in this example is skipped). Note that this
            parameter ignores commented lines and empty lines if
            ``skip_blank_lines=True``, so ``header=0`` denotes the first line of
            data rather than the first line of the file.
        names : array-like, optional
            List of column names to use. If the file contains a header row,
            then you should explicitly pass ``header=0`` to override the column names.
            Duplicates in this list are not allowed.
        index_col : int, str, sequence of int / str, or False, optional, default ``None``
          Column(s) to use as the row labels of the ``DataFrame``, either given as
          string name or column index. If a sequence of int / str is given, a
          MultiIndex is used.

          Note: ``index_col=False`` can be used to force pandas to *not* use the first
          column as the index, e.g. when you have a malformed file with delimiters at
          the end of each line.
        usecols : list-like or callable, optional
            Return a subset of the columns. If list-like, all elements must either
            be positional (i.e. integer indices into the document columns) or strings
            that correspond to column names provided either by the user in `names` or
            inferred from the document header row(s). If ``names`` are given, the document
            header row(s) are not taken into account. For example, a valid list-like
            `usecols` parameter would be ``[0, 1, 2]`` or ``['foo', 'bar', 'baz']``.
            Element order is ignored, so ``usecols=[0, 1]`` is the same as ``[1, 0]``.
            To instantiate a DataFrame from ``data`` with element order preserved use
            ``pd.read_csv(data, usecols=['foo', 'bar'])[['foo', 'bar']]`` for columns
            in ``['foo', 'bar']`` order or
            ``pd.read_csv(data, usecols=['foo', 'bar'])[['bar', 'foo']]``
            for ``['bar', 'foo']`` order.

            If callable, the callable function will be evaluated against the column
            names, returning names where the callable function evaluates to True. An
            example of a valid callable argument would be ``lambda x: x.upper() in
            ['AAA', 'BBB', 'DDD']``. Using this parameter results in much faster
            parsing time and lower memory usage.
        squeeze : bool, default False
            If the parsed data only contains one column then return a Series.

            .. deprecated:: 1.4.0
                Append ``.squeeze("columns")`` to the call to ``read_csv`` to squeeze
                the data.
        prefix : str, optional
            Prefix to add to column numbers when no header, e.g. 'X' for X0, X1, ...

            .. deprecated:: 1.4.0
               Use a list comprehension on the DataFrame's columns after calling ``read_csv``.
        mangle_dupe_cols : bool, default True
            Duplicate columns will be specified as 'X', 'X.1', ...'X.N', rather than
            'X'...'X'. Passing in False will cause data to be overwritten if there
            are duplicate names in the columns.
        dtype : Type name or dict of column -> type, optional
            Data type for data or columns. E.g. {'a': np.float64, 'b': np.int32,
            'c': 'Int64'}
            Use `str` or `object` together with suitable `na_values` settings
            to preserve and not interpret dtype.
            If converters are specified, they will be applied INSTEAD
            of dtype conversion.
        engine : {'c', 'python', 'pyarrow'}, optional
            Parser engine to use. The C and pyarrow engines are faster, while the python engine
            is currently more feature-complete. Multithreading is currently only supported by
            the pyarrow engine.

            .. versionadded:: 1.4.0

                The "pyarrow" engine was added as an *experimental* engine, and some features
                are unsupported, or may not work correctly, with this engine.
        converters : dict, optional
            Dict of functions for converting values in certain columns. Keys can either
            be integers or column labels.
        true_values : list, optional
            Values to consider as True.
        false_values : list, optional
            Values to consider as False.
        skipinitialspace : bool, default False
            Skip spaces after delimiter.
        skiprows : list-like, int or callable, optional
            Line numbers to skip (0-indexed) or number of lines to skip (int)
            at the start of the file.

            If callable, the callable function will be evaluated against the row
            indices, returning True if the row should be skipped and False otherwise.
            An example of a valid callable argument would be ``lambda x: x in [0, 2]``.
        skipfooter : int, default 0
            Number of lines at bottom of file to skip (Unsupported with engine='c').
        nrows : int, optional
            Number of rows of file to read. Useful for reading pieces of large files.
        na_values : scalar, str, list-like, or dict, optional
            Additional strings to recognize as NA/NaN. If dict passed, specific
            per-column NA values.  By default the following values are interpreted as
            NaN: '', '#N/A', '#N/A N/A', '#NA', '-1.#IND', '-1.#QNAN', '-NaN', '-nan',
            '1.#IND', '1.#QNAN', '<NA>', 'N/A', 'NA', 'NULL', 'NaN', 'n/a',
            'nan', 'null'.
        keep_default_na : bool, default True
            Whether or not to include the default NaN values when parsing the data.
            Depending on whether `na_values` is passed in, the behavior is as follows:

            * If `keep_default_na` is True, and `na_values` are specified, `na_values`
              is appended to the default NaN values used for parsing.
            * If `keep_default_na` is True, and `na_values` are not specified, only
              the default NaN values are used for parsing.
            * If `keep_default_na` is False, and `na_values` are specified, only
              the NaN values specified `na_values` are used for parsing.
            * If `keep_default_na` is False, and `na_values` are not specified, no
              strings will be parsed as NaN.

            Note that if `na_filter` is passed in as False, the `keep_default_na` and
            `na_values` parameters will be ignored.
        na_filter : bool, default True
            Detect missing value markers (empty strings and the value of na_values). In
            data without any NAs, passing na_filter=False can improve the performance
            of reading a large file.
        verbose : bool, default False
            Indicate number of NA values placed in non-numeric columns.
        skip_blank_lines : bool, default True
            If True, skip over blank lines rather than interpreting as NaN values.
        parse_dates : bool or list of int or names or list of lists or dict, default False
            The behavior is as follows:

            * boolean. If True -> try parsing the index.
            * list of int or names. e.g. If [1, 2, 3] -> try parsing columns 1, 2, 3
              each as a separate date column.
            * list of lists. e.g.  If [[1, 3]] -> combine columns 1 and 3 and parse as
              a single date column.
            * dict, e.g. {'foo' : [1, 3]} -> parse columns 1, 3 as date and call
              result 'foo'

            If a column or index cannot be represented as an array of datetimes,
            say because of an unparsable value or a mixture of timezones, the column
            or index will be returned unaltered as an object data type. For
            non-standard datetime parsing, use ``pd.to_datetime`` after
            ``pd.read_csv``. To parse an index or column with a mixture of timezones,
            specify ``date_parser`` to be a partially-applied
            :func:`pandas.to_datetime` with ``utc=True``. See
            :ref:`io.csv.mixed_timezones` for more.

            Note: A fast-path exists for iso8601-formatted dates.
        infer_datetime_format : bool, default False
            If True and `parse_dates` is enabled, pandas will attempt to infer the
            format of the datetime strings in the columns, and if it can be inferred,
            switch to a faster method of parsing them. In some cases this can increase
            the parsing speed by 5-10x.
        keep_date_col : bool, default False
            If True and `parse_dates` specifies combining multiple columns then
            keep the original columns.
        date_parser : function, optional
            Function to use for converting a sequence of string columns to an array of
            datetime instances. The default uses ``dateutil.parser.parser`` to do the
            conversion. Pandas will try to call `date_parser` in three different ways,
            advancing to the next if an exception occurs: 1) Pass one or more arrays
            (as defined by `parse_dates`) as arguments; 2) concatenate (row-wise) the
            string values from the columns defined by `parse_dates` into a single array
            and pass that; and 3) call `date_parser` once for each row using one or
            more strings (corresponding to the columns defined by `parse_dates`) as
            arguments.
        dayfirst : bool, default False
            DD/MM format dates, international and European format.
        cache_dates : bool, default True
            If True, use a cache of unique, converted dates to apply the datetime
            conversion. May produce significant speed-up when parsing duplicate
            date strings, especially ones with timezone offsets.

            .. versionadded:: 0.25.0
        iterator : bool, default False
            Return TextFileReader object for iteration or getting chunks with
            ``get_chunk()``.

            .. versionchanged:: 1.2

               ``TextFileReader`` is a context manager.
        chunksize : int, optional
            Return TextFileReader object for iteration.
            See the `IO Tools docs
            <https://pandas.pydata.org/pandas-docs/stable/io.html#io-chunking>`_
            for more information on ``iterator`` and ``chunksize``.

            .. versionchanged:: 1.2

               ``TextFileReader`` is a context manager.
        compression : str or dict, default 'infer'
            For on-the-fly decompression of on-disk data. If 'infer' and '%s' is
            path-like, then detect compression from the following extensions: '.gz',
            '.bz2', '.zip', '.xz', or '.zst' (otherwise no compression). If using
            'zip', the ZIP file must contain only one data file to be read in. Set to
            ``None`` for no decompression. Can also be a dict with key ``'method'`` set
            to one of {``'zip'``, ``'gzip'``, ``'bz2'``, ``'zstd'``} and other
            key-value pairs are forwarded to ``zipfile.ZipFile``, ``gzip.GzipFile``,
            ``bz2.BZ2File``, or ``zstandard.ZstdDecompressor``, respectively. As an
            example, the following could be passed for Zstandard decompression using a
            custom compression dictionary:
            ``compression={'method': 'zstd', 'dict_data': my_compression_dict}``.

            .. versionchanged:: 1.4.0 Zstandard support.

        thousands : str, optional
            Thousands separator.
        decimal : str, default '.'
            Character to recognize as decimal point (e.g. use ',' for European data).
        lineterminator : str (length 1), optional
            Character to break file into lines. Only valid with C parser.
        quotechar : str (length 1), optional
            The character used to denote the start and end of a quoted item. Quoted
            items can include the delimiter and it will be ignored.
        quoting : int or csv.QUOTE_* instance, default 0
            Control field quoting behavior per ``csv.QUOTE_*`` constants. Use one of
            QUOTE_MINIMAL (0), QUOTE_ALL (1), QUOTE_NONNUMERIC (2) or QUOTE_NONE (3).
        doublequote : bool, default ``True``
           When quotechar is specified and quoting is not ``QUOTE_NONE``, indicate
           whether or not to interpret two consecutive quotechar elements INSIDE a
           field as a single ``quotechar`` element.
        escapechar : str (length 1), optional
            One-character string used to escape other characters.
        comment : str, optional
            Indicates remainder of line should not be parsed. If found at the beginning
            of a line, the line will be ignored altogether. This parameter must be a
            single character. Like empty lines (as long as ``skip_blank_lines=True``),
            fully commented lines are ignored by the parameter `header` but not by
            `skiprows`. For example, if ``comment='#'``, parsing
            ``#empty\na,b,c\n1,2,3`` with ``header=0`` will result in 'a,b,c' being
            treated as the header.
        encoding : str, optional
            Encoding to use for UTF when reading/writing (ex. 'utf-8'). `List of Python
            standard encodings
            <https://docs.python.org/3/library/codecs.html#standard-encodings>`_ .

            .. versionchanged:: 1.2

               When ``encoding`` is ``None``, ``errors="replace"`` is passed to
               ``open()``. Otherwise, ``errors="strict"`` is passed to ``open()``.
               This behavior was previously only the case for ``engine="python"``.

            .. versionchanged:: 1.3.0

               ``encoding_errors`` is a new argument. ``encoding`` has no longer an
               influence on how encoding errors are handled.

        encoding_errors : str, optional, default "strict"
            How encoding errors are treated. `List of possible values
            <https://docs.python.org/3/library/codecs.html#error-handlers>`_ .

            .. versionadded:: 1.3.0

        dialect : str or csv.Dialect, optional
            If provided, this parameter will override values (default or not) for the
            following parameters: `delimiter`, `doublequote`, `escapechar`,
            `skipinitialspace`, `quotechar`, and `quoting`. If it is necessary to
            override values, a ParserWarning will be issued. See csv.Dialect
            documentation for more details.
        error_bad_lines : bool, optional, default ``None``
            Lines with too many fields (e.g. a csv line with too many commas) will by
            default cause an exception to be raised, and no DataFrame will be returned.
            If False, then these "bad lines" will be dropped from the DataFrame that is
            returned.

            .. deprecated:: 1.3.0
               The ``on_bad_lines`` parameter should be used instead to specify behavior upon
               encountering a bad line instead.
        warn_bad_lines : bool, optional, default ``None``
            If error_bad_lines is False, and warn_bad_lines is True, a warning for each
            "bad line" will be output.

            .. deprecated:: 1.3.0
               The ``on_bad_lines`` parameter should be used instead to specify behavior upon
               encountering a bad line instead.
        on_bad_lines : {'error', 'warn', 'skip'} or callable, default 'error'
            Specifies what to do upon encountering a bad line (a line with too many fields).
            Allowed values are :

                - 'error', raise an Exception when a bad line is encountered.
                - 'warn', raise a warning when a bad line is encountered and skip that line.
                - 'skip', skip bad lines without raising or warning when they are encountered.

            .. versionadded:: 1.3.0

                - callable, function with signature
                  ``(bad_line: list[str]) -> list[str] | None`` that will process a single
                  bad line. ``bad_line`` is a list of strings split by the ``sep``.
                  If the function returns ``None``, the bad line will be ignored.
                  If the function returns a new list of strings with more elements than
                  expected, a ``ParserWarning`` will be emitted while dropping extra elements.
                  Only supported when ``engine="python"``

            .. versionadded:: 1.4.0

        delim_whitespace : bool, default False
            Specifies whether or not whitespace (e.g. ``' '`` or ``'    '``) will be
            used as the sep. Equivalent to setting ``sep='\s+'``. If this option
            is set to True, nothing should be passed in for the ``delimiter``
            parameter.
        low_memory : bool, default True
            Internally process the file in chunks, resulting in lower memory use
            while parsing, but possibly mixed type inference.  To ensure no mixed
            types either set False, or specify the type with the `dtype` parameter.
            Note that the entire file is read into a single DataFrame regardless,
            use the `chunksize` or `iterator` parameter to return the data in chunks.
            (Only valid with C parser).
        memory_map : bool, default False
            If a filepath is provided for `filepath_or_buffer`, map the file object
            directly onto memory and access the data directly from there. Using this
            option can improve performance because there is no longer any I/O overhead.
        float_precision : str, optional
            Specifies which converter the C engine should use for floating-point
            values. The options are ``None`` or 'high' for the ordinary converter,
            'legacy' for the original lower precision pandas converter, and
            'round_trip' for the round-trip converter.

            .. versionchanged:: 1.2

        storage_options : dict, optional
            Extra options that make sense for a particular storage connection, e.g.
            host, port, username, password, etc. For HTTP(S) URLs the key-value pairs
            are forwarded to ``urllib`` as header options. For other URLs (e.g.
            starting with "s3://", and "gcs://") the key-value pairs are forwarded to
            ``fsspec``. Please see ``fsspec`` and ``urllib`` for more details.

            .. versionadded:: 1.2

        Returns
        -------
        DataFrame or TextParser
            A comma-separated values (csv) file is returned as two-dimensional
            data structure with labeled axes.

        See Also
        --------
        DataFrame.to_csv : Write DataFrame to a comma-separated values (csv) file.
        read_csv : Read a comma-separated values (csv) file into DataFrame.
        read_fwf : Read a table of fixed-width formatted lines into DataFrame.

        Examples
        --------
        >>> pd.read_csv('data.csv')  # doctest: +SKIP

```python
sample_df = pd.read_csv(sample_table_url, sep="\t")
library_df = pd.read_csv(library_table_url, sep="\t")
```

```python
sample_df.project_name.nunique()
```

    45

```python
library_df.project_name.nunique()
```

    43

###### Listing the columns of the sample dataframe

```python
sample_df.columns
```

    Index(['project_name', 'publication_year', 'publication_doi', 'site_name',
           'latitude', 'longitude', 'geo_loc_name', 'sample_name', 'sample_host',
           'sample_age', 'sample_age_doi', 'community_type', 'material', 'archive',
           'archive_project', 'archive_accession'],
          dtype='object')

###### Looking at the data type of the sample dataframe

```python
sample_df.dtypes
```

    project_name          object
    publication_year       int64
    publication_doi       object
    site_name             object
    latitude             float64
    longitude            float64
    geo_loc_name          object
    sample_name           object
    sample_host           object
    sample_age             int64
    sample_age_doi        object
    community_type        object
    material              object
    archive               object
    archive_project       object
    archive_accession     object
    dtype: object

- `int64` is for integers
- `floating64` is for floating point precision numbers, also known as double in some other programing languages
- `object` is a general type in pandas for everything that is not a number, interval, categorical, or date

###### Let's inspect our data

What is the size of our dataframe ?

```python
sample_df.shape
```

    (1060, 16)

This dataframe has **1060** rows, and **16** columns

Let's look at the first 5 rows

```python
sample_df.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Gola Forest</td>
      <td>7.657</td>
      <td>-10.841</td>
      <td>Sierra Leone</td>
      <td>Chimp</td>
      <td>Pan troglodytes</td>
      <td>100</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890499</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.328</td>
      <td>Spain</td>
      <td>ElSidron1</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890498</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.329</td>
      <td>Spain</td>
      <td>ElSidron2</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890496</td>
    </tr>
  </tbody>
</table>
</div>

**Unlike R, Python is `0` based language, meaning the first element is of index `0`, not like R where it is `1`.**

Let's look at the last 5 rows

```python
sample_df.tail()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1055</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T2</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283094,ERS7283095</td>
    </tr>
    <tr>
      <th>1056</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283096,ERS7283097</td>
    </tr>
    <tr>
      <th>1057</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283098,ERS7283099</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>Dom Square, Riga</td>
      <td>56.949</td>
      <td>24.104</td>
      <td>Latvia</td>
      <td>TZA3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283100,ERS7283101</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Peter’s Church, Riga</td>
      <td>56.947</td>
      <td>24.109</td>
      <td>Latvia</td>
      <td>TZA4</td>
      <td>Homo sapiens</td>
      <td>500</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283102,ERS7283103</td>
    </tr>
  </tbody>
</table>
</div>

Let's randomly inspect 5 rows

```python
sample_df.sample(n=5)
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>413</th>
      <td>Neukamm2020</td>
      <td>2020</td>
      <td>10.1186/s12915-020-00839-8</td>
      <td>Abusir el-Meleq</td>
      <td>29.240</td>
      <td>31.100</td>
      <td>Egypt</td>
      <td>Abusir1576</td>
      <td>Homo sapiens</td>
      <td>2200</td>
      <td>10.1038/ncomms15694</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>ENA</td>
      <td>PRJEB33848</td>
      <td>ERS3635981</td>
    </tr>
    <tr>
      <th>754</th>
      <td>Rampelli2021</td>
      <td>2021</td>
      <td>10.1038/s42003-021-01689-y</td>
      <td>El Salt</td>
      <td>38.687</td>
      <td>-0.508</td>
      <td>Spain</td>
      <td>V3</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>44700</td>
      <td>10.1038/s42003-021-01689-y</td>
      <td>gut</td>
      <td>sediment</td>
      <td>ENA</td>
      <td>PRJEB41665</td>
      <td>ERS5428042</td>
    </tr>
    <tr>
      <th>436</th>
      <td>Neukamm2020</td>
      <td>2020</td>
      <td>10.1186/s12915-020-00839-8</td>
      <td>Abusir el-Meleq</td>
      <td>29.240</td>
      <td>31.100</td>
      <td>Egypt</td>
      <td>Abusir1606</td>
      <td>Homo sapiens</td>
      <td>2600</td>
      <td>10.1186/s12915-020-00839-8</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>ENA</td>
      <td>PRJEB33848</td>
      <td>ERS3635928</td>
    </tr>
    <tr>
      <th>474</th>
      <td>Neukamm2020</td>
      <td>2020</td>
      <td>10.1186/s12915-020-00839-8</td>
      <td>Abusir el-Meleq</td>
      <td>29.240</td>
      <td>31.100</td>
      <td>Egypt</td>
      <td>Abusir1654</td>
      <td>Homo sapiens</td>
      <td>2300</td>
      <td>10.1038/ncomms15694</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB33848</td>
      <td>ERS3635960</td>
    </tr>
    <tr>
      <th>573</th>
      <td>Philips2017</td>
      <td>2017</td>
      <td>10.1186/s12864-020-06810-9</td>
      <td>Kowalewko</td>
      <td>52.699</td>
      <td>17.605</td>
      <td>Poland</td>
      <td>PCA0040</td>
      <td>Homo sapiens</td>
      <td>1900</td>
      <td>10.1186/s12864-020-06810-9</td>
      <td>oral</td>
      <td>tooth</td>
      <td>SRA</td>
      <td>PRJNA354503</td>
      <td>SRS1815407</td>
    </tr>
  </tbody>
</table>
</div>

###### Accessing the data by index/columns

The are different way of selecting of subset of a dataframe

Selecting by the row index

```python
# selecting the 10th row, and all columns
sample_df.iloc[9, :]
```

    project_name                    Weyrich2017
    publication_year                       2017
    publication_doi         10.1038/nature21674
    site_name            Stuttgart-Mühlhausen I
    latitude                             48.839
    longitude                             9.227
    geo_loc_name                        Germany
    sample_name                        EuroLBK1
    sample_host                    Homo sapiens
    sample_age                             7400
    sample_age_doi          10.1038/nature21674
    community_type                         oral
    material                    dental calculus
    archive                                 SRA
    archive_project                 PRJNA685265
    archive_accession                SRS7890488
    Name: 9, dtype: object

```python
# selecting the 10th to 12th row, and all columns
sample_df.iloc[9:12, :]
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
      <td>48.839</td>
      <td>9.227</td>
      <td>Germany</td>
      <td>EuroLBK1</td>
      <td>Homo sapiens</td>
      <td>7400</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890488</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
      <td>48.839</td>
      <td>9.227</td>
      <td>Germany</td>
      <td>EuroLBK2</td>
      <td>Homo sapiens</td>
      <td>7400</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890485</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
      <td>48.839</td>
      <td>9.227</td>
      <td>Germany</td>
      <td>EuroLBK3</td>
      <td>Homo sapiens</td>
      <td>7400</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890490</td>
    </tr>
  </tbody>
</table>
</div>

```python
# selecting the 10th to 12th row, and the first to the 4th column
sample_df.iloc[9:12, 0:4]
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Stuttgart-Mühlhausen I</td>
    </tr>
  </tbody>
</table>
</div>

```python
# selecting the column site_name
sample_df['site_name']
```

    0                           Dalheim
    1                           Dalheim
    2                       Gola Forest
    3                    El Sidrón Cave
    4                    El Sidrón Cave
                       ...
    1055    St. Gertrude’s Church, Riga
    1056    St. Gertrude’s Church, Riga
    1057    St. Gertrude’s Church, Riga
    1058               Dom Square, Riga
    1059       St. Peter’s Church, Riga
    Name: site_name, Length: 1060, dtype: object

```python
# Also valid, but less preferred
sample_df.site_name
```

    0                           Dalheim
    1                           Dalheim
    2                       Gola Forest
    3                    El Sidrón Cave
    4                    El Sidrón Cave
                       ...
    1055    St. Gertrude’s Church, Riga
    1056    St. Gertrude’s Church, Riga
    1057    St. Gertrude’s Church, Riga
    1058               Dom Square, Riga
    1059       St. Peter’s Church, Riga
    Name: site_name, Length: 1060, dtype: object

```python
# Removing a row
sample_df.drop(0)
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Gola Forest</td>
      <td>7.657</td>
      <td>-10.841</td>
      <td>Sierra Leone</td>
      <td>Chimp</td>
      <td>Pan troglodytes</td>
      <td>100</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890499</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.328</td>
      <td>Spain</td>
      <td>ElSidron1</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890498</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.329</td>
      <td>Spain</td>
      <td>ElSidron2</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890496</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Weyrich2017</td>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Spy Cave</td>
      <td>50.480</td>
      <td>4.674</td>
      <td>Belgium</td>
      <td>Spy1</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>35800</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890491</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1055</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T2</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283094,ERS7283095</td>
    </tr>
    <tr>
      <th>1056</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283096,ERS7283097</td>
    </tr>
    <tr>
      <th>1057</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283098,ERS7283099</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>Dom Square, Riga</td>
      <td>56.949</td>
      <td>24.104</td>
      <td>Latvia</td>
      <td>TZA3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283100,ERS7283101</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Peter’s Church, Riga</td>
      <td>56.947</td>
      <td>24.109</td>
      <td>Latvia</td>
      <td>TZA4</td>
      <td>Homo sapiens</td>
      <td>500</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283102,ERS7283103</td>
    </tr>
  </tbody>
</table>
<p>1059 rows × 16 columns</p>
</div>

```python
# Removing a columm
sample_df.drop('project_name', axis=1)
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>Gola Forest</td>
      <td>7.657</td>
      <td>-10.841</td>
      <td>Sierra Leone</td>
      <td>Chimp</td>
      <td>Pan troglodytes</td>
      <td>100</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890499</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.328</td>
      <td>Spain</td>
      <td>ElSidron1</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890498</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2017</td>
      <td>10.1038/nature21674</td>
      <td>El Sidrón Cave</td>
      <td>43.386</td>
      <td>-5.329</td>
      <td>Spain</td>
      <td>ElSidron2</td>
      <td>Homo sapiens neanderthalensis</td>
      <td>49000</td>
      <td>10.1038/nature21674</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA685265</td>
      <td>SRS7890496</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1055</th>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T2</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283094,ERS7283095</td>
    </tr>
    <tr>
      <th>1056</th>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283096,ERS7283097</td>
    </tr>
    <tr>
      <th>1057</th>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283098,ERS7283099</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>Dom Square, Riga</td>
      <td>56.949</td>
      <td>24.104</td>
      <td>Latvia</td>
      <td>TZA3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283100,ERS7283101</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Peter’s Church, Riga</td>
      <td>56.947</td>
      <td>24.109</td>
      <td>Latvia</td>
      <td>TZA4</td>
      <td>Homo sapiens</td>
      <td>500</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283102,ERS7283103</td>
    </tr>
  </tbody>
</table>
<p>1060 rows × 15 columns</p>
</div>

##### 4 - Dealing with missing data

Checking is some entries if the table have missing data (NA or NaN)

```python
sample_df.isna()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1055</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1056</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1057</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>1060 rows × 16 columns</p>
</div>

```python
# making the sum by row - axis=1
sample_df.isna().sum(axis=1)
```

    0       0
    1       0
    2       0
    3       0
    4       0
           ..
    1055    0
    1056    0
    1057    0
    1058    0
    1059    0
    Length: 1060, dtype: int64

Sorting by decreasing order to check which rows have missing values

```python
sample_df.isna().sum(axis=1).sort_values(ascending=False)
```

    800     2
    962     2
    992     2
    801     2
    802     2
           ..
    362     0
    363     0
    364     0
    365     0
    1059    0
    Length: 1060, dtype: int64

```python
sample_df.iloc[800,:]
```

    project_name                         FellowsYates2021
    publication_year                                 2021
    publication_doi               10.1073/pnas.2021655118
    site_name                               Not specified
    latitude                                          NaN
    longitude                                         NaN
    geo_loc_name         Democratic Republic of the Congo
    sample_name                                  GDC002.A
    sample_host                   Gorilla gorilla gorilla
    sample_age                                        200
    sample_age_doi                10.1073/pnas.2021655118
    community_type                                   oral
    material                              dental calculus
    archive                                           ENA
    archive_project                            PRJEB34569
    archive_accession                          ERS3774403
    Name: 800, dtype: object

What to do now ? The ideal scenario would be to correct or impute the data.  
However, sometimes, the only thing we can do is remove the row with missing data, with the `.dropna() function`.  
Here, we're just going to ignore them, and deal with it individually if necessary

##### 5 - Computing basic statistics

TLDR: use the `describe()` function, the equivalent of `summarize` in R

```python
sample_df.describe()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>publication_year</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>sample_age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>1060.000000</td>
      <td>1021.000000</td>
      <td>1021.000000</td>
      <td>1060.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2019.377358</td>
      <td>40.600493</td>
      <td>3.749624</td>
      <td>3588.443396</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.633877</td>
      <td>18.469421</td>
      <td>43.790316</td>
      <td>9862.416855</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2014.000000</td>
      <td>-34.030000</td>
      <td>-121.800000</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2018.000000</td>
      <td>29.240000</td>
      <td>-1.257000</td>
      <td>200.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2020.000000</td>
      <td>45.450000</td>
      <td>14.381000</td>
      <td>1000.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2021.000000</td>
      <td>52.699000</td>
      <td>23.892000</td>
      <td>2200.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2021.000000</td>
      <td>79.000000</td>
      <td>159.346000</td>
      <td>102000.000000</td>
    </tr>
  </tbody>
</table>
</div>

Let's look at various individual summary statistics
We can run them on the whole dataframe (for `int` or `float` columns), or on a subset of columns

```python
sample_df.mean()
```

    /var/folders/1c/l1qb09f15jddsh65f6xv1n_r0000gp/T/ipykernel_69168/2260452167.py:1:
    FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None')
    is deprecated; in a future version this will raise TypeError.  Select only valid columns
    before calling the reduction.





    publication_year    2019.377358
    latitude              40.600493
    longitude              3.749624
    sample_age          3588.443396
    dtype: float64

```python
sample_df['publication_year'].describe()
```

    count    1060.000000
    mean     2019.377358
    std         1.633877
    min      2014.000000
    25%      2018.000000
    50%      2020.000000
    75%      2021.000000
    max      2021.000000
    Name: publication_year, dtype: float64

```python
# The average publication year
sample_df['publication_year'].mean()
```

    2019.377358490566

```python
# The median publication year
sample_df['publication_year'].median()
```

    2020.0

```python
# The minimum, or oldest publication year
sample_df['publication_year'].min()
```

    2014

```python
# The maximum, or most recent publication year
sample_df['publication_year'].max()
```

    2021

```python
# The number of sites
sample_df['site_name'].nunique()
```

    246

```python
# The number of samples from the different hosts
sample_df['sample_host'].value_counts()
```

    Homo sapiens                      741
    Ursus arctos                       85
    Ambrosia artemisiifolia            46
    Arabidopsis thaliana               34
    Homo sapiens neanderthalensis      32
    Pan troglodytes schweinfurthii     26
    Gorilla beringei beringei          15
    Canis lupus                        12
    Gorilla gorilla gorilla             8
    Mammuthus primigenius               8
    Pan troglodytes verus               7
    Rangifer tarandus                   6
    Gorilla beringei graueri            6
    Pan troglodytes ellioti             6
    Papio hamadryas                     5
    Alouatta palliata                   5
    Conepatus chinga                    4
    Gerbilliscus boehmi                 4
    Strigocuscus celebensis             4
    Papio anubis                        2
    Gorilla beringei                    2
    Papio sp.                           1
    Pan troglodytes                     1
    Name: sample_host, dtype: int64

```python
# The quantile of the publication years
sample_df['publication_year'].quantile(np.arange(0,1,0.1))
```

    0.0    2014.0
    0.1    2017.0
    0.2    2018.0
    0.3    2018.0
    0.4    2020.0
    0.5    2020.0
    0.6    2020.0
    0.7    2021.0
    0.8    2021.0
    0.9    2021.0
    Name: publication_year, dtype: float64

```python
# We can also visualize it with built-in plot functions of pandas
sample_df['publication_year'].plot.hist()
```

    <AxesSubplot:ylabel='Frequency'>

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/tutorial_files/tutorial_74_1.png)

##### 6 - Filtering

There are different ways of filtering data with Pandas:

- The **classic** method with bracket indexing/subsetting
- The `query()` method

The classic method

```python
# Getting all the publications before 2015
sample_df[sample_df['publication_year']  < 2015 ]
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>272</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP4</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428959</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP10</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428961</td>
    </tr>
    <tr>
      <th>274</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP18</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428962</td>
    </tr>
    <tr>
      <th>275</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP37</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428963</td>
    </tr>
    <tr>
      <th>276</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428960</td>
    </tr>
    <tr>
      <th>277</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP48</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428964</td>
    </tr>
    <tr>
      <th>278</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP02,TP10,TP15,TP26</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428958</td>
    </tr>
    <tr>
      <th>279</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP32,TP42,TP45,TP48</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428972</td>
    </tr>
    <tr>
      <th>500</th>
      <td>Appelt2014</td>
      <td>2014</td>
      <td>10.1128/AEM.03242-13</td>
      <td>Place d'Armes, Namur</td>
      <td>50.460</td>
      <td>4.86</td>
      <td>Belgium</td>
      <td>4.453</td>
      <td>Homo sapiens</td>
      <td>600</td>
      <td>10.1128/AEM.03242-13</td>
      <td>gut</td>
      <td>palaeofaeces</td>
      <td>SRA</td>
      <td>PRJNA230469</td>
      <td>SRS510175</td>
    </tr>
  </tbody>
</table>
</div>

```python
# Getting all the publications before 2015, only in the Northern hemisphere
sample_df[(sample_df['publication_year']  < 2015) & (sample_df['longitude'] > 0)]
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>500</th>
      <td>Appelt2014</td>
      <td>2014</td>
      <td>10.1128/AEM.03242-13</td>
      <td>Place d'Armes, Namur</td>
      <td>50.460</td>
      <td>4.86</td>
      <td>Belgium</td>
      <td>4.453</td>
      <td>Homo sapiens</td>
      <td>600</td>
      <td>10.1128/AEM.03242-13</td>
      <td>gut</td>
      <td>palaeofaeces</td>
      <td>SRA</td>
      <td>PRJNA230469</td>
      <td>SRS510175</td>
    </tr>
  </tbody>
</table>
</div>

This syntax can rapidly become quite cumbersome, which is why we can also use the `query()` method

```python
# Getting all the publications before 2015
sample_df.query("publication_year < 2015")
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>272</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP4</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428959</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP10</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428961</td>
    </tr>
    <tr>
      <th>274</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP18</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428962</td>
    </tr>
    <tr>
      <th>275</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP37</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428963</td>
    </tr>
    <tr>
      <th>276</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428960</td>
    </tr>
    <tr>
      <th>277</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP48</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428964</td>
    </tr>
    <tr>
      <th>278</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP02,TP10,TP15,TP26</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428958</td>
    </tr>
    <tr>
      <th>279</th>
      <td>Campana2014</td>
      <td>2014</td>
      <td>10.1186/1756-0500-7-111</td>
      <td>Teposcolula Yucundaa</td>
      <td>17.490</td>
      <td>-97.46</td>
      <td>Mexico</td>
      <td>TP32,TP42,TP45,TP48</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.7183/1045-6635.23.4.467</td>
      <td>skeletal tissue</td>
      <td>bone</td>
      <td>SRA</td>
      <td>PRJNA205039</td>
      <td>SRS428972</td>
    </tr>
    <tr>
      <th>500</th>
      <td>Appelt2014</td>
      <td>2014</td>
      <td>10.1128/AEM.03242-13</td>
      <td>Place d'Armes, Namur</td>
      <td>50.460</td>
      <td>4.86</td>
      <td>Belgium</td>
      <td>4.453</td>
      <td>Homo sapiens</td>
      <td>600</td>
      <td>10.1128/AEM.03242-13</td>
      <td>gut</td>
      <td>palaeofaeces</td>
      <td>SRA</td>
      <td>PRJNA230469</td>
      <td>SRS510175</td>
    </tr>
  </tbody>
</table>
</div>

```python
# Getting all the publications before 2015, only the Northern hemisphere
sample_df.query("publication_year < 2015 and longitude > 0 ")
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742,SRS473743,SRS473744,SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747,SRS473746,SRS473748,SRS473749,SRS473750</td>
    </tr>
    <tr>
      <th>500</th>
      <td>Appelt2014</td>
      <td>2014</td>
      <td>10.1128/AEM.03242-13</td>
      <td>Place d'Armes, Namur</td>
      <td>50.460</td>
      <td>4.86</td>
      <td>Belgium</td>
      <td>4.453</td>
      <td>Homo sapiens</td>
      <td>600</td>
      <td>10.1128/AEM.03242-13</td>
      <td>gut</td>
      <td>palaeofaeces</td>
      <td>SRA</td>
      <td>PRJNA230469</td>
      <td>SRS510175</td>
    </tr>
  </tbody>
</table>
</div>

##### 7 - GroupBy operations, and computing statistics on grouped values

The "groupBy" operation, as the name suggests, allows us to group values by a grouping key, and perform a groupwise operation.  
For example, we can group by the `sample_host` and get the age of the **youngest** sample in each group

```python
sample_df.groupby("sample_host")['sample_age'].min()
```

    sample_host
    Alouatta palliata                   200
    Ambrosia artemisiifolia             100
    Arabidopsis thaliana                100
    Canis lupus                         400
    Conepatus chinga                    100
    Gerbilliscus boehmi                 100
    Gorilla beringei                    100
    Gorilla beringei beringei           200
    Gorilla beringei graueri            200
    Gorilla gorilla gorilla             200
    Homo sapiens                        100
    Homo sapiens neanderthalensis     35800
    Mammuthus primigenius             41800
    Pan troglodytes                     100
    Pan troglodytes ellioti             200
    Pan troglodytes schweinfurthii      100
    Pan troglodytes verus               200
    Papio anubis                        100
    Papio hamadryas                     100
    Papio sp.                           100
    Rangifer tarandus                   100
    Strigocuscus celebensis             100
    Ursus arctos                        100
    Name: sample_age, dtype: int64

Here `min()` is a so-called aggregation function

![](img/groupby.png)

Notice that `.value_counts()` is actually a special case of `.groupby()`

```python
sample_df.groupby("sample_host")["sample_host"].count()
```

    sample_host
    Alouatta palliata                   5
    Ambrosia artemisiifolia            46
    Arabidopsis thaliana               34
    Canis lupus                        12
    Conepatus chinga                    4
    Gerbilliscus boehmi                 4
    Gorilla beringei                    2
    Gorilla beringei beringei          15
    Gorilla beringei graueri            6
    Gorilla gorilla gorilla             8
    Homo sapiens                      741
    Homo sapiens neanderthalensis      32
    Mammuthus primigenius               8
    Pan troglodytes                     1
    Pan troglodytes ellioti             6
    Pan troglodytes schweinfurthii     26
    Pan troglodytes verus               7
    Papio anubis                        2
    Papio hamadryas                     5
    Papio sp.                           1
    Rangifer tarandus                   6
    Strigocuscus celebensis             4
    Ursus arctos                       85
    Name: sample_host, dtype: int64

##### 8 - Reshaping data, from wide to long and back

<img src="https://www.researchgate.net/publication/332048735/figure/fig1/AS:741418188406792@1553779279709/The-wide-versus-tidy-data-format-In-the-wide-spreadsheet-like-data-format-each-column.png" width="600">

###### From wide to long/tidy

The tidy format, or long format idea is that one column = one kind of data.  
Unfortunately for this tutorial, the AncientMetagenomeDir tables are already in the tidy format (good), so we'll see an example or the wide format just below

```python
wide_df = pd.DataFrame(
    [
    [150,155,157,160],
    [149,153,154,155]
    ]
    , index = ['John','Jack']
    , columns = [1991,1992,1993, 1994]
).rename_axis('individual').reset_index()
wide_df
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>individual</th>
      <th>1991</th>
      <th>1992</th>
      <th>1993</th>
      <th>1994</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>John</td>
      <td>150</td>
      <td>155</td>
      <td>157</td>
      <td>160</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jack</td>
      <td>149</td>
      <td>153</td>
      <td>154</td>
      <td>155</td>
    </tr>
  </tbody>
</table>
</div>

In this hypothetic dataframe, we have the years as column, the individual as index, and their height as value.  
We'll reformat to the tidy/long format using the `.melt()` function

```python
tidy_df = wide_df.melt(id_vars='individual', var_name='birthyear', value_name='height')
tidy_df
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>individual</th>
      <th>birthyear</th>
      <th>height</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>John</td>
      <td>1991</td>
      <td>150</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jack</td>
      <td>1991</td>
      <td>149</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John</td>
      <td>1992</td>
      <td>155</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Jack</td>
      <td>1992</td>
      <td>153</td>
    </tr>
    <tr>
      <th>4</th>
      <td>John</td>
      <td>1993</td>
      <td>157</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Jack</td>
      <td>1993</td>
      <td>154</td>
    </tr>
    <tr>
      <th>6</th>
      <td>John</td>
      <td>1994</td>
      <td>160</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Jack</td>
      <td>1994</td>
      <td>155</td>
    </tr>
  </tbody>
</table>
</div>

> Bonus: How to deal with a dataframe with the kind of data indicated in the column name, typically like so

```python
wide_df = pd.DataFrame(
    [
    [150,155,157,160],
    [149,153,154,155]
    ]
    , index = ['John','Jack']
    , columns = ["year-1991","year-1992","year-1993", "year-1994"]
).rename_axis('individual').reset_index()
wide_df
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>individual</th>
      <th>year-1991</th>
      <th>year-1992</th>
      <th>year-1993</th>
      <th>year-1994</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>John</td>
      <td>150</td>
      <td>155</td>
      <td>157</td>
      <td>160</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jack</td>
      <td>149</td>
      <td>153</td>
      <td>154</td>
      <td>155</td>
    </tr>
  </tbody>
</table>
</div>

```python
pd.wide_to_long(wide_df, ['year'], i='individual', j='birthyear', sep="-").rename(columns={'year':'height'})
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>height</th>
    </tr>
    <tr>
      <th>individual</th>
      <th>birthyear</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>John</th>
      <th>1991</th>
      <td>150</td>
    </tr>
    <tr>
      <th>Jack</th>
      <th>1991</th>
      <td>149</td>
    </tr>
    <tr>
      <th>John</th>
      <th>1992</th>
      <td>155</td>
    </tr>
    <tr>
      <th>Jack</th>
      <th>1992</th>
      <td>153</td>
    </tr>
    <tr>
      <th>John</th>
      <th>1993</th>
      <td>157</td>
    </tr>
    <tr>
      <th>Jack</th>
      <th>1993</th>
      <td>154</td>
    </tr>
    <tr>
      <th>John</th>
      <th>1994</th>
      <td>160</td>
    </tr>
    <tr>
      <th>Jack</th>
      <th>1994</th>
      <td>155</td>
    </tr>
  </tbody>
</table>
</div>

###### From long/tidy to wide format using the `.pivot()` function.

```python
tidy_df.pivot(index='individual', columns='birthyear', values='height')
```

    /Users/maxime/mambaforge/envs/intro-data/lib/python3.10/site-packages/pandas/core/algorithms.py:798: FutureWarning: In a future version, the Index constructor will not infer numeric dtypes when passed object-dtype sequences (matching Series behavior)

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>birthyear</th>
      <th>1991</th>
      <th>1992</th>
      <th>1993</th>
      <th>1994</th>
    </tr>
    <tr>
      <th>individual</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Jack</th>
      <td>149</td>
      <td>153</td>
      <td>154</td>
      <td>155</td>
    </tr>
    <tr>
      <th>John</th>
      <td>150</td>
      <td>155</td>
      <td>157</td>
      <td>160</td>
    </tr>
  </tbody>
</table>
</div>

##### 9 - Joining two different tables

In AncientMetagenomeDir, the information about each sample is located in sample table, and about the library in the library table.  
To match these two together, we need to join the tables together.

To do so, we need a column in common between the two tables, the so-called **joining key** (this key can be the index)

![](https://pandas.pydata.org/docs/_images/08_merge_left.svg)

For the samples and libraries dataframe, the joining key is the column `sample_name`

```python
sample_df.merge(library_df, on='sample_name').columns
```

    Index(['project_name_x', 'publication_year_x', 'publication_doi', 'site_name',
           'latitude', 'longitude', 'geo_loc_name', 'sample_name', 'sample_host',
           'sample_age', 'sample_age_doi', 'community_type', 'material',
           'archive_x', 'archive_project_x', 'archive_accession', 'project_name_y',
           'publication_year_y', 'data_publication_doi', 'archive_y',
           'archive_project_y', 'archive_sample_accession', 'library_name',
           'strand_type', 'library_polymerase', 'library_treatment',
           'library_concentration', 'instrument_model', 'library_layout',
           'library_strategy', 'read_count', 'archive_data_accession',
           'download_links', 'download_md5s', 'download_sizes'],
          dtype='object')

We have some duplicate columns that we can get rid of:

```python
merged_df = sample_df.merge(library_df.drop(['project_name', 'publication_year', 'archive_project', 'archive'], axis=1), on='sample_name')
merged_df
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>...</th>
      <th>library_treatment</th>
      <th>library_concentration</th>
      <th>instrument_model</th>
      <th>library_layout</th>
      <th>library_strategy</th>
      <th>read_count</th>
      <th>archive_data_accession</th>
      <th>download_links</th>
      <th>download_md5s</th>
      <th>download_sizes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2000</td>
      <td>SINGLE</td>
      <td>WGS</td>
      <td>13228381</td>
      <td>SRR957738</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/SRR957/SRR957738/...</td>
      <td>9c40c43b5d455e760ae8db924347f0b2</td>
      <td>953396663</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2000</td>
      <td>SINGLE</td>
      <td>WGS</td>
      <td>13260566</td>
      <td>SRR957739</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/SRR957/SRR957739/...</td>
      <td>dec1507f742de109529638bf00e0732f</td>
      <td>1026825795</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2000</td>
      <td>SINGLE</td>
      <td>WGS</td>
      <td>8869866</td>
      <td>SRR957740</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/SRR957/SRR957740/...</td>
      <td>bc49c59f489b4009206f8abcb737d55d</td>
      <td>661500786</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2000</td>
      <td>SINGLE</td>
      <td>WGS</td>
      <td>11275013</td>
      <td>SRR957741</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/SRR957/SRR957741/...</td>
      <td>e02e3549ddd3ba6dc278a7f573c07321</td>
      <td>877360302</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.84</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2000</td>
      <td>SINGLE</td>
      <td>WGS</td>
      <td>8978974</td>
      <td>SRR957742</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/SRR957/SRR957742/...</td>
      <td>b7c620b8ee165c08bee204529341ca5b</td>
      <td>690614774</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>Maixner2021</td>
      <td>2021</td>
      <td>10.1016/j.cub.2021.09.031</td>
      <td>Edlersbergwerk - oben, Hallstatt</td>
      <td>47.560</td>
      <td>13.63</td>
      <td>Austria</td>
      <td>2612</td>
      <td>Homo sapiens</td>
      <td>150</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina MiSeq</td>
      <td>PAIRED</td>
      <td>WGS</td>
      <td>1858404</td>
      <td>ERR5766179</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/ERR576/009/ERR576...</td>
      <td>542787c645b0aeebe15c66cc926d3f69;0bc58d56be3c3...</td>
      <td>86783041;98100690</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>Maixner2021</td>
      <td>2021</td>
      <td>10.1016/j.cub.2021.09.031</td>
      <td>Edlersbergwerk - oben, Hallstatt</td>
      <td>47.560</td>
      <td>13.63</td>
      <td>Austria</td>
      <td>2612</td>
      <td>Homo sapiens</td>
      <td>150</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina MiSeq</td>
      <td>PAIRED</td>
      <td>WGS</td>
      <td>1603064</td>
      <td>ERR5766180</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/ERR576/000/ERR576...</td>
      <td>022bb28da460e66590e974b4135bdd2e;f88acec67b648...</td>
      <td>74375931;77621627</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>Maixner2021</td>
      <td>2021</td>
      <td>10.1016/j.cub.2021.09.031</td>
      <td>Edlersbergwerk - oben, Hallstatt</td>
      <td>47.560</td>
      <td>13.63</td>
      <td>Austria</td>
      <td>2612</td>
      <td>Homo sapiens</td>
      <td>150</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina MiSeq</td>
      <td>PAIRED</td>
      <td>WGS</td>
      <td>1075088</td>
      <td>ERR5766181</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/ERR576/001/ERR576...</td>
      <td>57fc575d32db14f1d5c1ed7f6a106e91;4f57b9d978b53...</td>
      <td>51852071;56288763</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>Maixner2021</td>
      <td>2021</td>
      <td>10.1016/j.cub.2021.09.031</td>
      <td>Edlersbergwerk - oben, Hallstatt</td>
      <td>47.560</td>
      <td>13.63</td>
      <td>Austria</td>
      <td>2612</td>
      <td>Homo sapiens</td>
      <td>150</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>Illumina HiSeq 2500</td>
      <td>PAIRED</td>
      <td>WGS</td>
      <td>138836358</td>
      <td>ERR5766182</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/ERR576/002/ERR576...</td>
      <td>64e63df8da7542957d1d9eb08e764d38;3fc6cba02c74d...</td>
      <td>4332353625;4420486328</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>Maixner2021</td>
      <td>2021</td>
      <td>10.1016/j.cub.2021.09.031</td>
      <td>Edlersbergwerk - oben, Hallstatt</td>
      <td>47.560</td>
      <td>13.63</td>
      <td>Austria</td>
      <td>2612</td>
      <td>Homo sapiens</td>
      <td>150</td>
      <td>...</td>
      <td>none</td>
      <td>NaN</td>
      <td>HiSeq X Ten</td>
      <td>PAIRED</td>
      <td>WGS</td>
      <td>84192332</td>
      <td>ERR5766183</td>
      <td>ftp.sra.ebi.ac.uk/vol1/fastq/ERR576/003/ERR576...</td>
      <td>43ac661c4e211ed6ee2940dcab8b13cb;88de66a85df92...</td>
      <td>3128863954;3460789287</td>
    </tr>
  </tbody>
</table>
<p>1807 rows × 31 columns</p>
</div>

##### 10 - Visualizing some of the results with Plotnine

Plotnine is the Python clone of ggplot2, the syntax is identical, which makes it great if you're working with data in tidy/long format, and are already familiar with the ggplot2 syntax

```python
ggplot(merged_df, aes(x='publication_year')) + geom_histogram() + theme_classic()
```

    /Users/maxime/mambaforge/envs/intro-data/lib/python3.10/
    site-packages/plotnine/stats/stat_bin.py:95:
    PlotnineWarning: 'stat_bin()' using 'bins = 15'. Pick better value with 'binwidth'.

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/tutorial_files/tutorial_111_1.png)

    <ggplot: (366051178)>

We can start to ask some questions, for example, is the sequencing depth increasing with the years ?

```python
merged_df['publication_year'] = merged_df['publication_year'].astype('category')
```

```python
ggplot(merged_df, aes(x='publication_year', y='np.log10(read_count)', fill='publication_year')) +
geom_jitter(alpha=0.1) + geom_boxplot(alpha=0.8) + theme_classic()
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/tutorial_files/tutorial_114_0.png)

    <ggplot: (366112582)>

We could ask the same question, but first grouping the samples by publication year

```python
avg_read_count_by_year = merged_df.groupby('publication_year')['read_count'].mean().to_frame().reset_index()
avg_read_count_by_year
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>publication_year</th>
      <th>read_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>1.437173e+07</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2016</td>
      <td>3.653450e+04</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2017</td>
      <td>5.712598e+06</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2018</td>
      <td>9.273287e+06</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2019</td>
      <td>2.211632e+07</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2020</td>
      <td>1.111819e+07</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2021</td>
      <td>2.547655e+07</td>
    </tr>
  </tbody>
</table>
</div>

```python
ggplot(avg_read_count_by_year, aes(x='publication_year', y='np.log10(read_count)', fill='publication_year')) + geom_point()
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3b2-python-pandas/tutorial_files/tutorial_117_0.png)

    <ggplot: (366206706)>

**Your turn ! Make a plot to investigate the relation between the type of library treatment throughout the publication years**

##### 11 - Bonus, dealing with ill-formatted columns

Sometimes, colums can contains entries which could be split in multiple columns, typically values separated by a comma.
In AncientMetagenomeDir, this is the case with the archive accession column.

Here is how we would solve it with pandas

```python
sample_df.assign(archive_accession = sample_df.archive_accession.str.split(",")).explode('archive_accession')
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>project_name</th>
      <th>publication_year</th>
      <th>publication_doi</th>
      <th>site_name</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>geo_loc_name</th>
      <th>sample_name</th>
      <th>sample_host</th>
      <th>sample_age</th>
      <th>sample_age_doi</th>
      <th>community_type</th>
      <th>material</th>
      <th>archive</th>
      <th>archive_project</th>
      <th>archive_accession</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473742</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473743</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473744</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>B61</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Warinner2014</td>
      <td>2014</td>
      <td>10.1038/ng.2906</td>
      <td>Dalheim</td>
      <td>51.565</td>
      <td>8.840</td>
      <td>Germany</td>
      <td>G12</td>
      <td>Homo sapiens</td>
      <td>900</td>
      <td>10.1038/ng.2906</td>
      <td>oral</td>
      <td>dental calculus</td>
      <td>SRA</td>
      <td>PRJNA216965</td>
      <td>SRS473747</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1057</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Gertrude’s Church, Riga</td>
      <td>56.958</td>
      <td>24.121</td>
      <td>Latvia</td>
      <td>T9</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283099</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>Dom Square, Riga</td>
      <td>56.949</td>
      <td>24.104</td>
      <td>Latvia</td>
      <td>TZA3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283100</td>
    </tr>
    <tr>
      <th>1058</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>Dom Square, Riga</td>
      <td>56.949</td>
      <td>24.104</td>
      <td>Latvia</td>
      <td>TZA3</td>
      <td>Homo sapiens</td>
      <td>400</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283101</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Peter’s Church, Riga</td>
      <td>56.947</td>
      <td>24.109</td>
      <td>Latvia</td>
      <td>TZA4</td>
      <td>Homo sapiens</td>
      <td>500</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283102</td>
    </tr>
    <tr>
      <th>1059</th>
      <td>Kazarina2021b</td>
      <td>2021</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>St. Peter’s Church, Riga</td>
      <td>56.947</td>
      <td>24.109</td>
      <td>Latvia</td>
      <td>TZA4</td>
      <td>Homo sapiens</td>
      <td>500</td>
      <td>10.1016/j.jasrep.2021.103213</td>
      <td>oral</td>
      <td>tooth</td>
      <td>ENA</td>
      <td>PRJEB47251</td>
      <td>ERS7283103</td>
    </tr>
  </tbody>
</table>
<p>1262 rows × 16 columns</p>
</div>

</div>

</details>

---

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

<iframe width="560" height="630" src="https://www.youtube.com/embed/zp3fmPAZnBo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>

<div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

> ⚠️ We highly recommend viewing this walkthrough via the Jupyter notebook above!
> The output of commands on the website for this walkthrough are displayed in their
> own code blocks - be wary of what you copy-paste!

#### Download and Subsample

```python
import subprocess
import glob
from pathlib import Path
```

For this tutorial, we will be using the ERR5766177 library from the sample 2612 published by [Maixner et al. 2021](https://doi.org/10.1016/j.cub.2021.09.031)

![](https://ars.els-cdn.com/content/image/1-s2.0-S0960982221012719-fx1.jpg)

![](https://ars.els-cdn.com/content/image/1-s2.0-S0960982221012719-gr1.jpg)`

##### Subsampling the sequencing files to make the analysis quicker for this tutorial

```python
def subsample(filename, outdir, depth=1000000):
    basename = Path(filename).stem
    cmd = f"seqtk sample -s42 {filename} {depth} > {outdir}/{basename}_subsample_{depth}.fastq"
    print(cmd)
    subprocess.check_output(cmd, shell=True)
```

```python
for f in glob.glob("../data/raw/*"):
    outdir = "../data/subsampled"
    subsample(f, outdir)
```

    seqtk sample -s42 ../data/raw/ERR5766177_PE.mapped.hostremoved.fwd.fq.gz 1000000 >
    ../data/subsampled/ERR5766177_PE.mapped.hostremoved.fwd.fq_subsample_1000000.fastq
    seqtk sample -s42 ../data/raw/ERR5766177_PE.mapped.hostremoved.rev.fq.gz 1000000 >
    ../data/subsampled/ERR5766177_PE.mapped.hostremoved.rev.fq_subsample_1000000.fastq

```python
! gzip -f ../data/subsampled/*.fastq
```

#### Hands on introduction to ancient microbiome analysis

Author: Maxime Borry  
Date: 12/08/2021

In this tutorial, we're going to go through the steps necessary to:

- generate a taxonomic profile table with [metaphlan v3.0](https://github.com/biobakery/MetaPhlAn)
- have a look at metaphlan results with [Pavian](https://github.com/fbreitwieser/pavian) and generate a [Krona plot](https://github.com/marbl/Krona/wiki)
- Compare the diversity of our samples vs the diversity of modern human gut samples
- Compare the composition of our samples vs modern gut samples, and see where they fit in a lower dimensional space

##### 0. Quick intro to Jupyter Notebooks

This a markdown cell

```python
print("This is a python cell")
```

    This is a python cell

```python
! echo "This is how to run a single line bash command"
```

    This is how to run a single line bash command

```bash
%%bash
echo "This how to run a multi"
echo "lines bash command"
```

    This how to run a multi
    lines bash command

##### 1. Data pre-processing

Before starting to analyze our data, we will need to pre-process them to remove reads mapping to the host genome, here, _Homo sapiens_

To do so, I've used [nf-core/eager](https://github.com/nf-core/eager)

I've already pre-processed the data, and the resulting cleaned files are available in the [data/eager_cleaned](data/eager_cleaned), but the basic eager command to do so is:

```
nextflow run nf-core/eager -profile <docker/singularity/podman/conda/institute> --input '*_R{1,2}.fastq.gz' \
--fasta 'human_genome.fasta' --hostremoval_input_fastq
```

##### 2. Adapter sequence trimming and low-quality bases trimming

Sequencing adapters are small DNA sequences adding prior to DNA sequencing to allow the DNA fragments to attach to the
sequencing flow cells. Because these adapters could interfere with downtstream analyses, we need to remove them before
proceeding any further. Furthermore, because the quality of the sequencing is not always optimal, we need to remove bases
of lower sequencing quality to might lead to spurious results in downstream analyses.

To perform both of these tasks, we'll use the program [fastp](https://github.com/OpenGene/fastp).

```python
! fastp -h
```

    option needs value: --html
    usage: fastp [options] ...
    options:
      -i, --in1                            read1 input file name (string [=])
      -o, --out1                           read1 output file name (string [=])
      -I, --in2                            read2 input file name (string [=])
      -O, --out2                           read2 output file name (string [=])
          --unpaired1                      for PE input, if read1 passed QC but read2 not, it will be written to unpaired1.
                                           Default is to discard it. (string [=])
          --unpaired2                      for PE input, if read2 passed QC but read1 not, it will be written to unpaired2.
                                           If --unpaired2 is same as --unpaired1 (default mode), both unpaired reads will be
                                           written to this same file. (string [=])
          --overlapped_out                 for each read pair, output the overlapped region if it has no any mismatched
                                           base. (string [=])
          --failed_out                     specify the file to store reads that cannot pass the filters. (string [=])
      -m, --merge                          for paired-end input, merge each pair of reads into a single read if they are
                                           overlapped. The merged reads will be written
                                           to the file given by --merged_out, the unmerged reads will be written to the
                                           files specified by --out1 and --out2. The merging mode is disabled by default.
          --merged_out                     in the merging mode, specify the file name to store merged output, or specify
                                           --stdout to stream the merged output (string [=])
          --include_unmerged               in the merging mode, write the unmerged or unpaired reads to the file specified
                                           by --merge. Disabled by default.
      -6, --phred64                        indicate the input is using phred64 scoring (it'll be converted to phred33,
                                           so the output will still be phred33)
      -z, --compression                    compression level for gzip output (1 ~ 9). 1 is fastest, 9 is smallest, default is 4. (int [=4])
          --stdin                          input from STDIN. If the STDIN is interleaved paired-end FASTQ, please also add --interleaved_in.
          --stdout                         stream passing-filters reads to STDOUT. This option will result in interleaved
                                           FASTQ output for paired-end output. Disabled by default.
          --interleaved_in                 indicate that <in1> is an interleaved FASTQ which contains both read1 and read2.
                                           Disabled by default.
          --reads_to_process               specify how many reads/pairs to be processed. Default 0 means process all reads. (int [=0])
          --dont_overwrite                 don't overwrite existing files. Overwritting is allowed by default.
          --fix_mgi_id                     the MGI FASTQ ID format is not compatible with many BAM operation tools, enable this option to fix it.
      -V, --verbose                        output verbose log information (i.e. when every 1M reads are processed).
      -A, --disable_adapter_trimming       adapter trimming is enabled by default. If this option is specified, adapter trimming is disabled
      -a, --adapter_sequence               the adapter for read1. For SE data, if not specified, the adapter will be auto-detected.
                                           For PE data, this is used if R1/R2 are found not overlapped. (string [=auto])
          --adapter_sequence_r2            the adapter for read2 (PE data only). This is used if R1/R2 are found not overlapped.
                                           If not specified, it will be the same as <adapter_sequence> (string [=auto])
          --adapter_fasta                  specify a FASTA file to trim both read1 and read2 (if PE) by all the sequences in this FASTA file (string [=])
          --detect_adapter_for_pe          by default, the auto-detection for adapter is for SE data input only, turn on this
                                        option to enable it for PE data.
      -f, --trim_front1                    trimming how many bases in front for read1, default is 0 (int [=0])
      -t, --trim_tail1                     trimming how many bases in tail for read1, default is 0 (int [=0])
      -b, --max_len1                       if read1 is longer than max_len1, then trim read1 at its tail to make it as
                                           long as max_len1. Default 0 means no limitation (int [=0])
      -F, --trim_front2                    trimming how many bases in front for read2. If it's not specified, it will follow read1's settings (int [=0])
      -T, --trim_tail2                     trimming how many bases in tail for read2. If it's not specified, it will follow read1's settings (int [=0])
      -B, --max_len2                       if read2 is longer than max_len2, then trim read2 at its tail to make it as long as max_len2.
                                           Default 0 means no limitation. If it's not specified, it will follow read1's settings (int [=0])
      -D, --dedup                          enable deduplication to drop the duplicated reads/pairs
          --dup_calc_accuracy              accuracy level to calculate duplication (1~6), higher level uses more memory (1G, 2G, 4G, 8G, 16G, 24G).
                                           Default 1 for no-dedup mode, and 3 for dedup mode. (int [=0])
          --dont_eval_duplication          don't evaluate duplication rate to save time and use less memory.
      -g, --trim_poly_g                    force polyG tail trimming, by default trimming is automatically enabled for Illumina NextSeq/NovaSeq data
          --poly_g_min_len                 the minimum length to detect polyG in the read tail. 10 by default. (int [=10])
      -G, --disable_trim_poly_g            disable polyG tail trimming, by default trimming is automatically enabled for Illumina NextSeq/NovaSeq data
      -x, --trim_poly_x                    enable polyX trimming in 3' ends.
          --poly_x_min_len                 the minimum length to detect polyX in the read tail. 10 by default. (int [=10])
      -5, --cut_front                      move a sliding window from front (5') to tail, drop the bases in the window if
                                           its mean quality < threshold, stop otherwise.
      -3, --cut_tail                       move a sliding window from tail (3') to front, drop the bases in the window if
                                           its mean quality < threshold, stop otherwise.
      -r, --cut_right                      move a sliding window from front to tail, if meet one window with mean quality
                                           < threshold, drop the bases in the window and the right part, and then stop.
      -W, --cut_window_size                the window size option shared by cut_front, cut_tail or cut_sliding. Range: 1~1000, default: 4 (int [=4])
      -M, --cut_mean_quality               the mean quality requirement option shared by cut_front, cut_tail or cut_sliding.
                                           Range: 1~36 default: 20 (Q20) (int [=20])
          --cut_front_window_size          the window size option of cut_front, default to cut_window_size if not specified (int [=4])
          --cut_front_mean_quality         the mean quality requirement option for cut_front, default to cut_mean_quality if not specified (int [=20])
          --cut_tail_window_size           the window size option of cut_tail, default to cut_window_size if not specified (int [=4])
          --cut_tail_mean_quality          the mean quality requirement option for cut_tail, default to cut_mean_quality if not specified (int [=20])
          --cut_right_window_size          the window size option of cut_right, default to cut_window_size if not specified (int [=4])
          --cut_right_mean_quality         the mean quality requirement option for cut_right, default to cut_mean_quality if not specified (int [=20])
      -Q, --disable_quality_filtering      quality filtering is enabled by default. If this option is specified, quality filtering is disabled
      -q, --qualified_quality_phred        the quality value that a base is qualified. Default 15 means phred quality >=Q15 is qualified. (int [=15])
      -u, --unqualified_percent_limit      how many percents of bases are allowed to be unqualified (0~100). Default 40 means 40% (int [=40])
      -n, --n_base_limit                   if one read's number of N base is >n_base_limit, then this read/pair is discarded. Default is 5 (int [=5])
      -e, --average_qual                   if one read's average quality score <avg_qual, then this read/pair is discarded.
                                           Default 0 means no requirement (int [=0])
      -L, --disable_length_filtering       length filtering is enabled by default. If this option is specified, length filtering is disabled
      -l, --length_required                reads shorter than length_required will be discarded, default is 15. (int [=15])
          --length_limit                   reads longer than length_limit will be discarded, default 0 means no limitation. (int [=0])
      -y, --low_complexity_filter          enable low complexity filter. The complexity is defined as the percentage of base
                                           that is different from its next base (base[i] != base[i+1]).
      -Y, --complexity_threshold           the threshold for low complexity filter (0~100). Default is 30, which means 30% complexity is required. (int [=30])
          --filter_by_index1               specify a file contains a list of barcodes of index1 to be filtered out, one barcode per line (string [=])
          --filter_by_index2               specify a file contains a list of barcodes of index2 to be filtered out, one barcode per line (string [=])
          --filter_by_index_threshold      the allowed difference of index barcode for index filtering, default 0 means completely identical. (int [=0])
      -c, --correction                     enable base correction in overlapped regions (only for PE data), default is disabled
          --overlap_len_require            the minimum length to detect overlapped region of PE reads. This will affect overlap analysis based PE merge,
                                           adapter trimming and correction. 30 by default. (int [=30])
          --overlap_diff_limit             the maximum number of mismatched bases to detect overlapped region of PE reads.
                                           This will affect overlap analysis based PE merge, adapter trimming and correction. 5 by default. (int [=5])
          --overlap_diff_percent_limit     the maximum percentage of mismatched bases to detect overlapped region of PE reads.
                                           This will affect overlap analysis based PE merge, adapter trimming and correction. Default 20 means 20%. (int [=20])
      -U, --umi                            enable unique molecular identifier (UMI) preprocessing
          --umi_loc                        specify the location of UMI, can be (index1/index2/read1/read2/per_index/per_read, default is none (string [=])
          --umi_len                        if the UMI is in read1/read2, its length should be provided (int [=0])
          --umi_prefix                     if specified, an underline will be used to connect prefix and UMI (i.e.
                                           prefix=UMI, UMI=AATTCG, final=UMI_AATTCG). No prefix by default (string [=])
          --umi_skip                       if the UMI is in read1/read2, fastp can skip several bases following UMI, default is 0 (int [=0])
      -p, --overrepresentation_analysis    enable overrepresented sequence analysis.
      -P, --overrepresentation_sampling    one in (--overrepresentation_sampling) reads will be computed for overrepresentation
                                           analysis (1~10000), smaller is slower, default is 20. (int [=20])
      -j, --json                           the json format report file name (string [=fastp.json])
      -h, --html                           the html format report file name (string [=fastp.html])
      -R, --report_title                   should be quoted with ' or ", default is "fastp report" (string [=fastp report])
      -w, --thread                         worker thread number, default is 3 (int [=3])
      -s, --split                          split output by limiting total split file number with this option (2~999), a sequential number prefix
                                           will be added to output name ( 0001.out.fq, 0002.out.fq...), disabled by default (int [=0])
      -S, --split_by_lines                 split output by limiting lines of each file with this option(>=1000), a sequential number prefix will be
                                           added to output name ( 0001.out.fq, 0002.out.fq...), disabled by default (long [=0])
      -d, --split_prefix_digits            the digits for the sequential number padding (1~10), default is 4, so the filename will be padded as
                                           0001.xxx, 0 to disable padding (int [=4])
          --cut_by_quality5                DEPRECATED, use --cut_front instead.
          --cut_by_quality3                DEPRECATED, use --cut_tail instead.
          --cut_by_quality_aggressive      DEPRECATED, use --cut_right instead.
          --discard_unmerged               DEPRECATED, no effect now, see the introduction for merging.
      -?, --help                           print this message

```bash
%%bash
fastp \
    --in1 ../data/subsampled/ERR5766177_PE.mapped.hostremoved.fwd.fq_subsample_1000000.fastq.gz \
    --in2 ../data/subsampled/ERR5766177_PE.mapped.hostremoved.fwd.fq_subsample_1000000.fastq.gz \
    --merge \
    --merged_out ../results/fastp/ERR5766177.merged.fastq.gz \
    --include_unmerged \
    --dedup \
    --json ../results/fastp/ERR5766177.fastp.json \
    --html ../results/fastp/ERR5766177.fastp.html \
```

    Read1 before filtering:
    total reads: 1000000
    total bases: 101000000
    Q20 bases: 99440729(98.4562%)
    Q30 bases: 94683150(93.7457%)

    Read2 before filtering:
    total reads: 1000000
    total bases: 101000000
    Q20 bases: 99440729(98.4562%)
    Q30 bases: 94683150(93.7457%)

    Merged and filtered:
    total reads: 1994070
    total bases: 201397311
    Q20 bases: 198330392(98.4772%)
    Q30 bases: 188843169(93.7665%)

    Filtering result:
    reads passed filter: 1999252
    reads failed due to low quality: 728
    reads failed due to too many N: 20
    reads failed due to too short: 0
    reads with adapter trimmed: 282
    bases trimmed due to adapters: 18654
    reads corrected by overlap analysis: 0
    bases corrected by overlap analysis: 0

    Duplication rate: 0.2479%

    Insert size peak (evaluated by paired-end reads): 31

    Read pairs merged: 228
    % of original read pairs: 0.0228%
    % in reads after filtering: 0.0114339%


    JSON report: ../results/fastp/ERR5766177.fastp.json
    HTML report: ../results/fastp/ERR5766177.fastp.html

    fastp --in1 ../data/subsampled/ERR5766177_PE.mapped.hostremoved.fwd.fq_subsample_1000000.fastq.gz \
    --in2 ../data/subsampled/ERR5766177_PE.mapped.hostremoved.fwd.fq_subsample_1000000.fastq.gz --merge \
    --merged_out ../results/fastp/ERR5766177.merged.fastq.gz --include_unmerged --dedup \
    --json ../results/fastp/ERR5766177.fastp.json --html ../results/fastp/ERR5766177.fastp.html
    fastp v0.23.2, time used: 11 seconds

##### 3. Taxonomic profiling with Metaphlan

```python
! metaphlan  --help
```

    usage: metaphlan --input_type {fastq,fasta,bowtie2out,sam} [--force]
                     [--bowtie2db METAPHLAN_BOWTIE2_DB] [-x INDEX]
                     [--bt2_ps BowTie2 presets] [--bowtie2_exe BOWTIE2_EXE]
                     [--bowtie2_build BOWTIE2_BUILD] [--bowtie2out FILE_NAME]
                     [--min_mapq_val MIN_MAPQ_VAL] [--no_map] [--tmp_dir]
                     [--tax_lev TAXONOMIC_LEVEL] [--min_cu_len]
                     [--min_alignment_len] [--add_viruses] [--ignore_eukaryotes]
                     [--ignore_bacteria] [--ignore_archaea] [--stat_q]
                     [--perc_nonzero] [--ignore_markers IGNORE_MARKERS]
                     [--avoid_disqm] [--stat] [-t ANALYSIS TYPE]
                     [--nreads NUMBER_OF_READS] [--pres_th PRESENCE_THRESHOLD]
                     [--clade] [--min_ab] [-o output file] [--sample_id_key name]
                     [--use_group_representative] [--sample_id value]
                     [-s sam_output_file] [--legacy-output] [--CAMI_format_output]
                     [--unknown_estimation] [--biom biom_output] [--mdelim mdelim]
                     [--nproc N] [--install] [--force_download]
                     [--read_min_len READ_MIN_LEN] [-v] [-h]
                     [INPUT_FILE] [OUTPUT_FILE]

    DESCRIPTION
     MetaPhlAn version 3.1.0 (25 Jul 2022):
     METAgenomic PHyLogenetic ANalysis for metagenomic taxonomic profiling.

    AUTHORS: Francesco Beghini (francesco.beghini@unitn.it),Nicola Segata (nicola.segata@unitn.it), Duy Tin Truong,
    Francesco Asnicar (f.asnicar@unitn.it), Aitor Blanco Miguez (aitor.blancomiguez@unitn.it)

    COMMON COMMANDS

     We assume here that MetaPhlAn is installed using the several options available (pip, conda, PyPi)
     Also BowTie2 should be in the system path with execution and read permissions, and Perl should be installed)

    ========== MetaPhlAn clade-abundance estimation =================

    The basic usage of MetaPhlAn consists in the identification of the clades (from phyla to species )
    present in the metagenome obtained from a microbiome sample and their
    relative abundance. This correspond to the default analysis type (-t rel_ab).

    *  Profiling a metagenome from raw reads:
    $ metaphlan metagenome.fastq --input_type fastq -o profiled_metagenome.txt

    *  You can take advantage of multiple CPUs and save the intermediate BowTie2 output for re-running
       MetaPhlAn extremely quickly:
    $ metaphlan metagenome.fastq --bowtie2out metagenome.bowtie2.bz2 --nproc 5 --input_type fastq -o profiled_metagenome.txt

    *  If you already mapped your metagenome against the marker DB (using a previous MetaPhlAn run), you
       can obtain the results in few seconds by using the previously saved --bowtie2out file and
       specifying the input (--input_type bowtie2out):
    $ metaphlan metagenome.bowtie2.bz2 --nproc 5 --input_type bowtie2out -o profiled_metagenome.txt

    *  bowtie2out files generated with MetaPhlAn versions below 3 are not compatibile.
       Starting from MetaPhlAn 3.0, the BowTie2 ouput now includes the size of the profiled metagenome and the average read length.
       If you want to re-run MetaPhlAn using these file you should provide the metagenome size via --nreads:
    $ metaphlan metagenome.bowtie2.bz2 --nproc 5 --input_type bowtie2out --nreads 520000 -o profiled_metagenome.txt

    *  You can also provide an externally BowTie2-mapped SAM if you specify this format with
       --input_type. Two steps: first apply BowTie2 and then feed MetaPhlAn with the obtained sam:
    $ bowtie2 --sam-no-hd --sam-no-sq --no-unal --very-sensitive -S metagenome.sam -x \
      ${mpa_dir}/metaphlan_databases/mpa_v30_CHOCOPhlAn_201901 -U metagenome.fastq
    $ metaphlan metagenome.sam --input_type sam -o profiled_metagenome.txt

    *  We can also natively handle paired-end metagenomes, and, more generally, metagenomes stored in
      multiple files (but you need to specify the --bowtie2out parameter):
    $ metaphlan metagenome_1.fastq,metagenome_2.fastq --bowtie2out metagenome.bowtie2.bz2 --nproc 5 --input_type fastq

    -------------------------------------------------------------------


    ========== Marker level analysis ============================

    MetaPhlAn introduces the capability of characterizing organisms at the strain level using non
    aggregated marker information. Such capability comes with several slightly different flavours and
    are a way to perform strain tracking and comparison across multiple samples.
    Usually, MetaPhlAn is first ran with the default -t to profile the species present in
    the community, and then a strain-level profiling can be performed to zoom-in into specific species
    of interest. This operation can be performed quickly as it exploits the --bowtie2out intermediate
    file saved during the execution of the default analysis type.

    *  The following command will output the abundance of each marker with a RPK (reads per kilo-base)
       higher 0.0. (we are assuming that metagenome_outfmt.bz2 has been generated before as
       shown above).
    $ metaphlan -t marker_ab_table metagenome_outfmt.bz2 --input_type bowtie2out -o marker_abundance_table.txt
       The obtained RPK can be optionally normalized by the total number of reads in the metagenome
       to guarantee fair comparisons of abundances across samples. The number of reads in the metagenome
       needs to be passed with the '--nreads' argument

    *  The list of markers present in the sample can be obtained with '-t marker_pres_table'
    $ metaphlan -t marker_pres_table metagenome_outfmt.bz2 --input_type bowtie2out -o marker_abundance_table.txt
       The --pres_th argument (default 1.0) set the minimum RPK value to consider a marker present

    *  The list '-t clade_profiles' analysis type reports the same information of '-t marker_ab_table'
       but the markers are reported on a clade-by-clade basis.
    $ metaphlan -t clade_profiles metagenome_outfmt.bz2 --input_type bowtie2out -o marker_abundance_table.txt

    *  Finally, to obtain all markers present for a specific clade and all its subclades, the
       '-t clade_specific_strain_tracker' should be used. For example, the following command
       is reporting the presence/absence of the markers for the B. fragilis species and its strains
       the optional argument --min_ab specifies the minimum clade abundance for reporting the markers

    $ metaphlan -t clade_specific_strain_tracker --clade s__Bacteroides_fragilis metagenome_outfmt.bz2 --input_typ
      bowtie2out -o marker_abundance_table.txt

    -------------------------------------------------------------------

    positional arguments:
      INPUT_FILE            the input file can be:
                            * a fastq file containing metagenomic reads
                            OR
                            * a BowTie2 produced SAM file.
                            OR
                            * an intermediary mapping file of the metagenome generated by a previous MetaPhlAn run
                            If the input file is missing, the script assumes that the input is provided using the standard
                            input, or named pipes.
                            IMPORTANT: the type of input needs to be specified with --input_type
      OUTPUT_FILE           the tab-separated output file of the predicted taxon relative abundances
                            [stdout if not present]

    Required arguments:
      --input_type {fastq,fasta,bowtie2out,sam}
                            set whether the input is the FASTA file of metagenomic reads or
                            the SAM file of the mapping of the reads against the MetaPhlAn db.

    Mapping arguments:
      --force               Force profiling of the input file by removing the bowtie2out file
      --bowtie2db METAPHLAN_BOWTIE2_DB
                            Folder containing the MetaPhlAn database. You can specify the location by exporting the
                            DEFAULT_DB_FOLDER variable in the shell.
                            [default /Users/maxime/mambaforge/envs/summer_school_microbiome/lib/python3.9/site-packages/metaphlan/metaphlan_databases]
      -x INDEX, --index INDEX
                            Specify the id of the database version to use. If "latest", MetaPhlAn will get the latest version.
                            If an index name is provided, MetaPhlAn will try to use it, if available, and skip the online check.
                            If the database files are not found on the local MetaPhlAn installation they
                            will be automatically downloaded [default latest]
      --bt2_ps BowTie2 presets
                            Presets options for BowTie2 (applied only when a FASTA file is provided)
                            The choices enabled in MetaPhlAn are:
                             * sensitive
                             * very-sensitive
                             * sensitive-local
                             * very-sensitive-local
                            [default very-sensitive]
      --bowtie2_exe BOWTIE2_EXE
                            Full path and name of the BowTie2 executable. This option allowsMetaPhlAn to reach the
                            executable even when it is not in the system PATH or the system PATH is unreachable
      --bowtie2_build BOWTIE2_BUILD
                            Full path to the bowtie2-build command to use, deafult assumes that 'bowtie2-build is present in the system path
      --bowtie2out FILE_NAME
                            The file for saving the output of BowTie2
      --min_mapq_val MIN_MAPQ_VAL
                            Minimum mapping quality value (MAPQ) [default 5]
      --no_map              Avoid storing the --bowtie2out map file
      --tmp_dir             The folder used to store temporary files [default is the OS dependent tmp dir]

    Post-mapping arguments:
      --tax_lev TAXONOMIC_LEVEL
                            The taxonomic level for the relative abundance output:
                            'a' : all taxonomic levels
                            'k' : kingdoms
                            'p' : phyla only
                            'c' : classes only
                            'o' : orders only
                            'f' : families only
                            'g' : genera only
                            's' : species only
                            [default 'a']
      --min_cu_len          minimum total nucleotide length for the markers in a clade for
                            estimating the abundance without considering sub-clade abundances
                            [default 2000]
      --min_alignment_len   The sam records for aligned reads with the longest subalignment
                            length smaller than this threshold will be discarded.
                            [default None]
      --add_viruses         Allow the profiling of viral organisms
      --ignore_eukaryotes   Do not profile eukaryotic organisms
      --ignore_bacteria     Do not profile bacterial organisms
      --ignore_archaea      Do not profile archeal organisms
      --stat_q              Quantile value for the robust average
                            [default 0.2]
      --perc_nonzero        Percentage of markers with a non zero relative abundance for misidentify a species
                            [default 0.33]
      --ignore_markers IGNORE_MARKERS
                            File containing a list of markers to ignore.
      --avoid_disqm         Deactivate the procedure of disambiguating the quasi-markers based on the
                            marker abundance pattern found in the sample. It is generally recommended
                            to keep the disambiguation procedure in order to minimize false positives
      --stat                Statistical approach for converting marker abundances into clade abundances
                            'avg_g'  : clade global (i.e. normalizing all markers together) average
                            'avg_l'  : average of length-normalized marker counts
                            'tavg_g' : truncated clade global average at --stat_q quantile
                            'tavg_l' : truncated average of length-normalized marker counts (at --stat_q)
                            'wavg_g' : winsorized clade global average (at --stat_q)
                            'wavg_l' : winsorized average of length-normalized marker counts (at --stat_q)
                            'med'    : median of length-normalized marker counts
                            [default tavg_g]

    Additional analysis types and arguments:
      -t ANALYSIS TYPE      Type of analysis to perform:
                             * rel_ab: profiling a metagenomes in terms of relative abundances
                             * rel_ab_w_read_stats: profiling a metagenomes in terms of relative abundances and estimate
                                                    the number of reads coming from each clade.
                             * reads_map: mapping from reads to clades (only reads hitting a marker)
                             * clade_profiles: normalized marker counts for clades with at least a non-null marker
                             * marker_ab_table: normalized marker counts (only when > 0.0 and normalized by metagenome size if --nreads is specified)
                             * marker_counts: non-normalized marker counts [use with extreme caution]
                             * marker_pres_table: list of markers present in the sample (threshold at 1.0 if not differently specified with --pres_th
                             * clade_specific_strain_tracker: list of markers present for a specific clade, specified with --clade, and all its subclades
                            [default 'rel_ab']
      --nreads NUMBER_OF_READS
                            The total number of reads in the original metagenome. It is used only when
                            -t marker_table is specified for normalizing the length-normalized counts
                            with the metagenome size as well. No normalization applied if --nreads is not
                            specified
      --pres_th PRESENCE_THRESHOLD
                            Threshold for calling a marker present by the -t marker_pres_table option
      --clade               The clade for clade_specific_strain_tracker analysis
      --min_ab              The minimum percentage abundance for the clade in the clade_specific_strain_tracker analysis

    Output arguments:
      -o output file, --output_file output file
                            The output file (if not specified as positional argument)
      --sample_id_key name  Specify the sample ID key for this analysis. Defaults to 'SampleID'.
      --use_group_representative
                            Use a species as representative for species groups.
      --sample_id value     Specify the sample ID for this analysis. Defaults to 'Metaphlan_Analysis'.
      -s sam_output_file, --samout sam_output_file
                            The sam output file
      --legacy-output       Old MetaPhlAn2 two columns output
      --CAMI_format_output  Report the profiling using the CAMI output format
      --unknown_estimation  Scale relative abundances to the number of reads mapping to known clades in order to estimate unknowness
      --biom biom_output, --biom_output_file biom_output
                            If requesting biom file output: The name of the output file in biom format
      --mdelim mdelim, --metadata_delimiter_char mdelim
                            Delimiter for bug metadata: - defaults to pipe. e.g. the pipe in k__Bacteria|p__Proteobacteria

    Other arguments:
      --nproc N             The number of CPUs to use for parallelizing the mapping [default 4]
      --install             Only checks if the MetaPhlAn DB is installed and installs it if not. All other parameters are ignored.
      --force_download      Force the re-download of the latest MetaPhlAn database.
      --read_min_len READ_MIN_LEN
                            Specify the minimum length of the reads to be considered when parsing the input file with
                            'read_fastx.py' script, default value is 70
      -v, --version         Prints the current MetaPhlAn version and exit
      -h, --help            show this help message and exit

```bash
metaphlan ../results/fastp/ERR5766177.merged.fastq.gz  \
    --input_type fastq \
    --bowtie2out ../results/metaphlan/ERR5766177.bt2.out  \
    --nproc 4 \
    > ../results/metaphlan/ERR5766177.metaphlan_profile.txt
```

The main results files that we're interested in is located at
[../results/metaphlan/ERR5766177.metaphlan_profile.txt](../results/metaphlan/ERR5766177.metaphlan_profile.txt)

It's a tab separated file, with taxons in rows, with their relative abundance in the sample

```python
! head ../results/metaphlan/ERR5766177.metaphlan_profile.txt
```

    #mpa_v30_CHOCOPhlAn_201901
    #/home/maxime_borry/.conda/envs/maxime/envs/summer_school_microbiome/bin/metaphlan ../results/fastp/ERR5766177.merged.fastq.gz \
    --input_type fastq --bowtie2out ../results/metaphlan/ERR5766177.bt2.out --nproc 8
    #SampleID	Metaphlan_Analysis
    #clade_name	NCBI_tax_id	relative_abundance	additional_species
    k__Bacteria	2	82.23198
    k__Archaea	2157	17.76802
    k__Bacteria|p__Firmicutes	2|1239	33.47957
    k__Bacteria|p__Bacteroidetes	2|976	28.4209
    k__Bacteria|p__Actinobacteria	2|201174	20.33151
    k__Archaea|p__Euryarchaeota	2157|28890	17.76802

##### 4. Visualizing the taxonomic profile

###### 4.1 Visualizing metaphlan taxonomic profile with Pavian

[Pavian](https://github.com/fbreitwieser/pavian) is an interactive app to explore results of different taxonomic classifiers

There are different ways to run it:

- If you have [docker](https://www.docker.com/) installed (and are somehow familiar with it)

```bash
docker pull 'florianbw/pavian'
docker run --rm -p 5000:80 florianbw/pavian
```

Then open your browser and visit [localhost:5000](localhost:5000)

- If you are familiar with [R](https://www.r-project.org/)

```r
if (!require(remotes)) { install.packages("remotes") }
remotes::install_github("fbreitwieser/pavian")

pavian::runApp(port=5000)
```

Then open your browser and visit [localhost:5000](localhost:5000)

- Otherwise, just visit [fbreitwieser.shinyapps.io/pavian](https://fbreitwieser.shinyapps.io/pavian/.).

###### 4.2 Visualizing metaphlan taxonomic profile with [Krona](https://github.com/marbl/Krona/wiki)

```bash
%%bash
python ../scripts/metaphlan2krona.py -p ../results/metaphlan/ERR5766177.metaphlan_profile.txt -k ../results/krona/ERR5766177_krona.out
ktImportText -o ../results/krona/ERR5766177_krona.html ../results/krona/ERR5766177_krona.out
```

    Writing ../results/krona/ERR5766177_krona.html...

##### 5. Getting modern reference data

In order to compare our sample with modern reference samples, I used the curatedMetagenomicsData package,
which provides both curated metadata, and pre-computed metaphlan taxonomic profiles for published modern human samples.
The full R code to get these data is available in [curatedMetagenomics/get_sources.Rmd](./curatedMetagenomics/get_sources.Rmd)

I pre-selected 200 gut microbiome samples from non-westernized (100) and westernized (100) from healthy, non-antibiotic users donors.

```R
library(curatedMetagenomicData)
library(tidyverse)

sampleMetadata %>%
  filter(body_site=='stool' & antibiotics_current_use  == 'no' & disease == 'healthy') %>%
  group_by(non_westernized) %>%
  sample_n(100) %>%
  ungroup() -> selected_samples

selected_samples %>%
  returnSamples("relative_abundance") -> rel_ab

data_ranks = splitByRanks(rel_ab)

for (r in names(data_ranks)){
  print(r)
  assay_rank = as.data.frame(assay(data_ranks[[r]]))
  print(paste0("../../data/curated_metagenomics/modern_sources_",tolower(r),".csv"))
  write.csv(assay_rank, paste0("../../data/curated_metagenomics/modern_sources_",tolower(r),".csv"))


```

- The resulting metaphlan taxonomic profiles (split by taxonomic ranks) are available at
- [../data/curated_metagenomics](../data/curated_metagenomics)
- The associated metadata is available at
- [../data/metadata/curated_metagenomics_modern_sources.csv](../data/metadata/curated_metagenomics_modern_sources.csv)

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Taxonomic_Rank_Graph.svg/800px-Taxonomic_Rank_Graph.svg.png" alt="Taxonomic ranks" width="400">

##### 6. Bringing together ancient and modern data

This is the moment where we will the [Pandas](https://pandas.pydata.org) [Python](https://www.python.org/) library to perform some data manipulation.  
We will also use the [Taxopy](https://github.com/apcamargo/taxopy) library to work to taxonomic informations.

```python
! pip install taxopy
```

    Requirement already satisfied: taxopy in /Users/maxime/mambaforge/envs/summer_school_microbiome/lib/python3.9/site-packages (0.10.0)

```python
import pandas as pd
import taxopy
import pickle
import gzip
```

```python
with gzip.open("../data/taxopy/taxdb.p.gz", 'rb') as tdb:
    taxo_db = pickle.load(tdb)
```

```python
! head ../results/metaphlan/ERR5766177.metaphlan_profile.txt
```

    #mpa_v30_CHOCOPhlAn_201901
    #/home/maxime_borry/.conda/envs/maxime/envs/summer_school_microbiome/bin/metaphlan ../results/fastp/ERR5766177.merged.fastq.gz
    --input_type fastq --bowtie2out ../results/metaphlan/ERR5766177.bt2.out --nproc 8
    #SampleID	Metaphlan_Analysis
    #clade_name	NCBI_tax_id	relative_abundance	additional_species
    k__Bacteria	2	82.23198
    k__Archaea	2157	17.76802
    k__Bacteria|p__Firmicutes	2|1239	33.47957
    k__Bacteria|p__Bacteroidetes	2|976	28.4209
    k__Bacteria|p__Actinobacteria	2|201174	20.33151
    k__Archaea|p__Euryarchaeota	2157|28890	17.76802

```python
ancient_data = pd.read_csv("../results/metaphlan/ERR5766177.metaphlan_profile.txt",
                            comment="#",
                            delimiter="\t",
                            names=['clade_name','NCBI_tax_id','relative_abundance','additional_species'])
```

```python
ancient_data.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>clade_name</th>
      <th>NCBI_tax_id</th>
      <th>relative_abundance</th>
      <th>additional_species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>k__Bacteria</td>
      <td>2</td>
      <td>82.23198</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>k__Archaea</td>
      <td>2157</td>
      <td>17.76802</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>k__Bacteria|p__Firmicutes</td>
      <td>2|1239</td>
      <td>33.47957</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>k__Bacteria|p__Bacteroidetes</td>
      <td>2|976</td>
      <td>28.42090</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>k__Bacteria|p__Actinobacteria</td>
      <td>2|201174</td>
      <td>20.33151</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>

```python
ancient_data.sample(10)
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>clade_name</th>
      <th>NCBI_tax_id</th>
      <th>relative_abundance</th>
      <th>additional_species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>k__Archaea</td>
      <td>2157</td>
      <td>17.76802</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>46</th>
      <td>k__Bacteria|p__Bacteroidetes|c__Bacteroidia|o_...</td>
      <td>2|976|200643|171549|171552|838|165179</td>
      <td>25.75544</td>
      <td>k__Bacteria|p__Bacteroidetes|c__Bacteroidia|o_...</td>
    </tr>
    <tr>
      <th>55</th>
      <td>k__Bacteria|p__Firmicutes|c__Clostridia|o__Clo...</td>
      <td>2|1239|186801|186802|186803|189330|88431</td>
      <td>0.91178</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>18</th>
      <td>k__Archaea|p__Euryarchaeota|c__Halobacteria|o_...</td>
      <td>2157|28890|183963|2235</td>
      <td>0.71177</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>36</th>
      <td>k__Bacteria|p__Actinobacteria|c__Actinobacteri...</td>
      <td>2|201174|1760|85004|31953|1678</td>
      <td>9.39377</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>65</th>
      <td>k__Bacteria|p__Actinobacteria|c__Actinobacteri...</td>
      <td>2|201174|1760|85004|31953|1678|216816</td>
      <td>0.05447</td>
      <td>k__Bacteria|p__Actinobacteria|c__Actinobacteri...</td>
    </tr>
    <tr>
      <th>37</th>
      <td>k__Bacteria|p__Firmicutes|c__Clostridia|o__Clo...</td>
      <td>2|1239|186801|186802|186803|</td>
      <td>2.16125</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>38</th>
      <td>k__Bacteria|p__Firmicutes|c__Clostridia|o__Clo...</td>
      <td>2|1239|186801|186802|541000|216851</td>
      <td>1.24537</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>26</th>
      <td>k__Bacteria|p__Actinobacteria|c__Actinobacteri...</td>
      <td>2|201174|1760|85004|31953</td>
      <td>9.39377</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>48</th>
      <td>k__Bacteria|p__Firmicutes|c__Clostridia|o__Clo...</td>
      <td>2|1239|186801|186802|541000|1263|40518</td>
      <td>14.96816</td>
      <td>k__Bacteria|p__Firmicutes|c__Clostridia|o__Clo...</td>
    </tr>
  </tbody>
</table>
</div>

Because for this analysis, we're only going to look at the relative abundance, we'll only this column, an
the [TAXID](https://www.ncbi.nlm.nih.gov/taxonomy) information

```python
ancient_data = (
    ancient_data
    .rename(columns={'NCBI_tax_id': 'TAXID'})
    .drop(['clade_name','additional_species'], axis=1)
)
```

Always investigate your data at first !

```python
ancient_data.relative_abundance.sum()
```

    700.00007

**Pause and think**: A relative abundance of 700%, really ?

Let's proceed further and try to understand what's happening.

```python
ancient_data.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>TAXID</th>
      <th>relative_abundance</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>82.23198</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2157</td>
      <td>17.76802</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2|1239</td>
      <td>33.47957</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2|976</td>
      <td>28.42090</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2|201174</td>
      <td>20.33151</td>
    </tr>
  </tbody>
</table>
</div>

To make sense of the TAXID, we will use taxopy to get all the taxonomic related informations such as:

- name of the taxon
- rank of the taxon
- lineage of the taxon

```python
#### This function is here to help us get the taxon information
#### from the metaphlan taxonomic ID lineage, of the following form
#### 2|976|200643|171549|171552|838|165179

def to_taxopy(taxid_entry, taxo_db):
    """Returns a taxopy taxon object
    Args:
        taxid_entry(str): metaphlan TAXID taxonomic lineage
        taxo_db(taxopy database)
    Returns:
        (bool): Returns a taxopy taxon object
    """
    taxid = taxid_entry.split("|")[-1] # get the last element
    try:
        if len(taxid) > 0:
            return taxopy.Taxon(int(taxid), taxo_db) # if it's not empty, get the taxon corresponding to the taxid
        else:
            return taxopy.Taxon(12908, taxo_db) # otherwise, return the taxon associated with unclassified sequences
    except taxopy.exceptions.TaxidError as e:
        return taxopy.Taxon(12908, taxo_db)
```

```python
ancient_data['taxopy'] = ancient_data['TAXID'].apply(to_taxopy, taxo_db=taxo_db)
```

```python
ancient_data.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>TAXID</th>
      <th>relative_abundance</th>
      <th>taxopy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>82.23198</td>
      <td>s__Bacteria</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2157</td>
      <td>17.76802</td>
      <td>s__Archaea</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2|1239</td>
      <td>33.47957</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicutes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2|976</td>
      <td>28.42090</td>
      <td>s__Bacteria;c__FCB group;p__Bacteroidetes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2|201174</td>
      <td>20.33151</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Actinoba...</td>
    </tr>
  </tbody>
</table>
</div>

```python
ancient_data = ancient_data.assign(
    rank = ancient_data.taxopy.apply(lambda x: x.rank),
    name = ancient_data.taxopy.apply(lambda x: x.name),
    lineage = ancient_data.taxopy.apply(lambda x: x.name_lineage),
)
```

```python
ancient_data
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>TAXID</th>
      <th>relative_abundance</th>
      <th>taxopy</th>
      <th>rank</th>
      <th>name</th>
      <th>lineage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>82.23198</td>
      <td>s__Bacteria</td>
      <td>superkingdom</td>
      <td>Bacteria</td>
      <td>[Bacteria, cellular organisms, root]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2157</td>
      <td>17.76802</td>
      <td>s__Archaea</td>
      <td>superkingdom</td>
      <td>Archaea</td>
      <td>[Archaea, cellular organisms, root]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2|1239</td>
      <td>33.47957</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicutes</td>
      <td>phylum</td>
      <td>Firmicutes</td>
      <td>[Firmicutes, Terrabacteria group, Bacteria, ce...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2|976</td>
      <td>28.42090</td>
      <td>s__Bacteria;c__FCB group;p__Bacteroidetes</td>
      <td>phylum</td>
      <td>Bacteroidetes</td>
      <td>[Bacteroidetes, Bacteroidetes/Chlorobi group, ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2|201174</td>
      <td>20.33151</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Actinoba...</td>
      <td>phylum</td>
      <td>Actinobacteria</td>
      <td>[Actinobacteria, Terrabacteria group, Bacteria...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>62</th>
      <td>2|1239|186801|186802|186803|572511|33039</td>
      <td>0.24910</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicut...</td>
      <td>species</td>
      <td>[Ruminococcus] torques</td>
      <td>[[Ruminococcus] torques, Mediterraneibacter, L...</td>
    </tr>
    <tr>
      <th>63</th>
      <td>2|201174|84998|84999|84107|1472762|1232426</td>
      <td>0.17084</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Actinoba...</td>
      <td>species</td>
      <td>[Collinsella] massiliensis</td>
      <td>[[Collinsella] massiliensis, Enorma, Coriobact...</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2|1239|186801|186802|186803|189330|39486</td>
      <td>0.07690</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicut...</td>
      <td>species</td>
      <td>Dorea formicigenerans</td>
      <td>[Dorea formicigenerans, Dorea, Lachnospiraceae...</td>
    </tr>
    <tr>
      <th>65</th>
      <td>2|201174|1760|85004|31953|1678|216816</td>
      <td>0.05447</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Actinoba...</td>
      <td>species</td>
      <td>Bifidobacterium longum</td>
      <td>[Bifidobacterium longum, Bifidobacterium, Bifi...</td>
    </tr>
    <tr>
      <th>66</th>
      <td>2|1239|186801|186802|541000|1263|1262959</td>
      <td>0.01440</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicut...</td>
      <td>species</td>
      <td>Ruminococcus sp. CAG:488</td>
      <td>[Ruminococcus sp. CAG:488, environmental sampl...</td>
    </tr>
  </tbody>
</table>
<p>67 rows × 6 columns</p>
</div>

Because our modern data are split by ranks, we'll first split our ancient sample by rank

Which of the entries are at the `species rank` level ?

```python
ancient_species = ancient_data.query("rank == 'species'")
```

```python
ancient_species.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>TAXID</th>
      <th>relative_abundance</th>
      <th>taxopy</th>
      <th>rank</th>
      <th>name</th>
      <th>lineage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>46</th>
      <td>2|976|200643|171549|171552|838|165179</td>
      <td>25.75544</td>
      <td>s__Bacteria;c__FCB group;p__Bacteroidetes;c__B...</td>
      <td>species</td>
      <td>Prevotella copri</td>
      <td>[Prevotella copri, Prevotella, Prevotellaceae,...</td>
    </tr>
    <tr>
      <th>47</th>
      <td>2157|28890|183925|2158|2159|2172|2173</td>
      <td>17.05626</td>
      <td>s__Archaea;p__Euryarchaeota;c__Methanomada gro...</td>
      <td>species</td>
      <td>Methanobrevibacter smithii</td>
      <td>[Methanobrevibacter smithii, Methanobrevibacte...</td>
    </tr>
    <tr>
      <th>48</th>
      <td>2|1239|186801|186802|541000|1263|40518</td>
      <td>14.96816</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicut...</td>
      <td>species</td>
      <td>Ruminococcus bromii</td>
      <td>[Ruminococcus bromii, Ruminococcus, Oscillospi...</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2|1239|186801|186802|186803|841|301302</td>
      <td>13.57908</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Firmicut...</td>
      <td>species</td>
      <td>Roseburia faecis</td>
      <td>[Roseburia faecis, Roseburia, Lachnospiraceae,...</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2|201174|84998|84999|84107|102106|74426</td>
      <td>9.49165</td>
      <td>s__Bacteria;c__Terrabacteria group;p__Actinoba...</td>
      <td>species</td>
      <td>Collinsella aerofaciens</td>
      <td>[Collinsella aerofaciens, Collinsella, Corioba...</td>
    </tr>
  </tbody>
</table>
</div>

Let's do a bit of renaming to prepare for what's coming next

```python
ancient_species = ancient_species[['relative_abundance','name']].set_index('name').rename(columns={'relative_abundance':'ERR5766177'})
```

```python
ancient_species.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ERR5766177</th>
    </tr>
    <tr>
      <th>name</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Prevotella copri</th>
      <td>25.75544</td>
    </tr>
    <tr>
      <th>Methanobrevibacter smithii</th>
      <td>17.05626</td>
    </tr>
    <tr>
      <th>Ruminococcus bromii</th>
      <td>14.96816</td>
    </tr>
    <tr>
      <th>Roseburia faecis</th>
      <td>13.57908</td>
    </tr>
    <tr>
      <th>Collinsella aerofaciens</th>
      <td>9.49165</td>
    </tr>
  </tbody>
</table>
</div>

```python
ancient_phylums = ancient_data.query("rank == 'phylum'")
```

```python
ancient_phylums = ancient_phylums[['relative_abundance','name']].set_index('name').rename(columns={'relative_abundance':'ERR5766177'})
```

```python
ancient_phylums
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ERR5766177</th>
    </tr>
    <tr>
      <th>name</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Firmicutes</th>
      <td>33.47957</td>
    </tr>
    <tr>
      <th>Bacteroidetes</th>
      <td>28.42090</td>
    </tr>
    <tr>
      <th>Actinobacteria</th>
      <td>20.33151</td>
    </tr>
    <tr>
      <th>Euryarchaeota</th>
      <td>17.76802</td>
    </tr>
  </tbody>
</table>
</div>

Now, let's go back to the 700% relative abundance issue...

```python
ancient_data.groupby('rank')['relative_abundance'].sum()
```

    rank
    class            99.72648
    family           83.49854
    genus            97.56524
    no rank          19.48331
    order            99.72648
    phylum          100.00000
    species         100.00002
    superkingdom    100.00000
    Name: relative_abundance, dtype: float64

Seems better, right ?

**Pause and think: why don't we get exactly 100%** ?

Now let's load our modern reference samples

```python
modern_phylums = pd.read_csv("../data/curated_metagenomics/modern_sources_phylum.csv", index_col=0)
modern_phylums.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <th>PNP_Main_283</th>
      <th>PNP_Validation_55</th>
      <th>G80275</th>
      <th>PNP_Main_363</th>
      <th>SAMEA7045572</th>
      <th>SAMEA7045355</th>
      <th>HD-13</th>
      <th>EGAR00001420773_9002000001423910</th>
      <th>SID5428-4</th>
      <th>...</th>
      <th>A46_02_1FE</th>
      <th>TZ_87532</th>
      <th>A94_01_1FE</th>
      <th>KHG_7</th>
      <th>LDK_4</th>
      <th>KHG_9</th>
      <th>A48_01_1FE</th>
      <th>KHG_1</th>
      <th>TZ_81781</th>
      <th>A09_01_1FE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Bacteroidetes</th>
      <td>0.00000</td>
      <td>17.44332</td>
      <td>82.86400</td>
      <td>69.99087</td>
      <td>31.93081</td>
      <td>51.76204</td>
      <td>53.32801</td>
      <td>74.59667</td>
      <td>8.81074</td>
      <td>26.39694</td>
      <td>...</td>
      <td>1.97760</td>
      <td>1.49601</td>
      <td>67.21410</td>
      <td>4.29848</td>
      <td>68.16890</td>
      <td>38.59709</td>
      <td>14.81828</td>
      <td>10.13908</td>
      <td>57.14031</td>
      <td>11.61544</td>
    </tr>
    <tr>
      <th>Firmicutes</th>
      <td>95.24231</td>
      <td>60.47031</td>
      <td>16.53946</td>
      <td>22.81977</td>
      <td>65.23075</td>
      <td>41.96928</td>
      <td>45.77661</td>
      <td>23.51065</td>
      <td>54.35341</td>
      <td>62.23094</td>
      <td>...</td>
      <td>76.68499</td>
      <td>78.13269</td>
      <td>29.72394</td>
      <td>33.51772</td>
      <td>19.11149</td>
      <td>46.87139</td>
      <td>72.68136</td>
      <td>35.43789</td>
      <td>40.57101</td>
      <td>24.72113</td>
    </tr>
    <tr>
      <th>Proteobacteria</th>
      <td>4.49959</td>
      <td>0.77098</td>
      <td>0.05697</td>
      <td>4.07757</td>
      <td>0.27316</td>
      <td>3.33972</td>
      <td>0.02001</td>
      <td>1.72865</td>
      <td>0.00000</td>
      <td>1.81016</td>
      <td>...</td>
      <td>16.57250</td>
      <td>0.76159</td>
      <td>2.35058</td>
      <td>9.83772</td>
      <td>5.32392</td>
      <td>0.19699</td>
      <td>3.64655</td>
      <td>17.64151</td>
      <td>0.30580</td>
      <td>56.20177</td>
    </tr>
    <tr>
      <th>Actinobacteria</th>
      <td>0.25809</td>
      <td>10.27631</td>
      <td>0.45187</td>
      <td>1.11902</td>
      <td>2.31075</td>
      <td>2.92715</td>
      <td>0.77667</td>
      <td>0.16403</td>
      <td>36.55138</td>
      <td>1.19951</td>
      <td>...</td>
      <td>3.01814</td>
      <td>19.20468</td>
      <td>0.69913</td>
      <td>46.99479</td>
      <td>7.39093</td>
      <td>14.26365</td>
      <td>5.47750</td>
      <td>36.77145</td>
      <td>1.16426</td>
      <td>7.40894</td>
    </tr>
    <tr>
      <th>Verrucomicrobia</th>
      <td>0.00000</td>
      <td>0.00784</td>
      <td>0.00000</td>
      <td>1.99276</td>
      <td>0.25451</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.09940</td>
      <td>3.29795</td>
      <td>...</td>
      <td>0.05011</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 200 columns</p>
</div>

```python
modern_species = pd.read_csv("../data/curated_metagenomics/modern_sources_species.csv", index_col=0)
```

```python
modern_species.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <th>PNP_Main_283</th>
      <th>PNP_Validation_55</th>
      <th>G80275</th>
      <th>PNP_Main_363</th>
      <th>SAMEA7045572</th>
      <th>SAMEA7045355</th>
      <th>HD-13</th>
      <th>EGAR00001420773_9002000001423910</th>
      <th>SID5428-4</th>
      <th>...</th>
      <th>A46_02_1FE</th>
      <th>TZ_87532</th>
      <th>A94_01_1FE</th>
      <th>KHG_7</th>
      <th>LDK_4</th>
      <th>KHG_9</th>
      <th>A48_01_1FE</th>
      <th>KHG_1</th>
      <th>TZ_81781</th>
      <th>A09_01_1FE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Bacteroides vulgatus</th>
      <td>0.0</td>
      <td>0.60446</td>
      <td>1.59911</td>
      <td>4.39085</td>
      <td>0.04494</td>
      <td>4.66505</td>
      <td>2.99431</td>
      <td>29.30325</td>
      <td>1.48560</td>
      <td>0.98818</td>
      <td>...</td>
      <td>0.20717</td>
      <td>0.0</td>
      <td>0.00309</td>
      <td>0.48891</td>
      <td>0.00000</td>
      <td>0.02230</td>
      <td>0.00000</td>
      <td>0.15112</td>
      <td>0.0</td>
      <td>0.00836</td>
    </tr>
    <tr>
      <th>Bacteroides stercoris</th>
      <td>0.0</td>
      <td>0.00546</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>2.50789</td>
      <td>0.00000</td>
      <td>20.57498</td>
      <td>8.28443</td>
      <td>1.23261</td>
      <td>0.00000</td>
      <td>...</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.00693</td>
      <td>0.00000</td>
      <td>0.02603</td>
      <td>0.00000</td>
      <td>0.19318</td>
      <td>0.0</td>
      <td>0.00000</td>
    </tr>
    <tr>
      <th>Acidaminococcus intestini</th>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.32822</td>
      <td>0.00000</td>
      <td>...</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.00000</td>
    </tr>
    <tr>
      <th>Eubacterium sp CAG 38</th>
      <td>0.0</td>
      <td>0.06712</td>
      <td>0.81149</td>
      <td>0.05247</td>
      <td>0.26027</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>2.62415</td>
      <td>0.46585</td>
      <td>0.23372</td>
      <td>...</td>
      <td>0.78140</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.00499</td>
      <td>0.00000</td>
      <td>0.02446</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.00000</td>
    </tr>
    <tr>
      <th>Parabacteroides distasonis</th>
      <td>0.0</td>
      <td>1.34931</td>
      <td>2.00672</td>
      <td>5.85067</td>
      <td>0.59019</td>
      <td>7.00027</td>
      <td>1.28075</td>
      <td>0.61758</td>
      <td>0.07383</td>
      <td>2.80355</td>
      <td>...</td>
      <td>0.11423</td>
      <td>0.0</td>
      <td>0.01181</td>
      <td>0.01386</td>
      <td>0.03111</td>
      <td>0.07463</td>
      <td>0.15597</td>
      <td>0.07541</td>
      <td>0.0</td>
      <td>0.01932</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 200 columns</p>
</div>

Now, let's merge our ancient sample with the modern data in one single table

```python
all_species = ancient_species.merge(modern_species, left_index=True, right_index=True, how='outer').fillna(0)
all_phylums = ancient_phylums.merge(modern_phylums, left_index=True, right_index=True, how='outer').fillna(0)
```

Finally, let's load the metadata

```python
metadata = pd.read_csv("../data/metadata/curated_metagenomics_modern_sources.csv")
```

```python
metadata.head()
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>study_name</th>
      <th>sample_id</th>
      <th>subject_id</th>
      <th>body_site</th>
      <th>antibiotics_current_use</th>
      <th>study_condition</th>
      <th>disease</th>
      <th>age</th>
      <th>infant_age</th>
      <th>age_category</th>
      <th>...</th>
      <th>hla_drb11</th>
      <th>birth_order</th>
      <th>age_twins_started_to_live_apart</th>
      <th>zigosity</th>
      <th>brinkman_index</th>
      <th>alcohol_numeric</th>
      <th>breastfeeding_duration</th>
      <th>formula_first_day</th>
      <th>ALT</th>
      <th>eGFR</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ShaoY_2019</td>
      <td>de028ad4-7ae6-11e9-a106-68b59976a384</td>
      <td>C01528_ba</td>
      <td>stool</td>
      <td>no</td>
      <td>control</td>
      <td>healthy</td>
      <td>0.0</td>
      <td>4.0</td>
      <td>newborn</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ZeeviD_2015</td>
      <td>PNP_Main_283</td>
      <td>PNP_Main_283</td>
      <td>stool</td>
      <td>no</td>
      <td>control</td>
      <td>healthy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>adult</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ZeeviD_2015</td>
      <td>PNP_Validation_55</td>
      <td>PNP_Validation_55</td>
      <td>stool</td>
      <td>no</td>
      <td>control</td>
      <td>healthy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>adult</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>VatanenT_2016</td>
      <td>G80275</td>
      <td>T014806</td>
      <td>stool</td>
      <td>no</td>
      <td>control</td>
      <td>healthy</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>child</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ZeeviD_2015</td>
      <td>PNP_Main_363</td>
      <td>PNP_Main_363</td>
      <td>stool</td>
      <td>no</td>
      <td>control</td>
      <td>healthy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>adult</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 130 columns</p>
</div>

##### 7. Comparing ancient and modern samples

###### 7.1 Taxonomic composition

One common plot in microbiome papers in a stacked barplot, often at the phylum or family level.

First, we'll do some renaming, to make the value of the metadata variables a bit easier to understand

```python
group_info = (
    metadata['non_westernized']
    .map({'no':'westernized','yes':'non_westernized'}) # for the non_westernized in the modern sample metadata, rename the value levels
    .to_frame(name='group').set_index(metadata['sample_id']) # rename the column to group
    .reset_index()
    .append({'sample_id':'ERR5766177', 'group':'ancient'}, ignore_index=True) # add the ancient sample
)
group_info
```

    /var/folders/1c/l1qb09f15jddsh65f6xv1n_r0000gp/T/ipykernel_40830/27419655.py:2:
    FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version.
    Use pandas.concat instead.
      metadata['non_westernized']

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sample_id</th>
      <th>group</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>de028ad4-7ae6-11e9-a106-68b59976a384</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PNP_Main_283</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PNP_Validation_55</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>3</th>
      <td>G80275</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PNP_Main_363</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>196</th>
      <td>A48_01_1FE</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>197</th>
      <td>KHG_1</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>198</th>
      <td>TZ_81781</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>199</th>
      <td>A09_01_1FE</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>200</th>
      <td>ERR5766177</td>
      <td>ancient</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 2 columns</p>
</div>

We need transform our data in [tidy](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html) format to
plot with [plotnine](https://plotnine.readthedocs.io/en/stable/), a python clone of [ggplot](https://ggplot2.tidyverse.org/index.html).  
We then add the group information (Westernized, non westernized, or ancient sample), and compute the mean abundance for each phylum.

First we transpose the dataframe to have the samples as index, and the phylums as columns

We then add the metadata information

```python
(
    all_phylums
    .transpose()
    .merge(group_info, left_index=True, right_on='sample_id')
)
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actinobacteria</th>
      <th>Apicomplexa</th>
      <th>Ascomycota</th>
      <th>Bacteroidetes</th>
      <th>Basidiomycota</th>
      <th>Candidatus Melainabacteria</th>
      <th>Chlamydiae</th>
      <th>Chloroflexi</th>
      <th>Cyanobacteria</th>
      <th>Deferribacteres</th>
      <th>...</th>
      <th>Fusobacteria</th>
      <th>Lentisphaerae</th>
      <th>Planctomycetes</th>
      <th>Proteobacteria</th>
      <th>Spirochaetes</th>
      <th>Synergistetes</th>
      <th>Tenericutes</th>
      <th>Verrucomicrobia</th>
      <th>sample_id</th>
      <th>group</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>200</th>
      <td>20.33151</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>28.42090</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>ERR5766177</td>
      <td>ancient</td>
    </tr>
    <tr>
      <th>0</th>
      <td>0.25809</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>4.49959</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>de028ad4-7ae6-11e9-a106-68b59976a384</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.27631</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>17.44332</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.01486</td>
      <td>0.0</td>
      <td>0.77098</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00784</td>
      <td>PNP_Main_283</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.45187</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>82.86400</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.05697</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>PNP_Validation_55</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.11902</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>69.99087</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>4.07757</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.99276</td>
      <td>G80275</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>195</th>
      <td>14.26365</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>38.59709</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.19699</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>KHG_9</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>196</th>
      <td>5.47750</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>14.81828</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>3.64655</td>
      <td>0.09964</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>A48_01_1FE</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>197</th>
      <td>36.77145</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>10.13908</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>17.64151</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>KHG_1</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>198</th>
      <td>1.16426</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>57.14031</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.30580</td>
      <td>0.70467</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>TZ_81781</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>199</th>
      <td>7.40894</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>11.61544</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>56.20177</td>
      <td>0.00000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00000</td>
      <td>A09_01_1FE</td>
      <td>non_westernized</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 24 columns</p>
</div>

Now, we need it in the tidy format

```python
tidy_phylums = (
    all_phylums
    .transpose()
    .merge(group_info, left_index=True, right_on='sample_id')
    .melt(id_vars=['sample_id', 'group'], value_name='relative_abundance', var_name='Phylum', ignore_index=True)
)
```

Finally, we only want to keep the mean relative abundance for each phylum

```python
tidy_phylums = tidy_phylums.groupby(['group', 'Phylum']).mean().reset_index()
```

```python
tidy_phylums.groupby('group')['relative_abundance'].sum()
```

    group
    ancient            100.000000
    non_westernized     99.710255
    westernized         99.905089
    Name: relative_abundance, dtype: float64

```python
from plotnine import *
```

```python
ggplot(tidy_phylums, aes(x='group', y='relative_abundance', fill='Phylum')) \
+ geom_bar(position='stack', stat='identity') \
+ ylab('mean abundance') \
+ xlab("") \
+ theme_classic()
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_80_0.png)

    <ggplot: (406187548)>

###### 7.2 Ecological diversity

####### 7.2.1 Alpha diversity

Alpha diversity is the measure of diversity withing each sample. It is used to estimate how many species are present in a sample, and how diverse they are.  
We'll use the python library [scikit-bio](http://scikit-bio.org/) to compute it, and the [plotnine](https://plotnine.readthedocs.io/) library
(a python port of [ggplot2](https://ggplot2.tidyverse.org/reference/ggplot.html) to visualize the results).

```python
import skbio
```

Let's compute the [species richness](https://en.wikipedia.org/wiki/Species_richness), the
[Shannon, and Simpson index of diversity](https://www.biologydiscussion.com/biodiversity/types/2-types-of-diversity-indices-of-biodiversity/8388) index

```python
shannon = skbio.diversity.alpha_diversity(metric='shannon', counts=all_species.transpose(), ids=all_species.columns)
simpson = skbio.diversity.alpha_diversity(metric='simpson', counts=all_species.transpose(), ids=all_species.columns)
richness = (all_species != 0).astype(int).sum(axis=0)
alpha_diversity = (shannon.to_frame(name='shannon')
                   .merge(simpson.to_frame(name='simpson'), left_index=True, right_index=True)
                   .merge(richness.to_frame(name='richness'), left_index=True, right_index=True))
alpha_diversity
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>shannon</th>
      <th>simpson</th>
      <th>richness</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>ERR5766177</th>
      <td>3.032945</td>
      <td>0.844769</td>
      <td>21</td>
    </tr>
    <tr>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <td>0.798112</td>
      <td>0.251280</td>
      <td>11</td>
    </tr>
    <tr>
      <th>PNP_Main_283</th>
      <td>5.092878</td>
      <td>0.954159</td>
      <td>118</td>
    </tr>
    <tr>
      <th>PNP_Validation_55</th>
      <td>3.670162</td>
      <td>0.812438</td>
      <td>72</td>
    </tr>
    <tr>
      <th>G80275</th>
      <td>3.831358</td>
      <td>0.876712</td>
      <td>66</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>KHG_9</th>
      <td>3.884285</td>
      <td>0.861683</td>
      <td>87</td>
    </tr>
    <tr>
      <th>A48_01_1FE</th>
      <td>4.377755</td>
      <td>0.930024</td>
      <td>53</td>
    </tr>
    <tr>
      <th>KHG_1</th>
      <td>3.733834</td>
      <td>0.875335</td>
      <td>108</td>
    </tr>
    <tr>
      <th>TZ_81781</th>
      <td>2.881856</td>
      <td>0.719491</td>
      <td>44</td>
    </tr>
    <tr>
      <th>A09_01_1FE</th>
      <td>2.982322</td>
      <td>0.719962</td>
      <td>75</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 3 columns</p>
</div>

Let's load the group information from the metadata

```python
alpha_diversity = (
    alpha_diversity
    .merge(metadata[['sample_id', 'non_westernized']], left_index=True, right_on='sample_id', how='outer')
    .set_index('sample_id')
    .rename(columns={'non_westernized':'group'})
)
alpha_diversity['group'] = alpha_diversity['group'].replace({'yes':'non_westernized','no':'westernized', pd.NA:'ERR5766177'})
```

```python
alpha_diversity
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>shannon</th>
      <th>simpson</th>
      <th>richness</th>
      <th>group</th>
    </tr>
    <tr>
      <th>sample_id</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>ERR5766177</th>
      <td>3.032945</td>
      <td>0.844769</td>
      <td>21</td>
      <td>ERR5766177</td>
    </tr>
    <tr>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <td>0.798112</td>
      <td>0.251280</td>
      <td>11</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>PNP_Main_283</th>
      <td>5.092878</td>
      <td>0.954159</td>
      <td>118</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>PNP_Validation_55</th>
      <td>3.670162</td>
      <td>0.812438</td>
      <td>72</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>G80275</th>
      <td>3.831358</td>
      <td>0.876712</td>
      <td>66</td>
      <td>westernized</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>KHG_9</th>
      <td>3.884285</td>
      <td>0.861683</td>
      <td>87</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>A48_01_1FE</th>
      <td>4.377755</td>
      <td>0.930024</td>
      <td>53</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>KHG_1</th>
      <td>3.733834</td>
      <td>0.875335</td>
      <td>108</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>TZ_81781</th>
      <td>2.881856</td>
      <td>0.719491</td>
      <td>44</td>
      <td>non_westernized</td>
    </tr>
    <tr>
      <th>A09_01_1FE</th>
      <td>2.982322</td>
      <td>0.719962</td>
      <td>75</td>
      <td>non_westernized</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 4 columns</p>
</div>

```python
alpha_diversity = alpha_diversity.melt(id_vars='group', value_name='alpha diversity', var_name='diversity_index', ignore_index=False)
```

```python
alpha_diversity
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>group</th>
      <th>diversity_index</th>
      <th>alpha diversity</th>
    </tr>
    <tr>
      <th>sample_id</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>ERR5766177</th>
      <td>ERR5766177</td>
      <td>shannon</td>
      <td>3.032945</td>
    </tr>
    <tr>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <td>westernized</td>
      <td>shannon</td>
      <td>0.798112</td>
    </tr>
    <tr>
      <th>PNP_Main_283</th>
      <td>westernized</td>
      <td>shannon</td>
      <td>5.092878</td>
    </tr>
    <tr>
      <th>PNP_Validation_55</th>
      <td>westernized</td>
      <td>shannon</td>
      <td>3.670162</td>
    </tr>
    <tr>
      <th>G80275</th>
      <td>westernized</td>
      <td>shannon</td>
      <td>3.831358</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>KHG_9</th>
      <td>non_westernized</td>
      <td>richness</td>
      <td>87.000000</td>
    </tr>
    <tr>
      <th>A48_01_1FE</th>
      <td>non_westernized</td>
      <td>richness</td>
      <td>53.000000</td>
    </tr>
    <tr>
      <th>KHG_1</th>
      <td>non_westernized</td>
      <td>richness</td>
      <td>108.000000</td>
    </tr>
    <tr>
      <th>TZ_81781</th>
      <td>non_westernized</td>
      <td>richness</td>
      <td>44.000000</td>
    </tr>
    <tr>
      <th>A09_01_1FE</th>
      <td>non_westernized</td>
      <td>richness</td>
      <td>75.000000</td>
    </tr>
  </tbody>
</table>
<p>603 rows × 3 columns</p>
</div>

```python
g = ggplot(alpha_diversity, aes(x='group', y='alpha diversity', color='group'))
g += geom_violin()
g += geom_jitter()
g += theme_classic()
g += facet_wrap('~diversity_index', scales = 'free')
g += theme(axis_text_x=element_text(rotation=45, hjust=1))
g += scale_color_manual({'ERR5766177':'#DB5F57','westernized':'#5F57DB','non_westernized':'#57DB5E'})
g += theme(subplots_adjust={'wspace': 0.15})
g
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_91_1.png)

    <ggplot: (407407577)>

**Pause and think: Why do we observe a smaller species richness and diversity in our sample ?**

###### 7.2.2 Beta diversity

The Beta diversity is the measure of diversity between a pair of samples. It is used to compare the diversity between samples and see how they relate.

We will compute the beta diversity using the [bray-curtis](https://en.wikipedia.org/wiki/Bray%E2%80%93Curtis_dissimilarity) dissimilarity

```python
beta_diversity = skbio.diversity.beta_diversity(metric='braycurtis', counts=all_species.transpose(), ids=all_species.columns, validate=True)
```

We get a distance matrix

```python
print(beta_diversity)
```

    201x201 distance matrix
    IDs:
    'ERR5766177', 'de028ad4-7ae6-11e9-a106-68b59976a384', 'PNP_Main_283', ...
    Data:
    [[0.         1.         0.81508134 ... 0.85716612 0.69790092 0.8303726 ]
     [1.         0.         0.99988327 ... 0.99853413 0.994116   0.99877258]
     [0.81508134 0.99988327 0.         ... 0.82311942 0.87202543 0.91363156]
     ...
     [0.85716612 0.99853413 0.82311942 ... 0.         0.84253376 0.76616679]
     [0.69790092 0.994116   0.87202543 ... 0.84253376 0.         0.82409272]
     [0.8303726  0.99877258 0.91363156 ... 0.76616679 0.82409272 0.        ]]

To visualize this distance matrix in a lower dimensional space, we'll use a [PCoA](https://en.wikipedia.org/wiki/Multidimensional_scaling#Types), which is is a method very similar to a PCA, but taking a distance matrix as input.

```python
pcoa = skbio.stats.ordination.pcoa(beta_diversity)
```

    /Users/maxime/mambaforge/envs/summer_school_microbiome/lib/python3.9/site-packages/skbio/stats/ordination/_principal_coordinate_analysis.py:143: RuntimeWarning:
    The result contains negative eigenvalues. Please compare their magnitude with the magnitude of some of the largest positive eigenvalues.
    If the negative ones are smaller, it's probably safe to ignore them, but if they are large in magnitude, the results won't be useful.
    See the Notes section for more details. The smallest eigenvalue is -0.25334842745723996 and the largest is 10.204440747987945.

```python
pcoa.samples
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PC1</th>
      <th>PC2</th>
      <th>PC3</th>
      <th>PC4</th>
      <th>PC5</th>
      <th>PC6</th>
      <th>PC7</th>
      <th>PC8</th>
      <th>PC9</th>
      <th>PC10</th>
      <th>...</th>
      <th>PC192</th>
      <th>PC193</th>
      <th>PC194</th>
      <th>PC195</th>
      <th>PC196</th>
      <th>PC197</th>
      <th>PC198</th>
      <th>PC199</th>
      <th>PC200</th>
      <th>PC201</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>ERR5766177</th>
      <td>0.216901</td>
      <td>-0.039778</td>
      <td>0.107412</td>
      <td>0.273272</td>
      <td>0.020540</td>
      <td>0.114876</td>
      <td>-0.256332</td>
      <td>-0.151069</td>
      <td>0.097451</td>
      <td>0.060211</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>de028ad4-7ae6-11e9-a106-68b59976a384</th>
      <td>-0.099355</td>
      <td>0.145224</td>
      <td>-0.191676</td>
      <td>0.127626</td>
      <td>0.119754</td>
      <td>-0.132209</td>
      <td>-0.097382</td>
      <td>0.036728</td>
      <td>0.081294</td>
      <td>-0.056686</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>PNP_Main_283</th>
      <td>-0.214108</td>
      <td>-0.147466</td>
      <td>0.116027</td>
      <td>0.090059</td>
      <td>0.076644</td>
      <td>0.111536</td>
      <td>0.092115</td>
      <td>0.026477</td>
      <td>-0.006460</td>
      <td>-0.018592</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>PNP_Validation_55</th>
      <td>0.244827</td>
      <td>-0.173996</td>
      <td>-0.311197</td>
      <td>-0.012836</td>
      <td>0.031759</td>
      <td>0.117548</td>
      <td>0.148715</td>
      <td>-0.135641</td>
      <td>0.034730</td>
      <td>-0.009395</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>G80275</th>
      <td>-0.261358</td>
      <td>-0.077147</td>
      <td>-0.254374</td>
      <td>-0.065932</td>
      <td>0.088538</td>
      <td>0.165970</td>
      <td>-0.005260</td>
      <td>-0.028739</td>
      <td>-0.002016</td>
      <td>0.015719</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>KHG_9</th>
      <td>0.296057</td>
      <td>-0.150300</td>
      <td>0.013941</td>
      <td>0.032649</td>
      <td>-0.147692</td>
      <td>0.019663</td>
      <td>-0.063120</td>
      <td>-0.034453</td>
      <td>-0.073514</td>
      <td>0.070085</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>A48_01_1FE</th>
      <td>0.110621</td>
      <td>0.030971</td>
      <td>0.154231</td>
      <td>-0.185961</td>
      <td>-0.008512</td>
      <td>-0.103420</td>
      <td>0.028169</td>
      <td>-0.044530</td>
      <td>0.041902</td>
      <td>0.068597</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>KHG_1</th>
      <td>-0.100009</td>
      <td>0.167885</td>
      <td>0.009915</td>
      <td>0.076842</td>
      <td>-0.405582</td>
      <td>-0.039111</td>
      <td>-0.006421</td>
      <td>-0.009774</td>
      <td>-0.072252</td>
      <td>0.150000</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>TZ_81781</th>
      <td>0.405716</td>
      <td>-0.139297</td>
      <td>-0.075026</td>
      <td>-0.079716</td>
      <td>-0.053264</td>
      <td>-0.119271</td>
      <td>0.068261</td>
      <td>-0.018821</td>
      <td>0.198152</td>
      <td>-0.012792</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>A09_01_1FE</th>
      <td>0.089101</td>
      <td>0.471135</td>
      <td>0.069629</td>
      <td>-0.125644</td>
      <td>-0.036793</td>
      <td>0.115151</td>
      <td>0.060507</td>
      <td>-0.000912</td>
      <td>-0.027239</td>
      <td>-0.138436</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 201 columns</p>
</div>

Let's look at the variance explained by the first axes by using a scree plot

```python
var_explained = pcoa.proportion_explained[:9].to_frame(name='variance explained').reset_index().rename(columns={'index':'PC'})
```

```python
ggplot(var_explained, aes(x='PC', y='variance explained', group=1)) \
+ geom_point() \
+ geom_line() \
+ theme_classic()
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_102_0.png)

    <ggplot: (407531271)>

In this scree plot, we're looking for the "elbow", where there is a drop in the slope. Here, it seems that most of the variance is captures by the 3 first principal components

```python
pcoa_embed = pcoa.samples[['PC1','PC2','PC3']].rename_axis('sample').reset_index()
```

```python
pcoa_embed = (
    pcoa_embed
    .merge(metadata[['sample_id', 'non_westernized']], left_on='sample', right_on='sample_id', how='outer')
    .drop('sample_id', axis=1)
    .rename(columns={'non_westernized':'group'})
)
pcoa_embed['group'] = pcoa_embed['group'].replace({'yes':'non_westernized','no':'westernized', pd.NA:'ERR5766177'})
```

Let's first look at these components with 2D plots

```python
ggplot(pcoa_embed, aes(x='PC1', y='PC2', color='group')) \
+ geom_point() \
+ theme_classic() \
+ scale_color_manual({'ERR5766177':'#DB5F57','westernized':'#5F57DB','non_westernized':'#57DB5E'})
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_107_0.png)

    <ggplot: (407572134)>

```python
ggplot(pcoa_embed, aes(x='PC1', y='PC3', color='group')) +
geom_point() +
theme_classic() +
scale_color_manual({'ERR5766177':'#DB5F57','westernized':'#5F57DB','non_westernized':'#57DB5E'})
```

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_108_0.png)

    <ggplot: (407612651)>

Then with a 3d plot

```python
import plotly.express as px

fig = px.scatter_3d(pcoa_embed, x="PC1", y="PC2", z="PC3",
                  color = "group",
                  color_discrete_map={'ERR5766177':'#DB5F57','westernized':'#5F57DB','non_westernized':'#57DB5E'},
                  hover_name="sample")
fig.show()
```

> ⚠️ 3D PLOT HERE NOT DISPLAYED DUE TO RENDERING LIMITATIONS - PLEASE SEE JUPYTER NOTEBOOK

**Pause and think: How do you think this embedding represents how our sample relates to modern reference samples ?**

We can also visualize this distance matrix using a clustered heatmap, where pairs of sample with a small beta diversity are clustered together

```python
import seaborn as sns
import scipy.spatial as sp, scipy.cluster.hierarchy as hc
```

```python
pcoa_embed['colour'] = pcoa_embed['group'].map({'ERR5766177':'#DB5F57','westernized':'#5F57DB','non_westernized':'#57DB5E'})
```

```python
linkage = hc.linkage(sp.distance.squareform(beta_diversity.to_data_frame()), method='average')

sns.clustermap(
    beta_diversity.to_data_frame(),
    row_linkage=linkage,
    col_linkage=linkage,
    row_colors = pcoa_embed['colour'].to_list()
)
```

    <seaborn.matrix.ClusterGrid at 0x185b56100>

![png](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/3c-intro-to-taxprofiling/analysis_files/analysis_115_1.png)

##### 8. Additional steps

###### 8.1 Source tracking

Sourcetracker is a program that can estimate the proportion of different sources (reference biomes) contained in a sample (a sink).
However, because of the statistical framework that it uses (MCMC with [Gibbs sampling](https://en.wikipedia.org/wiki/Gibbs_sampling#:~:text=In%20statistics%2C%20Gibbs%20sampling%20or,when%20direct%20sampling%20is%20difficult.)), we recommend to limit the number of source samples to greatly reduce runtime

First, you will need to transform our relative abundance table to counts for SourceTracker

```python
all_species_counts = all_species.multiply(1000000).astype(int)
```

```python
min_count = all_species_counts.sum(axis=0).min()
min_count
```

    95327810

Exporting the count table to `tsv`

```python
all_species_counts.to_csv("../results/sourcetracker2/all_species_counts.tsv", sep="\t", index_label='Taxon')
```

Converting to [`biom` format](https://biom-format.org/)

```python
!biom convert -i ../results/sourcetracker2/all_species_counts.tsv \
-o ../results/sourcetracker2/all_species_counts.biom \
--table-type="Taxon table" --to-hdf5
```

Converting the metadata to Sourtracker format

```python
st2_metadata = metadata[['sample_id', 'non_westernized']].rename(columns={'non_westernized':'Env', 'sample_id':'#SampleID'})
st2_metadata['Env'] = st2_metadata['Env'].replace({'yes':'non_westernized','no':'westernized'})
st2_metadata['SourceSink'] = ['source'] * st2_metadata.shape[0]
```

We subset it to select only 10 samples from each source

```python
st2_metadata = st2_metadata.groupby('Env').sample(10).reset_index()
```

```python
st2_metadata = st2_metadata.append({'#SampleID':'ERR5766177', 'Env':'-','SourceSink':'sink'},
                                   ignore_index=True)[['#SampleID','SourceSink','Env']].set_index('#SampleID')
```

    /var/folders/1c/l1qb09f15jddsh65f6xv1n_r0000gp/T/ipykernel_40830/2882312005.py:1: FutureWarning:

    The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.

```python
st2_metadata.to_csv("../results/sourcetracker2/labels_st2.tsv", sep="\t", index_label='#SampleID')
```

```bash
sourcetracker2 gibbs \
    -i ../results/sourcetracker2/all_species_counts.biom \
    -m ../results/sourcetracker2/labels_st2.tsv \
    -o ../results/sourcetracker2/st2 \
    --source_rarefaction_depth 95327810 \
    --sink_rarefaction_depth 95327810 \
    --jobs 10
```

**Because SourceTracker is relying on MCMC sampling, it can very slow to run (which is why we won't run it here)**

Among alternative faster solutions for source tracking are (among others):

- FEAST ([article](https://doi.org/10.1038/s41592-019-0431-x), [code](https://github.com/cozygene/FEAST)),
- Sourcepredict ([article](https://doi.org/10.21105/joss.01540), [code](https://github.com/maxibor/sourcepredict))

###### 8.2 The next steps:

- Damage Analysis ([mapDamage](https://ginolhac.github.io/mapDamage/), [DamageProfiler](https://github.com/Integrative-Transcriptomics/DamageProfiler), [PyDamage](https://github.com/maxibor/pydamage))
- Assembly ([megahit](https://github.com/voutcn/megahit), [metaSPAdes](https://github.com/ablab/spades)), binning ([metabat2](https://bitbucket.org/berkeleylab/metabat/src/master/), [maxbin2](https://sourceforge.net/projects/maxbin2/), [dastool](https://github.com/cmks/DAS_Tool)), and bin validation ([checkm](https://github.com/Ecogenomics/CheckM), [gunc](https://github.com/grp-bork/gunc))
- Functional analysis ([Prokka](https://github.com/tseemann/prokka), [Humann](https://github.com/biobakery/humann))
- Differential abundance ([Maaslin2](https://github.com/biobakery/Maaslin2), [Lefse](https://github.com/biobakery/lefse), [Songbird](https://github.com/biocore/songbird), GLM, Mixed effect models). Nice review by [Wallen 2021](https://doi.org/10.1186/s12859-021-04193-6)
- genotyping
- Phylogenies
- ...

</div>

</details>

---

### Resources

### Readings

### Questions to think about

### Roundtable: Taxonomic Classifers

**Chairs**: Irina Velsko and James Fellows Yates

Which taxonomic classifier to pick is a context dependent question. Each classifier will has it's advantages and disadvantages depending on the type of data you have, and what research question you have. In this round table participants can ask for advice as to what to consider when selecting a particular classifier or classifiers for their projects.
