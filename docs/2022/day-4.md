# Day Four

## Lecture 4A: Introduction to microbial genomics

**Instructors**: Alexander Herbig

**Abstract**: The field of microbial genomics aims at the reconstruction and comparative analyses of genomes for gaining insights into the genetic foundation and evolution of various functional aspects such as virulence mechanisms in pathogens.

Including data from ancient samples into this comparative assessment allows for studying these evolutionary changes through time. This, for example, provides insights into the emergence of human pathogens and their development in conjunction with human cultural transitions.

In this lecture I will provide examples for how to utilise data from ancient genomes in comparative studies of human pathogens and today's practical sessions will highlight methodologies for the reconstruction of microbial genomes.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vS1q6ZwVnUVPge-kywBkxdv9gBl4pSnlZNd8YeZMkhy5CL1qRtP31J4spetCuujUmIVMPJ4f2LZAB5O/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4a-intro-to-microbial-genomics/SPAAM%20Summer%20School%202022%20-%204A%20-%20Intro%20to%20Microbial%20Genomics.pdf).

### Resources

### Readings

### Questions to think about

## Software

For today's practical sessions, please [activate](2022/resources#software-and-data) the `microbial-genomics` conda [environment](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day4.yml).

```bash
conda activate microbial-genomics
```

## Practical 4B: Genome mapping

**Instructors**: Alexander Herbig and Alina Hiß

**Abstract**: An important step in the reconstruction of full genomic sequences is mapping. Even relatively short genomes usually cannot be sequenced as a single consecutive piece. Instead, millions of short sequence reads are generated from genomic fragments. These reads can be several hundred nucleotides in length but are considerably shorter for ancient DNA (aDNA).

For many applications involving comparative genomics these 'reads' have to be aligned to one or multiple already-reconstructed reference genomes in order to identify differences between the sequenced genome and any given contextual dataset. Aligning millions of short reads to much longer genome sequences in a time-efficient and accurate manner is a bioinformatics challenge for which numerous algorithms and tools have been developed. Each of these programs comes with a variety of parameters that can significantly alter the results and default settings are often not optimal when working with aDNA. Furthermore, read mapping procedures are often part of complex computational genomics pipelines and are therefore not directly applied by many users.

In this session we will take a look at specific challenges during read mapping when dealing with aDNA. We will get an overview of common input and output formats and manually apply a read mapper to aDNA data studying the direct effects of variation in mapping parameters. We will conclude the session with an outlook on genotyping, which is an important follow-up analysis step, that in turn is very relevant for down-stream analyses such as phylogenetics.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSJ9ZUd53kHpZkROVNy_RDIv6XhtbHF5w_WAtEDm6_ZXb2zf0v8DZHLYIWyzzWjFc1fPn7J9fI8n_bN/embed?start=true&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/SPAAM%20Summer%20School%202022%20-%204B%20-%20Genome%20Mapping.pdf).

### Resources

Software:

- [BWA](http://bio-bwa.sourceforge.net/)
- [samtools](http://www.htslib.org/)
- [GATK](https://gatk.broadinstitute.org/hc/en-us)
- [MultiVCFAnalyzer](https://github.com/alexherbig/MultiVCFAnalyzer)
- [IGV](https://software.broadinstitute.org/software/igv/)

### Readings

- Spyrou, M. A., Bos, K. I., Herbig, A., & Krause, J. (2019). "Ancient pathogen genomics as an emerging tool for infectious disease research." Nature reviews. Genetics, 20(6), 323–340. [https://doi.org/10.1038/s41576-019-0119-1](https://doi.org/10.1038/s41576-019-0119-1)
- Bos, K. I., Kühnert, D., Herbig, A., Esquivel-Gomez, L. R., Andrades Valtueña, A., Barquera, R., Giffin, K., Kumar Lankapalli, A., Nelson, E. A., Sabin, S., Spyrou, M. A., & Krause, J. (2019). "Paleomicrobiology: Diagnosis and Evolution of Ancient Pathogens." Annual review of microbiology, 73, 639–666. [https://doi.org/10.1146/annurev-micro-090817-062436](https://doi.org/10.1146/annurev-micro-090817-062436)

### Questions to think about

## Practical 4C: Genome assembly

**Instructors**: Alexander Hübner and Nikolay Oskolkov

**Abstract**: _De novo_ assembly of ancient metagenomic samples enables the recovery of the genetic information of organisms without requiring any prior knowledge about their genomes. Therefore, this approach is very well suited to study the biological diversity of species that have not been studied well or are simply not known yet.

In this session, we will show you how to prepare your sequencing data and subsequently _de novo_ assemble them. Furthermore, we will then learn how we can actually evaluate what organisms we might have assembled and whether we obtained enough data to reconstruct a whole metagenome-assembled genome. We will particularly focus on the quality assessment of these reconstructed genomes and how we can ensure that we obtained high-quality genomes.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQiyXe-6yn1hfaoibwI8DBYHubQxEd_WEvXte6JqyyjnuY8DXfP64360tRvhmRxOPAoM4Gt6hqKG5ts/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4c-intro-to-denovoassembly/SPAAM%20Summer%20School%202022%20-%204C%20-%20Genome%20Assembly.pdf).

### Resources

### Readings

- Chen et al. (Genome Research, 2020): Accurate and complete genomes from metagenomes (doi: 10.1101/gr.258640.119)
- Meyer, Fritz et al. (Nature Methods, 2022): Critical Assessment of Metagenome Interpretation: the second round of challenges (doi: 10.1038/s41592-022-01431-4)
- Wibowo et al. (Nature, 2021): Reconstruction of ancient microbial genomes from the human gut (doi: 10.1038/s41586-021-03532-0)
- Maixner et al. (Current Biology, 2021): Hallstatt miners consumed blue cheese and beer during the Iron Age and retained a non-Westernized gut microbiome until the Baroque period (doi: 10.1016/j.cub.2021.09.031)

### Questions to think about

### Roundtable: Databases

**Chairs**: Maxime Borry and James Fellows Yates

Arguably, _which_ databases to use are even more important than classifiers when it comes to metagenomics. What is in and not in your database can greatly influence your output results. In this roundtable we will discuss how to select and create databases, and also strategies to get around issues such as computational limitations when constructing and using databases.
