# Day Two

## Lecture 2A: Introduction to ancient DNA

**Instructors**: Christina Warinner

**Abstract**: This lecture introduces you to ancient DNA and the enormous technological changes that have taken place since the field’s origins in 1984. Starting with the quagga and proceeding to microbes, we discuss where ancient microbial DNA can be found in the archaeological record and examime how ancient DNA is defined by its condition, not by a fixed age. We next cover genome basics and take an in-depth look at the way DNA degrades over time. We detail the fundamentals of DNA damage, including the specific chemical processes that lead to DNA fragmentation and C->T miscoding lesions. We then demystify the DNA damage “smile plot” and explain the how the plot’s symmetry or asymmetry is related to the specific enzymes used to repair DNA during library construction. We discuss how DNA damage is and is not clock-like, how to interpret and troubleshoot DNA damage plots, and how DNA damage patters can be used to authenticate ancient samples, specific taxa, and even sequences. We cover laboratory strategies for removing or reducing damage for greater accuracy for genotype calling, and we discuss the pros and cons of single-stranded library protocols. We then take a closer look at proofreading and non-proofreading polymerases and note key steps in NGS library preparation during which enzyme selection is critical in ancient DNA studies. Finally, we examine the big picture of why DNA damage matters in ancient microbial studies, and its effects on taxonomic identification of sequences, accurate genome mapping, and metagenomic assembly.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRQYqeq8LDnw-McfI8zRvEX2xL77awoP4BLGCBNPj2rorPOxFQOdwnhVosu8qqlnZKqDl5dd6SYt0qf/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Resources

### Readings

- Orlando, L., Allaby, R., Skoglund, P., Der Sarkissian, C., Stockhammer, P. W., Ávila-Arcos, M. C., ... & Warinner, C. (2021). Ancient DNA analysis. Nature Reviews Methods Primers, 1(1), 1-26.
- Higuchi, R., Bowman, B., Freiberger, M., Ryder, O. A., & Wilson, A. C. (1984). DNA sequences from the quagga, an extinct member of the horse family. Nature, 312(5991), 282-284.
- Briggs, A.W., Stenzel, U., Meyer, M., Krause, J., Kircher, M. and Pääbo, S., 2010. Removal of deaminated cytosines and detection of in vivo methylation in ancient DNA. Nucleic Acids Research, 38(6), pp.e87-e87.
- Gansauge, M.T. and Meyer, M., 2013. Single-stranded DNA library preparation for the sequencing of ancient or damaged DNA. Nature Protocols, 8(4), pp.737-748.
- Jónsson, H., Ginolhac, A., Schubert, M., Johnson, P. L., & Orlando, L. (2013). mapDamage2.0: fast approximate Bayesian estimates of ancient DNA damage parameters. Bioinformatics, 29(13), 1682-1684.
- Meyer, M. and Kircher, M., 2010. Illumina sequencing library preparation for highly multiplexed target capture and sequencing. Cold Spring Harbor Protocols, 2010(6), pp.pdb-prot5448.
- Warinner, C., Herbig, A., Mann, A., Yates, J. A. F., Weiβ, C. L., Burbano, H. A., ... & Krause, J. (2017). A robust framework for microbial archaeology. Annual Review of Genomics and Human Genetics, 18, 321.

### Questions to think about

## Software

For today's practical sessions, please activate the `git-eager` conda [environment](2022/resources#software-and-data)

```bash
conda activate git-eager
```

## Practical 2B: Introduction to Git(Hub)

**Instructors**: Megan Michel

**Abstract**: As the size and complexity of metagenomic analyses continues to expand, effectively organizing and tracking changes to scripts, code, and even data, continues to be a critical part of ancient metagenomic analyses. Furthermore, this complexity is leading to ever more collaborative projects, with input from multiple researchers.

In this practical session, we will introduce 'Git', an extremely popular version control system used in bioinformatics and software development to store, track changes, and collaborate on scripts and code. We will also introduce, GitHub, a cloud-based service for Git repositories for sharing data and code, and where many bioinformatic tools are stored. We will learn how to access and navigate course materials stored on GitHub through the web interface as well as the command line, and we will create our own repositories to store and share the output of upcoming sessions.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vR07xSxl-AaB6df4Mu4BN4X41U5SM41fKy0gvZ7sSSPtqRoF2RqFth-aduhN9nkRpkdzP0N6fb5x5Ok/embed?start=true&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Resources

- https://www.atlassian.com/git/tutorials
- https://ohshitgit.com/

### Readings

- Chacon, Scott, and Ben Straub. 2022. Pro Git. Second Edition. The Expert’s Voice. Apress.

### Questions to think about

1. Why is using a version control software for tracking data and code important?
2. How can using Git(Hub) help me to collaborate on group projects?

## Practical 2C: Introduction to AncientMetagenomeDir

**Instructors**: James Fellows Yates

**Abstract**: Finding relevent comparative data for your ancient metagenomic analysis is not trivial. While palaeogenomicists are very good at uploading their raw sequencing data to large sequencing data repositories such as the EBI's ENA or NCBI's SRA archives in standardised file formats, these files often have limited metadata. This often makes it difficult for researchers to search for and download relevent published data they wish to use use to augment their own analysis.

AncientMetagenomeDir is a community project from the SPAAM community to make ancient metagenomic data more accessible. We curate a list of standardised metadata of all published ancient metagenomic samples and libraries, hosted on GitHub. In this session we will go through how to use the AncientMetagenomeDir repository and associated tools to find and download data for your own analyses. We will also discuss important things to consider when publishing your own data to make it more accessible for other researchers.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSkO7KH9YEmHCjMlCRhoxtZrDxZ0cKnsPazEAS3PspBGuhAtA9qhQ0wnPXg64cZrAJZQECngZFfjTRL/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Resources

