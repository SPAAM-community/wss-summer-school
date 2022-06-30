# Resources

This edition of the summerschool will feature heavy use of the command-line. However
we will provide this to participants if they have a a modern web browser.

## GitHub account

Although the skills learnt in this workshop will be transferable between different platforms (e.g. GitLab, BitBucket etc.). This workshop will heavily use GitHub for training in `git`. Participants will need to create an account at [github.com](https://github.com) if they have not already done so.

## Software and Data

We will be using the following software during the summer school.

While **you will not need to install these yourself for the summer school**, we provide links here to the software used for installation and usage in your own time.

If you wish to use conda to install the tools, environment files are available for you in the links below.

You can download the minimal version of (mini)conda from [here](https://docs.conda.io/en/latest/miniconda.html#miniconda). Once installed, to create the conda environment from the files listed below, you can run the following

```bash
conda env create -f <env_file>.yml
```

Note: you only have to run the environment creation once.

Follow the instructions as prompted (yes to running `conda init`, and we DO recommend running the `conda config` command). Once created, you can see a list of environments with

```bash
conda env list
```

To load the relevant environment, you can run

```bash
conda activate <name_of_envonment>.yml
```

and the software will be available on your command line. You can deactivate the environment with `conda deactivate`.

### Day 1

This day only uses a base Unix environment.

### Day 2

The conda environment (`git-eager`) for day 2 is available [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day2.yml), and includes:

- [nextflow](https://www.nextflow.io/)
- [nf-core tools](https://nf-co.re/tools)
- [nf-core/eager](https://nf-co.re/eager)

Software used in day two and not included in the conda environment are as follows:

- [git](https://git-scm.com/) (normally installed by default on all UNIX based operating systems e.g. Linux, OSX)
- [AMDirT](https://github.com/SPAAM-community/AMDirT/tree/dev) while the tool itself is not within the conda environment, all dependencies are in the conda environment. Use the instructions in the AMDirT GitHub to install, and ignore warnings during conda creation.

### Day 3

The conda environment (`r-python`) for day 3 is available [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day3.yml), and includes:

- [r](https://www.r-project.org/)
- [r studio (desktop)](https://www.rstudio.com/products/rstudio/)
- [tidyverse](https://www.tidyverse.org/)
- [python](https://www.python.org/)
- [jupyter](https://jupyter.org/)

### Day 4

The conda environment (`microbial-genomics`) for day 4 is available [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day4.yml), and includes:

- [bwa](http://bio-bwa.sourceforge.net/)
- [igv](https://igv.org/)
- [gatk](https://gatk.broadinstitute.org/hc/en-us)
- [fastp](https://github.com/OpenGene/fastp)
- [megahit](https://github.com/voutcn/megahit)
- [bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)
- [samtools](http://www.htslib.org/)
- [bioawk](https://github.com/lh3/bioawk)
- [diamond](https://github.com/bbuchfink/diamond)
- [metabat2](https://bitbucket.org/berkeleylab/metabat/src/master/)
- [maxbin2](https://sourceforge.net/projects/maxbin/#:~:text=MaxBin%20is%20a%20software%20for,coverage%20information%20or%20sequencing%20reads.)
- [concoct](https://concoct.readthedocs.io/en/latest/)
- [metawrap](https://github.com/bxlab/metaWRAP)
- [checkm-genome](https://ecogenomics.github.io/CheckM/#:~:text=CheckM%20provides%20a%20set%20of,copy%20within%20a%20phylogenetic%20lineage.)
- [gunc](https://grp-bork.embl-community.io/gunc/)
- [pydamage](https://pydamage.readthedocs.io/en/0.7/)
- [prokka](https://github.com/tseemann/prokka)

### Day 5

The conda environment (`phylogenomics-functional`) for day 5 is available [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/software/2022/day5.yml), and includes:

- [r](https://www.r-project.org/)
- [r studio (desktop)](https://www.rstudio.com/products/rstudio/)
- [tidyverse](https://www.tidyverse.org/)
- [beast2](https://www.beast2.org/)\_
- [tracer](http://tree.bio.ed.ac.uk/software/tracer/)
- [humann3](https://huttenhower.sph.harvard.edu/humann/)

Software used in day two and not included in the conda environment are as follows:

- [tempest](https://beast.community/tempest)
- [mega](https://www.megasoftware.net/)

## Data

- [AncientMetagenomeDir](https://github.com/SPAAM-community/AncientMetagenomeDir/)
- [ENA](https://www.ebi.ac.uk/ena/browser/view/)

## Literature

We also suggest reading the following literature

Warinner, Christina, Alexander Herbig, Allison Mann, James A. Fellows Yates, Clemens L. Weiß, Hernán A. Burbano, Ludovic Orlando, and Johannes Krause. 2017. “A Robust Framework for Microbial Archaeology.” Annual Review of Genomics and Human Genetics 18 (August): 321–56. [https://doi.org/10.1146/annurev-genom-091416-035526](https://doi.org/10.1146/annurev-genom-091416-035526).

Der Sarkissian, Clio, Irina M. Velsko, Anna K. Fotakis, Åshild J. Vågene, Alexander Hübner, and James A. Fellows Yates. 2021. “Ancient Metagenomic Studies: Considerations for the Wider Scientific Community.” mSystems 6 (6): e0131521. [https://doi.org/10.1128/msystems.01315-21](https://doi.org/10.1128/msystems.01315-21).

Velsko, Irina M., Laurent A. F. Frantz, Alexander Herbig, Greger Larson, and Christina Warinner. 2018. “Selection of Appropriate Metagenome Taxonomic Classifiers for Ancient Microbiome Research.” mSystems 3 (4). https://doi.org/10.1128/mSystems.00080-18.

Arizmendi Cárdenas, Yami Ommar, Samuel Neuenschwander, and Anna-Sapfo Malaspinas. 2022. “Benchmarking Metagenomics Classifiers on Ancient Viral DNA: A Simulation Study.” PeerJ 10 (March): e12784. https://doi.org/10.7717/peerj.12784.
