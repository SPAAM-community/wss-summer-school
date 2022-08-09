# Day One

## Welcome Presentation

**Instructors**: James Fellows Yates and Christina Warinner

Introduction to the course and general organisation details.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vR4BvNdBFVhar9tYMN_P2fESJV3jx4UNZtKwIBxA8uB8XDxDWUGE_6j-siqXuOTwCmI4Q21eRO9KbXJ/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://raw.githubusercontent.com/SPAAM-community/wss-summer-school/main/docs/assets/slides/2022/0a-welcome/SPAAM%20Summer%20School%202022%20-%200A%20-%20Welcome%20and%20Organisational.pdf).

## Lecture 1A: Introduction to NGS data

**Instructors**: James Fellows Yates

**Abstract**: In this lecture, I will introduce how we are able to convert DNA
molecules to human readable sequences of A, C, T, and Gs, which we can
subsequently can computationally analyse.

The field of Ancient DNA was revolutionised by the
development of 'Next Generation Sequencing' (NGS), which relies on sequencing of millions
of _short_ fragments of DNA in parallel. The global leading DNA sequencing company is Illumina, and the technology used by Illumina is also most popular by palaeogeneticists. Therefore I will describe
how the various technologies behind Illumina next-generation sequencing machines.

I will also describe some important differences in the way different models
of Illumina sequences work, and how this can influence ancient DNA research. Finally I will
introduce the structure of 'FASTQ' files, the most popular file format for representing the
DNA sequence output of NGS sequencing machines.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQA8VEi99wl-vMrZDAItfQ7GlXEjyVJEm-Np6j-GBfzGWDz709lOh-IFh2LKzV3WJGUAQ9HvhxHfich/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://raw.githubusercontent.com/SPAAM-community/wss-summer-school/main/docs/assets/slides/2022/1a-intro-to-ngs/SPAAM%20Summer%20School%202022%20-%201A%20-%20Introduction%20to%20NGS%20Data.pdf).

### Resources

