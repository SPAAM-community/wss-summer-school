# Introduction to Ancient Metagenomics Summer School - 2022

## What

The **Ancient Metagenomics Summer School** will be a 5 day **practical** workshop (block praktikum). Attendees who participate in the entire course will be eligible for 1.5 ECTS points (40 hours of instruction and **practicals**, 5 hours of coursework).

The course is taught by scientific staff at the Max Planck Institute for Evolutionary Anthropology and supported by the Werner Siemens Foundation, in collaboration with the Max Planck Harvard Center for the Archaeoscience of the Ancient Mediterranean (MHAAM), the Leibniz Institute for Natural Product Research and Infection Biology, and the Jena School for Microbial Communications. The course coordinators are Prof. Dr. Christina Warinner (christina_warinner@eva.mpg.de) and James Fellows Yates (james_fellows_yates@eva.mpg.de).

## Who

The course is aimed at masters students and early-stage PhD students, to a maximum of 25 participants.

You can meet the instructors [here](/2022/instructors.md).

## Where

We will be running this virtual edition of the SPAAM Summer School Introduction to Metagenomics on [Gather.Town](https://gather.town), on the SPAAM workspace [here](https://app.gather.town/app/PlXjb0deog0B4JCq/spaam-community).

If you're not familiar with this platform please see the documentation on the gather.town website, or [this 'Quick Start' video from nf-core](https://nf-co.re/events/2022/bytesize-37-gathertown).

> ⚠️ If you're using Mac/OSX we highly recommend using the desktop app of gather.town rather than your webbrowser, for optimisation purposes.

## When

The summer school will be provisionally held between 1st-5th August, 09:00-17:00 CEST (Berlin Time).

Note the following additional dates:

- **Applications open**: 29th April 2022
- **Applications close**: 1st June 2022
- **Decision notifications**: 15th June 2022

## What

You will need access to the internet, and a modern web browser - either Google Chrome or Firefox. Please note, if using Firefox, please turn on clipboard support using [these](https://sudoedit.com/firefox-async-clipboard/) instructions.

Each participant will being given a cloud computing node kindly provided by the German [deNBI infrastructure](https://www.denbi.de/cloud) for the duration of the summer school.

Registration links will be sent via email all participants, however detailed instructions on registration procedure can be seen [here](2022/denbi-registration).

Once you've recieved your link, each participant will need to open the link in their browser. On the Guacamole page please use the username/password und 'Login credentials' [here](https://cloud.denbi.de/wiki/simple_vm/customization/#apache-guacamole). You should then see a desktop environment.

If you get a message about permissions for 'colour mangement', please use the password described for the 'Ubuntu User' in the next code block below the 'Login Credentials'.

## Schedule

Subject to change

| **Time**    | **Session Type** | **Day 1**                    | **Day 2**                                                               | **Day 3**                                                                             | **Day 4**                              | **Day 5**                |
| ----------- | ---------------- | ---------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | -------------------------------------- | ------------------------ |
| 09:00-10:15 | Theoretical      | 1A: Introduction to NGS data | 2A: Introduction to ancient DNA                                         | 3A: Introduction to Metagenomics                                                      | 4A: Introduction to microbial genomics | 5A: Evolutionary Biology |
| 10:15-10:30 |                  | Break                        | Break                                                                   | Break                                                                                 | Break                                  | Break                    |
| 10:30-12:30 | Practical        | 1B: BareBonesBash 1          | 2B: Introduction to Git(Hub) & 2C: Introduction to AncientMetagenomeDir | 3B-1: Introduction to R and the tidyverse & 3B-2: - Introduction to Python and Pandas | 4B: Genome mapping                     | 5B: Phylogenomics        |
| 12:30-13:30 |                  | Lunch                        | Lunch                                                                   | Lunch                                                                                 | Lunch                                  | Lunch                    |
| 13:30-15:30 | Practical        | 1C: BareBonesBash 2          | 2D: Introduction to nf-core/eager                                       | 3C: Taxonomic Profiling, OTU Tables and Visualisation                                 | 4C: Genome assembly                    | 5C: Functional Genomics  |
| 15:30-15:45 |                  | Break                        | Break                                                                   | Break                                                                                 | Break                                  | Break                    |
| 15:45-17:00 | Roundtable       | Introductions                | Project Organization                                                    | Taxonomic Classifiers                                                                 | Databases                              | Social                   |

All times CEST (Berlin Time)

## Contents Overview

### DAY 1

- **Lecture** Introduction to NGS data: _James Fellows Yates_
  - What is NGS sequencing and what does its data look like?
- **Practical** BareBonesBash 1: _Aida Andrades Valtueña and Thiseas Lamnidis_
  - Introduction to the UNIX command line.
- **Practical** BareBonesBash 2: _Aida Andrades Valtueña and Thiseas Lamnidis_
  - How to navigate and batch-manipulate files.
- **Round table** Introductions
  - Welcome - let's get to know eachother

### DAY 2

- **Lecture** Introduction to ancient DNA: _Christina Warinner_
  - How to identify and handle DNA from ancient contexts
- **Practical** Bytesize git: _James Fellows Yates and Megan Michel_
  - What is git and github? How to clone a repository? What does commit/pull/push mean?
- **Practical** ancientMetagenomeDir: _James Fellows Yates and Megan Michel_
  - Where to get ancient metagenomic comparative data, and why is metadata important?
  - Git practice
- **Practical** nf-core/eager: _James Fellows Yates and Megan Michel_
  - How do I quality control NGS aDNA data? How do I remove adapters and contamination? How to perform taxonomic profiling?
- **Round table** Project organisation
  - How to structure my project analysis folders? How to reproducibly document my work?

### DAY 3

- **Lecture** Introduction to Metagenomics: _Christina Warinner_
  - What are the questions tackled in metagenomics? What are the challenges?
- **Practical** Introduction to R and the tidyverse / Introduction to Python and Pandas: _Clemens Schmid and Nikolay Oskolkov_ / _Maxime Borry_
  - How to read/write files and run statistical analyses? How to make figures with ggplot2/plotnine
  - (Note: Parallel sessions partcipants can choose which to attend based on their prior experience)
- **Practical** Taxonomic Profiling, OTU Tables and Visualisation: _Maxime Borry and Irina Velsko_
  - Python practice. How to normalise OTU tables and perform microbial ecology analyses.
- **Round table** Taxonomic Classifiers
  - How do I pick a taxonomic classifier? What is best for aDNA?

### DAY 4

- **Lecture** Introduction to microbial genomics: _Alexander Herbig_
  - How can we learn from studying the genomes of microbes? What questions can we ask?
- **Practical** Genome mapping: _Alexander Herbig and Alina Hiss_
  - Why and how do we map against a reference? What parameters are important for aDNA?
- **Practical** Genome assembly: _Alexander Hübner and Nikolay Oskolkov_
  - De novo methods for obtaining metagenomically assembled genomes (MAGs). What are the best pipelines and parameters for ancient DNA?
- **Roundtable** Databases
  - Why are databases so important? What impact does database selection have on my results? What pitfalls should I watch out for?

### DAY 5

- **Lecture** Evolutionary Biology: _Sebastian Duchene_
  - How have microbes and microbial communities evolved and changed through time? How does this inform our current understanding of the relationships among microbes?
- **Practical** Phylogenomics: _Aida Andrades Valtueña and Arthur Kocher_
  - How to perform phylogenetic analysis. What to consider when dealing with low coverage data
- **Practical** Functional Genomics: _Irina Velsko_
  - How can we infer genomic function from sequences? What sort of analysis can we do?
- **Round table** Workshop recap