- https://github.com/SPAAM-community/AncientMetagenomeDir
- https://github.com/SPAAM-community/AMDirT

### Readings

- Fellows Yates, James A., Aida Andrades Valtueña, Åshild J. Vågene, Becky Cribdon, Irina M. Velsko, Maxime Borry, Miriam J. Bravo-Lopez, et al. 2021. “Community-Curated and Standardised Metadata of Published Ancient Metagenomic Samples with AncientMetagenomeDir.” Scientific Data 8 (1): 31. https://doi.org/10.1038/s41597-021-00816-y.
- Wilkinson, Mark D., Michel Dumontier, I. Jsbrand Jan Aalbersberg, Gabrielle Appleton, Myles Axton, Arie Baak, Niklas Blomberg, et al. 2016. “The FAIR Guiding Principles for Scientific Data Management and Stewardship.” Scientific Data 3 (March): 160018. https://doi.org/10.1038/sdata.2016.18.

### Questions to think about

- Why is metadata critical for downloading public data?
- What are suitable places to upload your raw data?
- How should you format your metadata?
- Where should you upload metadata about your samples?

## Practical 2D: Introduction to nf-core/eager

**Instructors**: Megan Michel and James Fellows Yates

**Abstract**: Analyses in the field of ancient DNA are growing, both in terms of the number of samples processed and in the diversity of our research questions and analytical methods. Computational pipelines are a solution to the challenges of big data, helping researchers to perform analyses efficiently and in a reproducible fashion. Today we will introduce nf-core/eager, one of several pipelines designed specifically for the preprocessing, analysis, and authentication of ancient next-generation sequencing data.

In this practical session we will learn how to perform basic analyses with nf-core/eager, starting from raw data and performing preprocessing, alignment, and genotyping of several _Yersinia pestis_-positive samples. We will gain an appreciation of the diversity of analyses that can be performed within nf-core eager, as well as where to find additional information for customizing your own nf-core/eager runs. Finally, we will learn how to use nf-core/eager to evaluate the quality and authenticity of our ancient samples. After this session, you will be ready to strike out into the world of nf-core/eager and build your own analyses from scratch!

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQ96Xk7UUc71fwdjxCEgxPoGPLiO6xKRLAH5scnGnZrFm3WK5AEndp9mpwzWJQeD4SLjKhWU6BGs92t/embed?start=true&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Resources

- nf-core/eager pipeline docuemntation: [https://nf-co.re/eager](https://nf-co.re/eager)
- nf-core/eager parameter documentation: [https://nf-co.re/eager/2.4.4/parameters](https://nf-co.re/eager/2.4.4/parameters)
- nf-core/eager GUI: [https://nf-co.re/eager/launch](https://help.tower.nf/22.2/)
- nf-core tower documentation: [https://help.tower.nf/22.2/](https://help.tower.nf/22.2/)

### Readings

- Fellows Yates, James A., Thiseas C. Lamnidis, Maxime Borry, Aida Andrades Valtueña, Zandra Fagernäs, Stephen Clayton, Maxime U. Garcia, Judith Neukamm, and Alexander Peltzer. 2021. “Reproducible, Portable, and Efficient Ancient Genome Reconstruction with Nf-Core/eager.” PeerJ 9 (March): e10947. https://doi.org/10.7717/peerj.10947.
- Peltzer, Alexander, Günter Jäger, Alexander Herbig, Alexander Seitz, Christian Kniep, Johannes Krause, and Kay Nieselt. 12/2016. “EAGER: Efficient Ancient Genome Reconstruction.” Genome Biology 17 (1). https://doi.org/10.1186/s13059-016-0918-z.
- Schubert, Mikkel, Luca Ermini, Clio Der Sarkissian, Hákon Jónsson, Aurélien Ginolhac, Robert Schaefer, Michael D. Martin, et al. 2014. “Characterization of Ancient and Modern Genomes by SNP Detection and Phylogenomic and Metagenomic Analysis Using PALEOMIX.” Nature Protocols 9 (5): 1056–82. https://doi.org/10.1038/nprot.2014.063.
- Orlando, Ludovic, Robin Allaby, Pontus Skoglund, Clio Der Sarkissian, Philipp W. Stockhammer, María C. Ávila-Arcos, Qiaomei Fu, et al. 2021. “Ancient DNA Analysis.” Nature Reviews Methods Primers 1 (1): 1–26. https://doi.org/10.1038/s43586-020-00011-0.
- Warinner, Christina, Alexander Herbig, Allison Mann, James A. Fellows Yates, Clemens L. Weiß, Hernán A. Burbano, Ludovic Orlando, and Johannes Krause. 2017. “A Robust Framework for Microbial Archaeology.” Annual Review of Genomics and Human Genetics 18 (1): 321–56.https://doi.org/10.1146/annurev-genom-091416-035526.

### Questions to think about

1. Why is it important to use a pipeline for genomic analysis of ancient data?
2. How can the design of the nf-core/eager pipeline help researchers comply with the FAIR princples for management of scientific data?
3. What metrics do you use to evaluate the success/failure of ancient DNA sequencing experiments? How can these measures be evaluated when using nf-core/eager for data preprocessing and analysis?

## Roundtable: Project organisation

**Chairs**: Alexander Hübner and James Fellows yates

We will discuss the various ways how to structure analysis folders for your research in a manner that promotes portability and reproducibility. Participants can ask for advice and suggestions from the instructors for their specific research projects.

### Resources

- [https://github.com/paleobiotechnology/analysis-project-structure](https://github.com/paleobiotechnology/analysis-project-structure)