- [https://www.youtube.com/watch?v=fCd6B5HRaZ8](https://www.youtube.com/watch?v=fCd6B5HRaZ8)
- [https://emea.illumina.com/content/dam/illumina-marketing/documents/products/illumina_sequencing_introduction.pdf](https://emea.illumina.com/content/dam/illumina-marketing/documents/products/illumina_sequencing_introduction.pdf)

### Readings

#### Reviews

- Schuster, Stephan C. 2008. “Next-Generation Sequencing Transforms Today’s Biology.” Nature Methods 5 (1): 16–18. [https://doi.org/10.1038/nmeth1156](https://doi.org/10.1038/nmeth1156).
- Shendure, Jay, and Hanlee Ji. 2008. “Next-Generation DNA Sequencing.” Nature Biotechnology 26 (10): 1135–45. [https://doi.org/10.1038/nbt1486](https://doi.org/10.1038/nbt1486).
- Slatko, Barton E., Andrew F. Gardner, and Frederick M. Ausubel. 2018. “Overview of Next-Generation Sequencing Technologies.” Current Protocols in Molecular Biology / Edited by Frederick M. Ausubel... [et Al.] 122 (1): e59. [https://doi.org/10.1002/cpmb.59](https://doi.org/10.1002/cpmb.59).
- Dijk, Erwin L. van, Hélène Auger, Yan Jaszczyszyn, and Claude Thermes. 2014. “Ten Years of next-Generation Sequencing Technology.” Trends in Genetics 30 (9): 418–26. [https://doi.org/10.1016/j.tig.2014.07.001](https://doi.org/10.1016/j.tig.2014.07.001).

#### Sequencing Library Construction

- Kircher, Martin, Susanna Sawyer, and Matthias Meyer. 2012. “Double Indexing Overcomes Inaccuracies in Multiplex Sequencing on the Illumina Platform.” Nucleic Acids Research 40 (1): e3. [https://doi.org/10.1093/nar/gkr771](https://doi.org/10.1093/nar/gkr771).
- Meyer, Matthias, and Martin Kircher. 2010. “Illumina Sequencing Library Preparation for Highly Multiplexed Target Capture and Sequencing.” Cold Spring Harbor Protocols 2010 (6): db.prot5448. [https://doi.org/10.1101/pdb.prot5448](https://doi.org/10.1101/pdb.prot5448).

#### Errors and Considerations

- Ma, Xiaotu, Ying Shao, Liqing Tian, Diane A. Flasch, Heather L. Mulder, Michael N. Edmonson, Yu Liu, et al. 2019. “Analysis of Error Profiles in Deep next-Generation Sequencing Data.” Genome Biology 20 (1): 50. [https://doi.org/10.1186/s13059-019-1659-6](https://doi.org/10.1186/s13059-019-1659-6).
- Sinha, Rahul, Geoff Stanley, Gunsagar Singh Gulati, Camille Ezran, Kyle Joseph Travaglini, Eric Wei, Charles Kwok Fai Chan, et al. 2017. “Index Switching Causes ‘spreading-of-Signal’ among Multiplexed Samples in Illumina HiSeq 4000 DNA Sequencing.” bioRxiv. [https://doi.org/10.1101/125724](https://doi.org/10.1101/125724).
- Valk, Tom van der, Francesco Vezzi, Mattias Ormestad, Love Dalén, and Katerina Guschanski. 2019. “Index Hopping on the Illumina HiseqX Platform and Its Consequences for Ancient DNA Studies.” Molecular Ecology Resources, March. [https://doi.org/10.1111/1755-0998.13009](https://doi.org/10.1111/1755-0998.13009.).

### Questions to think about

- Why is Illumina sequencing technologies useful for aDNA?
- What problems can the 2-colour chemistry technology of NextSeq and NovaSeqs cause in downstream analysis?
- Why is 'Index-Hopping' a problem?
- What is good software to evaluate the quality of your sequencing runs?

## Software

For today's practical sessions, a standard UNIX environment with a (ba)sh shell is necessary (e.g. Linux, OSX) - no additional software is required.

## Practical 1B: Bare Bones Bash 1

**Instructors**: Aida Andrades Valtueña and Thiseas Lamnidis

**Abstract**: Computational work in metagenomics often involves connecting to remote servers to run analyses via the use of command line tools. Bash is a programming language that is used as the main command line interface of most UNIX systems, and hence most remote servers a user will encounter. By learning bash, users can work more efficiently and reproducibly on these remote servers.

In this session we will introduce the basic concepts of bash and the command line. Students will learn how to move around the filesystem and interact with files, how to chain multiple commands together using "pipes", and how to use loops and regular expressions to simplify the running of repetitive tasks.

Finally, students will learn how to create a bash script of their own, that can run a set of commands in sequence. This session requires no prior knowledge of bash or the command line and is meant to serve as an entry-level introduction to basic programming concepts that can be applicable in other programming languages too.

### Slides

For a full screen version on the presentation and press <kbd class="keybd">f</kbd> on your keyboard.

[Intro to Bash](https://spaam-community.github.io/wss-summer-school/assets/slides/2022/1bc-barebonesbash/bbb1/session1.html ":include :type=iframe width=100% height=600px")

PDF version of these slides can be downloaded from [here](https://raw.githubusercontent.com/SPAAM-community/wss-summer-school/main/docs/assets/slides/2022/1bc-barebonesbash/SPAAM%20Summer%20School%202022%20-%201B%20-%20BareBonesBash%201.pdf).

The teaching material for the FULL BareBonesBash course can be found on the [BareBonesBash
website](https://barebonesbash.github.io/)

### Resources

- [https://google.com](https://google.com) (no, not kidding, should always be your first solution!)
- [https://wiki.bash-hackers.org/syntax/pe#substring_removal](https://wiki.bash-hackers.org/syntax/pe#substring_removal)
- [https://linux.die.net/](https://linux.die.net/)
- [https://barebonesbash.github.io](https://barebonesbash.github.io)
- [https://regex.io/](https://regex.io/)
- [https://stackoverflow.com/](https://stackoverflow.com/)
- [https://wiki.bash-hackers.org/](https://wiki.bash-hackers.org/)
- [https://devhints.io/bash](https://devhints.io/bash)

## Practical 1C: Bare Bones Bash 2

### Slides

For a full screen version click on the presentation and press <kbd class="keybd">f</kbd> on your keyboard.

[Intro to Bash](https://spaam-community.github.io/wss-summer-school/assets/slides/2022/1bc-barebonesbash/bbb2/session2.html ":include :type=iframe width=100% height=600px")

PDF version of these slides can be downloaded from [here](https://raw.githubusercontent.com/SPAAM-community/wss-summer-school/main/docs/assets/slides/2022/1bc-barebonesbash/SPAAM%20Summer%20School%202022%20-%201C%20-%20BareBonesBash%202.pdf).

The teaching material for the FULL BareBonesBash course can be found on the [BareBonesBash
website](https://barebonesbash.github.io/)

### Resources

- [https://google.com](https://google.com) (no, not kidding, should always be your first solution!)
- [https://wiki.bash-hackers.org/syntax/pe#substring_removal](https://wiki.bash-hackers.org/syntax/pe#substring_removal)
- [https://linux.die.net/](https://linux.die.net/)
- [https://barebonesbash.github.io](https://barebonesbash.github.io)
- [https://regex.io/](https://regex.io/)
- [https://stackoverflow.com/](https://stackoverflow.com/)
- [https://wiki.bash-hackers.org/](https://wiki.bash-hackers.org/)
- [https://devhints.io/bash](https://devhints.io/bash)

## Roundtable: Introductions

**Chairs**: Tina Warinner and James Fellows Yates

We will go around the group and introduce ourselves, to get familiar what the
range of participants backgrounds and current research are.
