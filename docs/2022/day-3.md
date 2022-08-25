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

### Slides

<iframe src="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/nevrome/spaam_r_tidyverse_intro_2h/main/presentation.pdf&embedded=true" width="960" height="569"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/nevrome/spaam_r_tidyverse_intro_2h/raw/main/presentation.pdf).

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
