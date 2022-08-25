# Day Five

## Lecture 5A: Evolutionary Biology

**Instructors**: Sebastian Duchene

**Abstract**: Pathogen genome data are an invaluable source of information about the evolution and spread of these organisms. This talk will focus on molecular phylogenetic methods and the insight that they can reveal from improving our understanding of ancient evolution to the epidemiological dynamics of current outbreaks.

The first section will introduce phylognenetic trees and a set of core terms and concepts for their interpretation. Next, it will focus on some of the most popular approaches to inferring phylogenetic trees; those based on genetic distance, maximum likelihood, and Bayesian inference. These methods carry important considerations regarding the process that generated the data, computational capability, and data quality, all of which will be discussed here. Finally, we will direct our attention to examples of analyses of ancient and modern pathogens (e.g. Yersinia pestis, Hepatitis B virus, SARS-CoV-2) and critically assess appropriate choice of models and methods.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vT3-tOQI6WIaZ6nUt-23Dl03me7tuyTkSCq-tad2KRrs5MqF92Ufsr3p1Ddsa5U_3Zr_7rDW5SnYOiS/embed?start=false&loop=true&delayms=3000" frameborder="0" width="1058" height="624" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5a-intro-to-evobio/SPAAM%20Summer%20School%202022%20-%205A%20-%20Evolutionary%20Biology%20and%20Phylogenetics.pdf).

### Resources

### Readings

### Questions to think about

## Software

For today's practical sessions, please [activate](2022/resources#software-and-data) the `phylogenomics-functional` conda [environment](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day5.yml).

```bash
conda activate phylogenomics-functional
```

## Practical 5B: Phylogenomics

**Instructors**: Aida Andrades Valtueña and Arthur Kocher

**Abstract**: Phylogenetic trees are central tools for studying the evolution of microorganisms, as they provide essential information about their relationships and timing of divergence between microbial strains.

In this session, we will introduce basic phylogenetic concepts and definitions, and provide guidance on how to interpret phylogenetic trees. We will then learn how to reconstruct phylogenetic trees from DNA sequences using various methods ranging from distance-based methods to probabilistic approaches, including maximum likelihood and Bayesian phylogenetics. In particular, we will learn how to use ancient genomic data to reconstruct time-calibrated trees with BEAST2.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSexn0hc-7Qt2o5jarBzZ3WMLZ4jcjj0fd_QgLYpm5y0tNC_KLnMT00pA6uvpOomQ/embed?start=false&loop=true&delayms=10000" frameborder="0" width="1280" height="749" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/SPAAM%20Summer%20School%202022%20-%205B%20-%20Phylogenomics.pdf).

### Resources

### Readings

### Questions to think about

## Practical 5C: Functional Genomics

**Instructors**: Irina Velsko and James Fellows Yates

