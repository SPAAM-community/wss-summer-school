# Introduction to Ancient Metagenomics Summer School - 2023

<img style="display: block;
  margin-left: auto;
  margin-right: auto;
  width: 30%;" src="assets/images/2023/summerschool2023-photo1.png">

<p style="text-align:center"><b>Many thanks to all the instructors and students for making the second SPAAM summer school a success!</b></p>

## Latest

Applications for the 2023 Introduction to Ancient Metagenomics Summer school is now **closed**!

We were once again over subscribed with almost 100 applications. Decision emails will be sent in a few weeks.

<!-- You can send your application on the following form: [https://survey.academiccloud.de/index.php/773422](https://survey.academiccloud.de/index.php/773422) -->

## What

The **Ancient Metagenomics Summer School** is a 5 day **practical** workshop (block praktikum). Attendees who participated in the entire course will receive 1.5 ECTS points (40 hours of instruction and practicals) from the Jena School for Microbial Communications graduate school (Friedrich Schiller Universität Jena) and a Certificate of Participation by Harvard University.

The course is taught by active researchers of the SPAAM Community (including MPI-EVA in Germany, Harvard University in the US, SciLifeLab in Sweden, and University of Vienna in Austria) and supported by the Werner Siemens Foundation, in collaboration with the Max Planck Harvard Center for the Archaeoscience of the Ancient Mediterranean (MHAAM), the Leibniz Institute for Natural Product Research and Infection Biology, and the Jena School for Microbial Communications. The course coordinators are Dr. James Fellows Yates (james_fellows_yates@eva.mpg.de) and Prof. Dr. Christina Warinner (christina_warinner@eva.mpg.de).

The course will be following the content in the (draft) [Introduction to Ancient Metagenomics textbook](https://www.spaam-community.org/intro-to-ancient-metagenomics-book/).

## Who

The course is aimed at Masters or early-stage PhD students (or equivalent), to a maximum of 40 participants.

You can meet the instructors [here](/2023/instructors.md).

## When

The summer school was held between 31st-4th August 2023, 09:00-17:00 CEST (Berlin Time).

Note the following additional dates:

- **Applications open**: 3rd April 2023
- **Applications close**: 26th May 2023
- **Decision notifications**: from 5th June 2023 onwards

## Where

We will be running this virtual edition of the SPAAM Summer School Introduction to Metagenomics on [Gather.Town](https://gather.town), on the SPAAM workspace [here](https://app.gather.town/app/PlXjb0deog0B4JCq/spaam-community).

If you're not familiar with this platform please see the documentation on the gather.town website, or [this 'Quick Start' video from nf-core](https://nf-co.re/events/2022/bytesize-37-gathertown).

> ⚠️ If you're using Mac/OSX we highly recommend using the desktop app of gather.town rather than your webbrowser, for optimisation purposes.

## What

You will need access to the internet, and a modern web browser - either Google Chrome, Chromium or Microsoft Edge.
Firefox, is also possible, but makes copy-pasting difficult (you will need to press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>alt</kbd> a lot...). Safari isn't recommended.

Each participant will being given a cloud computing node kindly provided by the German [deNBI infrastructure](https://www.denbi.de/cloud) for the duration of the summer school.

Registration links will be sent via email all participants, however detailed instructions on registration procedure can be seen [here](2023/denbi-registration).

Once you've received your link, each participant will need to open the link in their browser. On the Guacamole page please use the username/password und 'Login credentials' [here](https://cloud.denbi.de/wiki/simple_vm/customization/#apache-guacamole). You should then see a desktop environment.

If you get a message about permissions for 'colour management', please use the password described for the 'Ubuntu User' in the next code block below the 'Login Credentials' in the instructions above.

## Schedule

| **Time**    | **Session Type** | **Day 1**                                                               | **Day 2**                                                               | **Day 3**                                         | **Day 4**                          | **Day 5**                               |
| ----------- | ---------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------- | ---------------------------------- | --------------------------------------- |
| 09:00-10:15 | Theoretical      | Welcome & Introduction to NGS data                                      | Introduction to ancient DNA                                             | Introduction to Metagenomics                      | Introduction to microbial genomics | Evolutionary Biology                    |
| 10:15-10:30 |                  | Break                                                                   | Break                                                                   | Break                                             | Break                              | Break                                   |
| 10:30-12:30 | Practical        | BareBonesBash                                                           | Introduction to R and the tidyverse & Introduction to Python and Pandas | Taxonomic Profiling, OTU Tables and Visualisation | Genome assembly                    | Phylogenomics                           |
| 12:30-13:30 |                  | Lunch                                                                   | Lunch                                                                   | Lunch                                             | Lunch                              | Lunch                                   |
| 13:30-15:30 | Practical        | Introduction to R and the tidyverse & Introduction to Python and Pandas | Introduction to Git(Hub) & Introduction to AncientMetagenomeDir (1hr)   | Genome mapping                                    | Decontamination and authentication | Ancient Metagenomic Pipelines & Wrap Up |
| 13:30-15:45 |                  | Break                                                                   | Break                                                                   | Break                                             | Break                              |
| 15:45-17:00 | Roundtable       | Introductions                                                           | Project Organization                                                    | Taxonomic Classifiers                             | Databases                          | Dinner (Leipzig Only)                   |

Lectures and Practical sessions are typically 2 hours, and round-table discussions 1 hour.

\* All times are in CEST (Leipzig, Germany)!

## Contents Overview

### DAY 1

- **Lecture** Introduction to NGS data: _James Fellows Yates_
  - What is NGS sequencing and what does its data look like?
- **Practical** BareBonesBash: _Aida Andrades Valtueña and Thiseas Lamnidis_
  - Introduction to the UNIX command line.
- **Practical** Introduction to R and the tidyverse / Introduction to Python and Pandas: _Clemens Schmid and James Fellows Yates_ / _Kevin Nota and Robin Warner_
  - How to read/write files and run statistical analyses? How to make figures with ggplot2/plotnine
  - (Note: Parallel sessions partcipants can choose which to attend based on their prior experience)
- **Round table** Introductions
  - Welcome - let's get to know eachother

### DAY 2

- **Lecture** Introduction to ancient DNA: _Christina Warinner_
  - How to identify and handle DNA from ancient contexts
- **Practical** Introduction to R and the tidyverse / Introduction to Python and Pandas: _Clemens Schmid and James Fellows Yates_ / _Kevin Nota and Robin Warner_
  - How to read/write files and run statistical analyses? How to make figures with ggplot2/plotnine
  - (Note: Parallel sessions partcipants can choose which to attend based on their prior experience)
- **Practical** Bytesize git: _James Fellows Yates_
  - What is git and github? How to clone a repository? What does commit/pull/push mean?
- **Practical** ancientMetagenomeDir: _James Fellows Yates_
  - Where to get ancient metagenomic comparative data, and why is metadata important?
  - Git practice
- **Round table** Project organisation
  - How to structure my project analysis folders? How to reproducibly document my work?

### DAY 3

- **Lecture** Introduction to Metagenomics: _Christina Warinner_
  - What are the questions tackled in metagenomics? What are the challenges?
- **Practical** Taxonomic Profiling, OTU Tables and Visualisation: _Maxime Borry and Kevin Nota_
  - Python practice. How to normalise OTU tables and perform microbial ecology analyses.
- **Practical** Genome mapping: _Alina Hiss and Alexander Herbig_
  - Why and how do we map against a reference? What parameters are important for aDNA?
- **Round table** Taxonomic Classifiers
  - How do I pick a taxonomic classifier? What is best for aDNA?

### DAY 4

- **Lecture** Introduction to microbial genomics: _Meriam Guellil_
  - How can we learn from studying the genomes of microbes? What questions can we ask?
- **Practical** Genome assembly: _Alex Hübner and Nikolay Oskolkov_
  - De novo methods for obtaining metagenomically assembled genomes (MAGs). What are the best pipelines and parameters for ancient DNA?
- **Practical** Phylogenomics: _Arthur Kocher and Alexander Herbig_
  - How to perform phylogenetic analysis. What to consider when dealing with low coverage data
- **Roundtable** Databases
  - Why are databases so important? What impact does database selection have on my results? What pitfalls should I watch out for?

### DAY 5

- **Lecture** Evolutionary Biology: _Alexander Herbig_
  - How have microbes and microbial communities evolved and changed through time? How does this inform our current understanding of the relationships among microbes?
- **Practical** Authentication and Decontamination: \_Nikolay Oskolkov and James Fellows Yates
  - How can I validate my DNA is ancient? What sort of analyses can convice ourselves and a reviewer we have good preservation?
- **Practical** Ancient Metagenomic Pipelines: _James Fellows Yates and Nikolay Oskolkov_
  - What pipelines exist for specifically ancient DNA and ancient metagenomic data?
- **Round table** Workshop recap