**Abstract**: The value of microbial taxonomy lies in the implied biochemical properties of a given taxon. Historically taxonomy was determined by growth characteristics and cell properties, and more recently through genomic and genetic similarity. The genomic content of microbial taxa, specifically the presence or absence of genes, determine how those taxa interact with their environment, including all the biochemical processes they participate in, both internally and externally. Strains within any microbial species may have different genetic content and therefore may behave strikingly differently in the same environment, which cannot be determined through taxonomic profiling. Functionally profiling a microbial community, or determining all of the genes present independent of the species they are derived from, reveals the biochemical reactions and metabolic products the community may perform and produce, respectively. This approach may provide insights to community activity and environmental interactions that are hidden when using taxonomic approaches alone. In this session we will perform functional profiling of metagenomic communities to assess their genetic content and inferred metabolic pathways.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTbQRU__-fDvsJ09fd1KeZxGRDrtLD8Ab0ZLagN-4s9CKDfv4ekJlyv4RdQBkBPFj4hdjhY1Un4dRAg/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5c-intro-to-functional-analysis/SPAAM%20Summer%20School%202022%20-%205C%20-%20Function%20Analysis.pdf).

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>
        <div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.6983188](https://doi.org/10.5281/zenodo.6983188). See instructions on page.

Change into the session directory

```bash
cd /<path>/<to>/5c-functional-genomics/
```

Load the conda environment.

```bash
conda activate phylogenomics-functional
```

Open R Studio from within the conda environment, and we can load the required libraries for this walkthrough.

```r
library(mixOmics) ## For PCA generation

## Utility packages (pretty stuff)
library(knitr)
library(data.table)
library(tidyverse)
library(gplots)
library(ggrepel)
library(viridis)
library(patchwork)
```

#### HUMAnN3 Pathways

First, we need to run HUMMAn3 to align reads against gene databases and convert to gene family names counts.

Note: we will not run HUMANn3 here as it requires very large databases and takes a long time to run, so we will give you the commands
you normally would run but we provide with you pre-made results files before you (see below).

```bash
## DO NOT RUN!

# run humann3
humann3 --input file.fastq --output output --threads <threads>

# join all output tables (can do for both gene and pathways)
humann_join_tables -i output/ -o genefamilies_joined.tsv --file_name unmapped_genefamilies

# normalize the output (here by tss - total sum scaling, can do for both gene and pathways)
humann_renorm_table --input genefamilies_joined.tsv --output genefamilies_joined_cpm.tsv --units tss

# regroup the table to combine gene families (standardise gene family IDs across taxa)
humann_regroup_table --input genefamilies_joined_cpm.tsv --output genefamilies_joined_cpm_ur90rxn.tsv --groups uniref90_rxn

# give the gene families names
humann_rename_table --input genefamilies_joined_cpm_ur90rxn.tsv --output genefamilies_joined_cpm_ur90rxn_names.tsv -n metacyc-rxn
```

#### humann3 tables

First lets load a pre-made pathway abundance file

```r
## load the species and genus tables generated with humann3
humann3_path_full <- fread("./pathabundance_joined_cpm.tsv")
humann3_path_full <- as_tibble(humann3_path_full)

# clean the file names
humann3_path_full <- rename(humann3_path_full, Pathway = `# Pathway`)
colnames(humann3_path_full) <- gsub(".unmapped_Abundance","", colnames(humann3_path_full))
colnames(humann3_path_full) <- gsub(".SG1","", colnames(humann3_path_full))

# remove unmapped and ungrouped reads
humann3_path <- humann3_path_full %>% filter(!str_detect(Pathway, "UNMAPPED|UNINTEGRATED"))

```

Then lets load associated sample metadata to help make it easier for comparative analysis and make actual informative inferences.

The data being used in this session, is from [Velsko et al. 2022 (PNAS Nexus)](https://doi.org/10.1093/pnasnexus/pgac148), where we tried to find associations between dental pathologies and taxonomic and genome content. We had a large skeletal collection from a single site in the Netherlands, with a lot of osteological metadata. The study aimed to see if there were any links between the oral microbiome and groups of dental pathologies.

```r
# load the metadata file
full_metadata <- fread("full_combined_metadata.tsv")


## Example of metadata
tibble(full_metadata %>%
    filter(Site_code == "MID") %>%
    select(Site, Time_period, Library_ID, Sequencing_instrument, Pipenotch, Max_Perio_Score, `%teeth_with_caries`))

```

First step: we can pre-define various functions for generate PCAs we will use downstream - you don't have to worry about these too much they are just custom functions to quickly plot PCAs from a `mixOmics` PCA output object with ggplot, but we leave the code here for if you're curious.

```r
# plot PCA with colored dots and the title including the # of species or genera
plot_pca <- function(df, pc1, pc2, color_group, shape_group, ncomps) {
    metadata_group_colors <- get(paste(color_group, "_colors", sep = ""))
    metadata_group_shapes <- get(paste(shape_group, "_shapes", sep = ""))

    pca.list <- mixOmics::pca(df, ncomp = ncomps, logratio = 'CLR')

    ## Pull out loadings
    exp_var <- paste0(round(pca.list$explained_variance * 100, 2), "%")
    df_X <- pca.list$variates$X %>%
              as.data.frame() %>%
              rownames_to_column("Library_ID") %>%
              inner_join(full_metadata, by = "Library_ID")

    color_group = df_X[[color_group]]
    shape_group = df_X[[shape_group]]

    ## Selecting which PCs to plot
    if (pc1 == 'PC1') {
        pc1 <- df_X$PC1
        exp_var_pc1 <- exp_var[1]
        xaxis <- c("PC1")
    }  else if (pc1 == 'PC2') {
        pc1 <- df_X$PC2
        exp_var_pc1 <- exp_var[2]
        xaxis <- c("PC2")
    } else if (pc1 == 'PC3') {
        pc1 <- df_X$PC3
        exp_var_pc1 <- exp_var[3]
        xaxis <- c("PC3")
    }

    if (pc2 == 'PC1') {
        pc2 <- df_X$PC1
        exp_var_pc2 <- exp_var[1]
        yaxis <- c("PC1")
    }  else if (pc2 == 'PC2') {
        pc2 <- df_X$PC2
        exp_var_pc2 <- exp_var[2]
        yaxis <- c("PC2")
    } else if (pc2 == 'PC3') {
        pc2 <- df_X$PC3
        exp_var_pc2 <- exp_var[3]
        yaxis <- c("PC3")
    }

    ## Generate figure
    pca_plot <- ggplot(df_X, aes(pc1, pc2)) +
     geom_point(aes(fill = color_group, shape = shape_group), size = 4.5, stroke = 0.3) +
     scale_fill_manual(values = metadata_group_colors) +
     scale_shape_manual(values = metadata_group_shapes) +
     # stat_ellipse() +
     xlab(paste(xaxis, " - ", exp_var_pc1)) +
     ylab(paste(yaxis, " - ", exp_var_pc2)) +
     theme_minimal(base_size = 16) +
     theme(text = element_text(size=16)) +
     theme(legend.title = element_blank(),
           legend.key.size = unit(2,"mm"),
           legend.text = element_text(size = 6)) +
     theme(legend.position = "top")

    return(pca_plot)
}

# for continuous data
plot_pca_cont <- function(df, pc1, pc2, color_group, shape_group, ncomps, title_text) {

    pca.list <- mixOmics::pca(df, ncomp = ncomps, logratio = 'CLR')

    exp_var <- paste0(round(pca.list$explained_variance * 100, 2), "%")
    df_X <- pca.list$variates$X %>%
              as.data.frame() %>%
              rownames_to_column("Library_ID") %>%
              inner_join(full_metadata, by = "Library_ID")

    color_group = df_X[[color_group]]
    shape_group = df_X[[shape_group]]

    if (pc1 == 'PC1') {
        pc1 <- df_X$PC1
        exp_var_pc1 <- exp_var[1]
        xaxis <- c("PC1")
    }  else if (pc1 == 'PC2') {
        pc1 <- df_X$PC2
        exp_var_pc1 <- exp_var[2]
        xaxis <- c("PC2")
    } else if (pc1 == 'PC3') {
        pc1 <- df_X$PC3
        exp_var_pc1 <- exp_var[3]
        xaxis <- c("PC3")
    }

    if (pc2 == 'PC1') {
        pc2 <- df_X$PC1
        exp_var_pc2 <- exp_var[1]
        yaxis <- c("PC1")
    }  else if (pc2 == 'PC2') {
        pc2 <- df_X$PC2
        exp_var_pc2 <- exp_var[2]
        yaxis <- c("PC2")
    } else if (pc2 == 'PC3') {
        pc2 <- df_X$PC3
        exp_var_pc2 <- exp_var[3]
        yaxis <- c("PC3")
    }

    pca_plot <- ggplot(df_X, aes(pc1, pc2, fill = color_group, shape = shape_group)) +
     geom_point(size = 5, color = "black") +
     scale_fill_viridis_c(option = "C") +
     scale_shape_manual(values = c(24,21)) +
     # stat_ellipse() +
     xlab(paste(xaxis, " - ", exp_var_pc1)) +
     ylab(paste(yaxis, " - ", exp_var_pc2)) +
     theme_minimal(base_size = 16) +
     theme(text = element_text(size=16)) +
     theme(legend.title = element_blank(),
           legend.key.size = unit(2,"mm"),
           legend.text = element_text(size = 6)) +
     theme(legend.position = "top") +
     ggtitle(title_text) + theme(plot.title = element_text(size = 10))

    return(pca_plot)
}

plot_pca_bi <- function(df, pc1, pc2, metadata_group, columntitle) {
    metadata_group_colors <- get(paste(metadata_group, "_colors", sep = ""))
    metadata_group_shapes <- get(paste(metadata_group, "_shapes", sep = ""))

    arrow_pc <- enquo(columntitle)

    exp_var <- paste0(round(df$explained_variance * 100, 2), "%") # explained variance for x- and y-labels

    # select only the PCs from the PCA and add metadata
    df_X <- df$variates$X %>%
              as.data.frame() %>%
              rownames_to_column("Library_ID") %>%
              inner_join(full_metadata, by = "Library_ID")

    metadata_group = df_X[[metadata_group]]

    corr_lam <- df$sdev[c("PC1", "PC2", "PC3")] * sqrt(nrow(df_X))

    df_X <- df_X %>%
      mutate(PC1 = PC1 / corr_lam[1],
             PC2 = PC2 / corr_lam[2],
             PC3 = PC3 / corr_lam[3])

    # select the correct PC column and explained variance for PC1
    if (pc1 == 'PC1') {
        Pc1 <- df_X$PC1
        exp_var_pc1 <- exp_var[1]
        xaxis <- c("PC1")
    } else if (pc1 == 'PC2') {
        Pc1 <- df_X$PC2
        exp_var_pc1 <- exp_var[2]
        xaxis <- c("PC2")
    } else if (pc1 == 'PC3') {
        Pc1 <- df_X$PC3
        exp_var_pc1 <- exp_var[3]
        xaxis <- c("PC3")
   }

    # select the correct PC column and explained variance for PC2
    if (pc2 == 'PC1') {
        Pc2 <- df_X$PC1
        exp_var_pc2 <- exp_var[1]
        yaxis <- c("PC1")
 } else if (pc2 == 'PC2') {
       Pc2 <- df_X$PC2
       exp_var_pc2 <- exp_var[2]
       yaxis <- c("PC2")
    } else if (pc2 == 'PC3') {
       Pc2 <- df_X$PC3
       exp_var_pc2 <- exp_var[3]
       yaxis <- c("PC3")
   }

    # Identify the 10 pathways that have highest positive and negative loadings in the selected PC
    pws_10 <- df$loadings$X %>%
      as.data.frame(.) %>%
      rownames_to_column(var = "Pathway") %>%
      separate(Pathway, into = "Pathway", sep = ":", extra = "drop") %>%
      top_n(10, !!arrow_pc)

    neg_10 <- df$loadings$X %>%
      as.data.frame(.) %>%
      rownames_to_column(var = "Pathway") %>%
      separate(Pathway, into = "Pathway", sep = ":", extra = "drop") %>%
      top_n(-10, !!arrow_pc)


    pca_plot_bi <- ggplot(df_X, aes(x = Pc1, y = Pc2)) +
      geom_point(size = 3.5, aes(shape = metadata_group, fill = metadata_group))+
      geom_segment(data = pws_10,
                   aes(xend = get(paste(pc1)), yend = get(paste(pc2))),
                   x = 0, y = 0, colour = "black",
                   size = 0.5,
                   arrow = arrow(length = unit(0.03, "npc"))) +
      geom_label_repel(data = pws_10,
                   aes(x = get(paste(pc1)), y = get(paste(pc2)), label = Pathway),
                   size = 2.5, colour = "grey20", label.padding = 0.2, force = 5, max.overlaps = 20) +
      geom_segment(data = neg_10,
                   aes(xend = get(paste(pc1)), yend = get(paste(pc2))),
                   x = 0, y = 0, colour = "grey50",
                   size = 0.5,
                   arrow = arrow(length = unit(0.03, "npc"))) +
      geom_label_repel(data = neg_10,
                   aes(x = get(paste(pc1)), y = get(paste(pc2)), label = Pathway),
                   size = 2.5, colour = "grey20", label.padding = 0.2, max.overlaps = 12) +
      labs(x = paste(xaxis, " - ", exp_var_pc1),
           y = paste(yaxis, " - ", exp_var_pc2)) +
      scale_fill_manual(values = metadata_group_colors) +
      scale_shape_manual(values = metadata_group_shapes) +
      theme_minimal() + theme(text = element_text(size = 16)) +
      theme(text = element_text(size=16)) +
      theme(legend.position = "top")

    return(pca_plot_bi)
}

```

As we are dealing with aDNA, and we often have bad samples, its sometimes interesting to see differences between well/badly preserved samples at all stages of analysis.

Therefore we may generate results for all samples. However for actual analysis where we want to intepret biological differences, should exclude outliers (in this case highly contaminated samples - as identified by the `decontam` package - see [Velsko et al. 2022 \_PNAS Nexus](https://doi.org/10.1093/pnasnexus/pgac148) for more details).

We can make a list the outliers from the previous authentication analyses.

```r
outliers_mpa3 <- c("EXB059.A2101","EXB059.A2501","EXB015.A3301","EXB034.A2701",
                   "EXB059.A2201","EXB059.A2301","EXB059.A2401","LIB058.A0103","LIB058.A0106","LIB058.A0104")
poor_samples_mpa3 <- c("CS28","CS38","CSN","ELR003.A0101","ELR010.A0101",
                       "KT09calc","MID024.A0101","MID063.A0101","MID092.A0101")

outliersF <- str_c(outliers_mpa3, collapse = "|")

```

#### Sample Clustering with PCA

##### Pathway abundance analyses

Once we've removed outlier samples, our first simple question is - what is the functional relationships of the groups?

Can we already see distinctive patterns between the different groups in our dataset?

To do this lets clean up the data a bit (cleaning names, removing samples with no metadata etc.), normalise (via a 'centered-log-ratio' transform ), and run a PCA.

Once we've done this we should always check our PCA's Scree plot first.

```r

humann3_path_l1 <- humann3_path %>%
  filter(!str_detect(Pathway, "\\|")) %>%
  # no full_metadata, remove these
  select(-c("MID025.A0101","MID033.A0101","MID052.A0101","MID056.A0101",
            "MID065.A0101","MID068.A0101","MID076.A0101","MID078.A0101")) %>%
  # remove poorly preserved saples
  select(-c("MID024.A0101","MID063.A0101","MID092.A0101")) %>%
  select(-matches("EXB|LIB")) %>%
  # inner_join(., humann3_path.decontam_noblanks_presence_more_30, by = "Pathway") %>%
  gather("Library_ID","Counts",2:ncol(.)) %>%
  mutate(Counts = Counts + 1) %>%
  spread(Pathway,Counts) %>%
  column_to_rownames("Library_ID")

# prepare to run a PCA
# check the number of components to retain by tuning the PCA
mixOmics::tune.pca(humann3_path_l1, logratio = 'CLR')


humann3_all_otu.pca <- mixOmics::pca(humann3_path_l1, ncomp = 3, logratio = 'CLR')
humann3_all_pca_values <- humann3_all_otu.pca$variates$X %>%
  as.data.frame() %>%
  rownames_to_column("Library_ID") %>%
  inner_join(., full_metadata, by = "Library_ID")

```

We can see the first couple of PCs in the scree plot account for a good chunk of the variation of our dataset, so lets visualise the PCA itself.

We visualise the PCA with one of our custom functions defined above, and colour by the Pipe notch metadata column.

```r
# pipenotch colors/shapes
Pipenotch_colors = c("#311068","#C83E73")
Pipenotch_shapes = c(16,17)

# by minimum number of pipenotches
pipenotch <- plot_pca_cont(humann3_path_l1, "PC1", "PC2","Min_no_Pipe_notches","Pipenotch", 3,"Min. No. Pipe Notches")
pipenotch

```

We can see there is a slight separation between the groups, but how do we find out which pathways are maybe driving this pattern?

For this we can generate a PCA bi-plot which show what loadings are driving the spread of the samples.

```r
Pipenotch_colors = c("#311068","#C83E73")
Pipenotch_shapes = c(24,21)

biplot <- plot_pca_bi(humann3_all_otu.pca, "PC1", "PC2", "Pipenotch", PC1)
biplot

```

From the biplot we can see which pathways are differentiating along PC1.

We can pull these IDs out to find out what pathways there are from the biplot object itself.

```r
# make a table of the pathways to save, to use again later in another R notebook
humann3_pathway_biplot_list <- biplot$plot_env$pws_10 %>% arrange(desc(PC1)) %>% select(Pathway, PC1, PC2) %>% mutate(Direction = "PC1+")
humann3_pathway_biplot_list <- humann3_pathway_biplot_list %>%
  bind_rows(biplot$plot_env$neg_10 %>% arrange(desc(PC1)) %>% select(Pathway, PC1, PC2)%>% mutate(Direction = "PC1-"))

```

##### Species contributions to pathways

However, this ID numbers aren't very informative to us. At this point we have to do a bit of literature review/database scraping to pull the human-readable names/descriptions of the IDs - which we have already done for you.

We can load these back into our environment

```r
# PC biplot loading top 10s
humann3_pathway_biplot_list <- fread("./humann3_pathway_biplot_list.tsv")
humann3_pathway_biplot_list <- humann3_pathway_biplot_list %>%
  rename(Pathway = pathway) %>%
  mutate(Path = sapply(Pathway, function(f) {
                                  unlist(str_split(f, ":"))[1]
                                  })) %>%
  select(Pathway, Path, everything()) %>%
  # remove 3 of the 4 ubiquinol pathways w/identical loadings
  filter(!str_detect(Pathway, "5856|5857|6708"))

tibble(humann3_pathway_biplot_list)

```

We now have the pathway ID, and a pathway description for each of the loadings of the PCA.

##### PC1

While we have the pathways, we don't _who_ contributed these.

For this, we can join our pathway table back onto the original output from HUMANn3 we loaded at the beginning, which includes the taxa information.

```r
# list the 10 orthologs with strongest loading in PC1 + values
humann3_path_biplot_pc <- humann3_pathway_biplot_list %>%
  filter(Direction == "PC1+") %>%
  pull(Path) %>%
  str_c(., collapse = "|") # need this format for filtering in the next step


# select only those 10 pathways from the list, and split the column with names into 3 (Pathway, Genus, Species)
humann3_path_pc1pws <- humann3_path %>%
  filter(str_detect(Pathway, humann3_path_biplot_pc)) %>%
  filter(str_detect(Pathway, "\\|")) %>%
  gather("SampleID", "CPM", 2:ncol(.)) %>%
  mutate(Pathway = str_replace_all(Pathway, "\\.s__", "|s__")) %>%
  separate(., Pathway, into = c("Pathway", "Genus", "Species"), sep = "\\|") %>%
  mutate(Species = replace_na(Species, "unclassified"),
         Genus = str_replace_all(Genus, "g__", ""),
         Species = str_replace_all(Species, "s__", "")) %>%
  inner_join(., humann3_pathway_biplot_list %>%
              select(Pathway, Path) %>%
               distinct(.), by = "Pathway") %>%
  inner_join(.,  humann3_pathway_biplot_list %>%
               filter(Direction == "PC1+") %>%
               select(Path), by = "Path") %>%
  # select(-Pathway) %>%
  select(Path, everything()) %>%
  arrange(Path)

tibble(humann3_path_pc1pws)

```

We can now see who contributed which pathway, and also the abundance information (CPM)!

Given many taxa may contribute to the same pathway, we may want to see which taxa are more 'dominantly' contributing to this.

For this we can calculate of all copies of a given pathway what fraction comes from which taxa (you can imagine this like 'depth' coverage in genomic analysis), based on the percentage of the total copies per million for that pathway.

```r
# calculate the % for each pathway contributed by each genus
humann3_path_pc1pws_stats <- humann3_path_pc1pws %>%
  group_by(Path, Genus) %>%
  summarize(Sum = sum(CPM)) %>%
  mutate(Percent = Sum/sum(Sum)*100) %>%
  ungroup(.)

# create the list of 10 orthologs again, but don't collapse the list as above
humann3_path_biplot_pc <- humann3_pathway_biplot_list %>%
  filter(Direction == "PC1+") %>%
  arrange(Path) %>%
  pull(Path)

# calculate the total % of all genera that contribute < X% to each ortholog
humann3_path_pc1pws_stats_extra <- lapply(humann3_path_biplot_pc, function(eclass) {
 high_percent <- humann3_path_pc1pws_stats %>%
   filter(Path == eclass) %>%
   filter(Percent < 5) %>%
   summarise(Remaining = sum(Percent)) %>%
   mutate(Path = eclass,
          Genus = "Other")
}) %>%
 bind_rows(.)

# add this additional % to the main table
humann3_path_pcbi_bar_df <- humann3_path_pc1pws_stats_extra %>%
  rename(Percent = Remaining) %>%
  bind_rows(., humann3_path_pc1pws_stats %>%
              select(-Sum)) %>%
  select(Path, Genus, Percent) %>%
  mutate(Direction = "PC1+") %>%
  distinct()
```

And we can visualize the contributors to the top 10 pathways) driving the main variation along PC1 (with the assumption these maybe the most biological significant, and to reduce the numbers of pathways we have to research.

For the loadings falling in the positive direction of the PC1:

```r
# plot the values in a bar chart
paths_sp_pc1 <- humann3_path_pcbi_bar_df %>%
  # filter(Direction == "PC1+", Genus != "Other") %>% # removing Other plots all species/unassigned - no need to filter the pathways
  filter(Percent >= 5 | (Percent <= 5 & Genus == "Other")) %>% # filter out the genera with % < 5, but keep Other < 5
  # filter(Percent >= 5) %>% # filter out the genera with % < 5, but keep Other < 5
  mutate(
    Genus = fct_relevel(Genus, "Other","unclassified","Aggregatibacter","Capnocytophaga","Cardiobacterium",
                        "Eikenella","Haemophilus","Kingella","Lautropia","Neisseria","Ottowia","Streptococcus"),
         Path = fct_relevel(Path, humann3_pathway_biplot_list %>%
                              filter(Direction == "PC1+") %>%
                              pull(Path))) %>%
  ggplot(., aes(x=Path, y=Percent, fill = Genus)) +
    geom_bar(stat = "identity") +
    theme_minimal() +
    scale_fill_manual(values = c("#0D0887FF","#969696","#5D01A6FF","#7E03A8FF",
                                 "#9C179EFF","#B52F8CFF","#CC4678FF","#DE5F65FF",
                                 "#ED7953FF","#F89441FF","#FDB32FFF","#FBD424FF","#F0F921FF")) +
    theme(text = element_text(size=18),
          axis.text.x = element_text(angle = 90, vjust = 0.5, hjust = 1)) +
    ylab("Percent") +
    ggtitle("Metacyc pathways - PC1 positive") +
    theme(title = element_text(size=10))

# viridis_pal(option = "B")(13)
paths_sp_pc1

```

Note: PWY-5345 has no species assignment to that pathway.

And the negative loadings:

```r
# list the 10 orthologs with strongest loading in PC1 + values
humann3_path_biplot_pc <- humann3_pathway_biplot_list %>%
  filter(Direction == "PC1-") %>%
  arrange(Path) %>%
  pull(Path) %>%
  str_c(., collapse = "|") # need this format for filtering in the next step

# select only those 10 orthologs from the list, and split the column with names into 3 (Ortholog, Genus, Species)
humann3_path_pc1neg <- humann3_path %>%
  filter(str_detect(Pathway, humann3_path_biplot_pc)) %>%
  filter(str_detect(Pathway, "\\|")) %>%
  gather("SampleID", "CPM", 2:ncol(.)) %>%
  mutate(Pathway = str_replace_all(Pathway, "\\.s__", "|s__")) %>%
  separate(., Pathway, into = c("Pathway", "Genus", "Species"), sep = "\\|") %>%
  mutate(Species = replace_na(Species, "unclassified"),
         Genus = str_replace_all(Genus, "g__", ""),
         Species = str_replace_all(Species, "s__", "")) %>%
  inner_join(., humann3_pathway_biplot_list %>%
              select(Pathway, Path) %>%
               distinct(.), by = "Pathway") %>%
  inner_join(.,  humann3_pathway_biplot_list %>%
               filter(Direction == "PC1-") %>%
               select(Path), by = "Path") %>%
  select(-Pathway) %>%
  select(Path, everything()) %>%
  arrange(Path)

# calculate the % for each ortholog contributed by each genus
humann3_path_pc1neg_stats <- humann3_path_pc1neg %>%
  group_by(Path, Genus) %>%
  summarize(Sum = sum(CPM)) %>%
  mutate(Percent = Sum/sum(Sum)*100) %>%
  ungroup(.)

# create the list of 10 orthologs again, but don't collapse the list as above
humann3_path_biplot_pc <- humann3_pathway_biplot_list %>%
  filter(Direction == "PC1-") %>%
  arrange(Path) %>%
  pull(Path)

# calculate the total % of all genera that contribute < X% to each ortholog
humann3_path_pc1neg_stats_extra <- lapply(humann3_path_biplot_pc, function(eclass) {
 high_percent <- humann3_path_pc1neg_stats %>%
   filter(Path == eclass) %>%
   filter(Percent < 5) %>%
   summarise(Remaining = sum(Percent)) %>%
   mutate(Path = eclass,
          Genus = "Other")
}) %>%
 bind_rows(.)

# add this additional % to the main table
humann3_path_pcbi_bar_df <- humann3_path_pcbi_bar_df %>%
  bind_rows(humann3_path_pc1neg_stats_extra %>%
            rename(Percent = Remaining) %>%
            bind_rows(., humann3_path_pc1neg_stats %>%
                      select(-Sum)) %>%
            select(Path, Genus, Percent) %>%
            mutate(Direction = "PC1-")) %>%
  distinct()

# plot the values in a bar chart
paths_sp_pc2 <- humann3_path_pcbi_bar_df %>%
  filter(Direction == "PC1-") %>% # removing Other plots all species/unassigned - no need to filter the pathways
  filter(Percent >= 5 | (Percent <= 5 & Genus == "Other")) %>% # filter out the genera with % < 5, but keep Other < 5
  mutate(Genus = fct_relevel(Genus, "Other","unclassified","Desulfobulbus","Desulfomicrobium","Methanobrevibacter"),
         Path = fct_relevel(Path, humann3_pathway_biplot_list %>%
                              filter(Direction == "PC1-") %>%
                              pull(Path))) %>%
  ggplot(., aes(x=Path, y=Percent, fill = Genus)) +
    geom_bar(stat = "identity") +
    theme_minimal() +
    scale_fill_manual(values = c("#0D0887FF","#969696","#B52F8CFF","#ED7953FF","#FCFFA4FF")) +
    theme(text = element_text(size=18),
          axis.text.x = element_text(angle = 90, vjust = 0.5, hjust = 1)) +
    # facet_wrap(~pathrtholog, nrow=2) +
    ylab("Percent") +
    ggtitle("Metacyc pathways - PC1 negative") +
    theme(title = element_text(size=12))

paths_sp_pc2
```

##### Final Visualisation

Finally, we can stick the biplot and the taxon contribution plots together!

```r
h3biplots <- biplot + paths_sp_pc2 + paths_sp_pc1 +
  plot_layout(widths = c(2, 1,1))

ggsave("./h3_paths_biplots.pdf", plot = h3biplots,
        device = "pdf", scale = 1, width = 20, height = 9.25, units = c("in"), dpi = 300)

system(paste0('firefox "h3_paths_biplots.pdf"'))

```

This allows us to evaluate all the information together.

From this point onwards, we would have to do manual research/literature reviews into each of the pathways, see if they make 'sense' to the sample type and associated groups of samples, and evaluate whether they are interesting or not..

        </div>

</details>

---

### Resources

### Readings

- Vernikos, G. S. 2020. “A Review of Pangenome Tools and Recent Studies.” In The Pangenome: Diversity, Dynamics and Evolution of Genomes, edited by Hervé Tettelin and Duccio Medini. Cham (CH): Springer. [https://doi.org/10.1007/978-3-030-38281-0](https://doi.org/10.1007/978-3-030-38281-0).
- Westbrook, Anthony, Jordan Ramsdell, Taruna Schuelke, Louisa Normington, R. Daniel Bergeron, W. Kelley Thomas, and Matthew D. MacManes. 2017. “PALADIN: Protein Alignment for Functional Profiling Whole Metagenome Shotgun Data.” Bioinformatics 33 (10): 1473-78. [https://doi.org/10.1093/bioinformatics/btx021](https://doi.org/10.1093/bioinformatics/btx021).
- Franzosa, Eric A., Lauren J. McIver, Gholamali Rahnavard, Luke R. Thompson, Melanie Schirmer, George Weingart, Karen Schwarzberg Lipson, et al. 2018. “Species-Level Functional Profiling of Metagenomes and Metatranscriptomes.” Nature Methods 15 (11): 962-68. [https://doi.org/10.1038/s41592-018-0176-y](https://doi.org/10.1038/s41592-018-0176-y)

### Questions to think about

### Roundtable: Social (Leipzig Only)

Those present in Leipzig can join for a summer school dinner.
