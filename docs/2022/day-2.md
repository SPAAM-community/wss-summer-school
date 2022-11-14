# Day Two

## Lecture 2A: Introduction to ancient DNA

**Instructors**: Christina Warinner

**Abstract**: This lecture introduces you to ancient DNA and the enormous technological changes that have taken place since the field’s origins in 1984. Starting with the quagga and proceeding to microbes, we discuss where ancient microbial DNA can be found in the archaeological record and examime how ancient DNA is defined by its condition, not by a fixed age. We next cover genome basics and take an in-depth look at the way DNA degrades over time. We detail the fundamentals of DNA damage, including the specific chemical processes that lead to DNA fragmentation and C->T miscoding lesions. We then demystify the DNA damage “smile plot” and explain the how the plot’s symmetry or asymmetry is related to the specific enzymes used to repair DNA during library construction. We discuss how DNA damage is and is not clock-like, how to interpret and troubleshoot DNA damage plots, and how DNA damage patters can be used to authenticate ancient samples, specific taxa, and even sequences. We cover laboratory strategies for removing or reducing damage for greater accuracy for genotype calling, and we discuss the pros and cons of single-stranded library protocols. We then take a closer look at proofreading and non-proofreading polymerases and note key steps in NGS library preparation during which enzyme selection is critical in ancient DNA studies. Finally, we examine the big picture of why DNA damage matters in ancient microbial studies, and its effects on taxonomic identification of sequences, accurate genome mapping, and metagenomic assembly.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRQYqeq8LDnw-McfI8zRvEX2xL77awoP4BLGCBNPj2rorPOxFQOdwnhVosu8qqlnZKqDl5dd6SYt0qf/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/slides/2022/2a-intro-to-adna/SPAAM%20Summer%20School%202022%20-%202A%20-%20Intro%20to%20Ancient%20DNA.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/_8VE72Od7Cg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Resources

### Readings

- Borry, M., Hübner, A., Rohrlach, A. B., & Warinner, C. (2021). PyDamage: automated ancient damage identification and estimation for contigs in ancient DNA de novo assembly. PeerJ, 9, e11845.
- Briggs, A. W., Stenzel, U., Johnson, P. L., Green, R. E., Kelso, J., Prüfer, K., ... & Pääbo, S. (2007). Patterns of damage in genomic DNA sequences from a Neandertal. Proceedings of the National - Academy of Sciences, 104(37), 14616-14621.
- Fellows Yates, J. A., Velsko, I. M., Aron, F., Posth, C., Hofman, C. A., Austin, R. M., ... & Warinner, C. (2021). The evolution and changing ecology of the African hominid oral microbiome. Proceedings - of the National Academy of Sciences, 118(20), e2021655118.
- Gansauge, M.T. and Meyer, M., 2019. A method for single-stranded ancient DNA library preparation. In Ancient DNA (pp. 75-83). Humana Press, New York, NY.
- Higuchi, R., Bowman, B., Freiberger, M., Ryder, O. A., & Wilson, A. C. (1984). DNA sequences from the quagga, an extinct member of the horse family. Nature, 312(5991), 282-284.
- Hofreiter, M., Serre, D., Poinar, H.N., Kuch, M. and Pääbo, S., 2001. Ancient DNA. Nature Reviews Genetics, 2(5), pp.353-359.
- Jónsson, H., Ginolhac, A., Schubert, M., Johnson, P. L., & Orlando, L. (2013). mapDamage2. 0: fast approximate Bayesian estimates of ancient DNA damage parameters. Bioinformatics, 29(13), 1682-1684.
- Meyer, M. and Kircher, M., 2010. Illumina sequencing library preparation for highly multiplexed target capture and sequencing. Cold Spring Harbor Protocols, 2010(6), pp.pdb-prot5448.
- Orlando, L., Allaby, R., Skoglund, P., Der Sarkissian, C., Stockhammer, P. W., Ávila-Arcos, M. C., ... & Warinner, C. (2021). Ancient DNA analysis. Nature Reviews Methods Primers, 1(1), 1-26.
- Rohland, N., Harney, E., Mallick, S., Nordenfelt, S. and Reich, D., 2015. Partial uracil-DNA-glycosylase treatment for screening of ancient DNA. Philosophical Transactions of the Royal Society B: - Biological Sciences, 370(1660), p.20130624.
- Skoglund, P., Northoff, B. H., Shunkov, M. V., Derevianko, A. P., Pääbo, S., Krause, J., & Jakobsson, M. (2014). Separating endogenous ancient DNA from modern day contamination in a Siberian Neandertal.- Proceedings of the National Academy of Sciences, 111(6), 2229-2234.
- Velsko, I. M., Frantz, L. A., Herbig, A., Larson, G., & Warinner, C. (2018). Selection of appropriate metagenome taxonomic classifiers for ancient microbiome research. mSystems, 3(4), e00080-18.
- Warinner, C., Herbig, A., Mann, A., Yates, J. A. F., Weiβ, C. L., Burbano, H. A., ... & Krause, J. (2017). A robust framework for microbial archaeology. Annual Review of Genomics and Human Genetics,- 18, 321.

### Questions to think about

- What is ancient DNA?
- Where do we find ancient DNA from microbes?
- How does DNA degrade?
- How do I interpret a DNA damage plot?
- How is DNA damage used to authenticate ancient genomes and samples?
- What methods are available for managing DNA damage?
- How does DNA damage matter for my analyses?

## Software

For today's practical sessions, please [activate](2022/resources#software-and-data) the `git-eager` conda [environment](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/software/2022/day2.yml).

```bash
conda activate git-eager
```

## Practical 2B: Introduction to Git(Hub)

**Instructors**: Megan Michel

**Abstract**: As the size and complexity of metagenomic analyses continues to expand, effectively organizing and tracking changes to scripts, code, and even data, continues to be a critical part of ancient metagenomic analyses. Furthermore, this complexity is leading to ever more collaborative projects, with input from multiple researchers.

In this practical session, we will introduce 'Git', an extremely popular version control system used in bioinformatics and software development to store, track changes, and collaborate on scripts and code. We will also introduce, GitHub, a cloud-based service for Git repositories for sharing data and code, and where many bioinformatic tools are stored. We will learn how to access and navigate course materials stored on GitHub through the web interface as well as the command line, and we will create our own repositories to store and share the output of upcoming sessions.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vR07xSxl-AaB6df4Mu4BN4X41U5SM41fKy0gvZ7sSSPtqRoF2RqFth-aduhN9nkRpkdzP0N6fb5x5Ok/embed?start=true&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](<https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/slides/2022/2b-intro-to-github/SPAAM%20Summer%20School%202022%20-%202B%20-%20Introduction%20to%20Git(Hub).pdf>).

<iframe width="560" height="630" src="https://www.youtube.com/embed/Eh9TldDahW0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>

<div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The conda environment `.yaml` file for this practical session can be downloaded from here: [https://zenodo.org/record/6983120#.YxdEaOxBz0o](https://zenodo.org/record/6983120#.YxdEaOxBz0o). See instructions on page.

#### Introduction

In this walkthrough, we will introduce the version control system **Git** as well as **Github**, a remote hosting service for version controlled repositories. Git and Github are increasingly popular tools for tracking data, collaborating on research projects, and sharing data and code, and learning to use them will help in many aspects of your own research. For more information on the benefits of using version control systems, see the slides.

#### SSH setup

To begin, you will set up an SSH key to facilitate easier authentication when transferring data between local and remote repositories. In other words, follow this section of the tutorial so that you never have to type in your github password again!
Begin by activating the conda environment for this section (see **Preparation** above).

```bash
conda activate git-eager
```

Next, generate your own ssh key, replacing the email below with your own address.

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

I recommend saving the file to the default location and skipping passphrase setup. To do this, simply press enter without typing anything.

You should now (hopefully!) have generated an ssh key. To check that it worked, run the following commands to list the files containing your public and private keys and check that the ssh program is running.

```bash
cd ~/.ssh/
ls id*
eval "$(ssh-agent -s)"
```

Now you need to give ssh your key to record:

```bash
ssh-add ~/.ssh/id_ed15519
```

Next, open your webbrowser and navigate to your github account. Go to settings -> SSH & GPG Keys -> New SSH Key. Give you key a title and paste the public key that you just generated on your local machine.

```bash
cat ~/.ssh/id_ed15519
```

Finally, press Add SSH key. To check that it worked, run the following command on your local machine. You should see a message telling you that you've successfully authenticated.

```bash
ssh -T git@github.com
```

For more information about setting up the SSH key, including instructions for different operating systems, check out github's documentation: [https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

#### The only 6 commands you really need to know

Now that you have set up your own SSH key, we can begin working on some version controlled data! Navigate to your github homepage and create a new repository. You can choose any name for your new repo (including the default). Add a README file, then select Create Repository.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/master/docs/assets/slides/2022/2b-intro-to-github/create_repo.png">

**Note:** For the remainder of the session, replace the name of my repository (vigilant-octo-journey) with your own repo name.

Change into the directory where you would like to work, and let's get started!
First, we will learn to **clone** a remote repository onto your local machine. Navigate to your new repo, select the _Code_ dropdown menu, select SSH, and copy the address as shown below.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/master/docs/assets/slides/2022/2b-intro-to-github/git_clone.png">

Back at your command line, clone the repo as follows:

```bash
git clone git@github.com:meganemichel/vigilant-octo-journey.git
```

Next, let's **add** a new or modified file to our 'staging area' on our local machine.

```bash
cd vigilant-octo-journey
echo "test_file" > file_A.txt
echo "Just an example repo" >> README.md
git add file_A.txt
```

Now we can check what files have been locally changed, staged, etc. with **status**.

```bash
git status
```

You should see that `file_A.txt` is staged to be committed, but `README.md` is NOT. Try adding `README.md` and check the status again.

Now we need to package or save the changes into a **commit** with a message describing the changes we've made. Each commit comes with a unique hash ID and will be stored forever in git history.

```bash
git commit -m "Add example file"
```

Finally, let's **push** our local commit back to our remote repository.

```bash
git push
```

What if we want to download new commits from our remote to our local repository?

```bash
git pull
```

You should see that your repository is already up-to-date, since we have not made new changes to the remote repo. Let's try making a change to the remote repository's README file (as below). Then, back on the command line, pull the repository again.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/master/docs/assets/slides/2022/2b-intro-to-github/git_pull.png">

#### Working collaboratively

Github facilitates simultaneous work by small teams through branching, which generates a copy of the main repository within the repository. This can be edited without breaking the 'master' version.
First, back on github, make a new branch of your repository.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/master/docs/assets/slides/2022/2b-intro-to-github/git_switch.png">

From the command line, you can create a new branch as follows:

```bash
git switch -c new_branch
```

To switch back to the main branch, use

```bash
git switch main
```

Note that you **must commit changes** for them to be saved to the desired branch!

#### Pull requests

A **Pull request** (aka PR) is used to propose changes to a branch from another branch. Others can comment and make suggestinos before your changes are merged into the main branch.
For more information on creating a pull request, see github's documentation: [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

</div>

</details>

---

### Resources

- [https://www.atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials)
- [https://ohshitgit.com/](https://ohshitgit.com/)

### Readings

- Chacon, Scott, and Ben Straub. 2022. Pro Git. Second Edition. The Expert’s Voice. Apress.

### Questions to think about

1. Why is using a version control software for tracking data and code important?
2. How can using Git(Hub) help me to collaborate on group projects?

## Practical 2C: Introduction to AncientMetagenomeDir

**Instructors**: James Fellows Yates

**Abstract**: Finding relevent comparative data for your ancient metagenomic analysis is not trivial. While palaeogenomicists are very good at uploading their raw sequencing data to large sequencing data repositories such as the EBI's ENA or NCBI's SRA archives in standardised file formats, these files often have limited metadata. This often makes it difficult for researchers to search for and download relevent published data they wish to use use to augment their own analysis.

AncientMetagenomeDir is a community project from the SPAAM community to make ancient metagenomic data more accessible. We curate a list of standardised metadata of all published ancient metagenomic samples and libraries, hosted on GitHub. In this session we will go through how to use the AncientMetagenomeDir repository and associated tools to find and download data for your own analyses. We will also discuss important things to consider when publishing your own data to make it more accessible for other researchers.

### Resources

- [https://github.com/SPAAM-community/AncientMetagenomeDir](https://github.com/SPAAM-community/AncientMetagenomeDir)
- [https://github.com/SPAAM-community/AMDirT](https://github.com/SPAAM-community/AMDirT)

### Readings

- Fellows Yates, James A., Aida Andrades Valtueña, Åshild J. Vågene, Becky Cribdon, Irina M. Velsko, Maxime Borry, Miriam J. Bravo-Lopez, et al. 2021. “Community-Curated and Standardised Metadata of Published Ancient Metagenomic Samples with AncientMetagenomeDir.” Scientific Data 8 (1): 31. [https://doi.org/10.1038/s41597-021-00816-y](https://doi.org/10.1038/s41597-021-00816-y).
- Wilkinson, Mark D., Michel Dumontier, I. Jsbrand Jan Aalbersberg, Gabrielle Appleton, Myles Axton, Arie Baak, Niklas Blomberg, et al. 2016. “The FAIR Guiding Principles for Scientific Data Management and Stewardship.” Scientific Data 3 (March): 160018. [https://doi.org/10.1038/sdata.2016.18](https://doi.org/10.1038/sdata.2016.18).

### Questions to think about

- Why is metadata critical for downloading public data?
- What are suitable places to upload your raw data?
- How should you format your metadata?
- Where should you upload metadata about your samples?

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSkO7KH9YEmHCjMlCRhoxtZrDxZ0cKnsPazEAS3PspBGuhAtA9qhQ0wnPXg64cZrAJZQECngZFfjTRL/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/SPAAM%20Summer%20School%202022%20-%202C%20-%20AncientMetagenomeDir.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/3cYSJtqkNJg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>

<div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.6983130](https://doi.org/10.5281/zenodo.6983130). See instructions on page.

#### Introduction

In most bioinformatic projects, we need to include publically available comparative data to expand or compare our newly generated data with.

Including public data can benefit ancient metagenomic studies in a variety of ways. It can help increase our sample sizes (a common problem when dealing with rare archaeological samples) - thus providing stronger statistical power. Comparison with a range of previously published data of different preservational levels can allow an estimate on the quality of the new samples. When considering solely (re)using public data, we can consider that this can also spawn new ideas, projects, and meta analyses to allow further deeper exploration of ancient metagenomic data (e.g., looking for correlations between various environmental factors and preservation).

Fortuately for us, genomicists and [particularly palaeogenomicists](http://dx.doi.org/10.1371/journal.pone.0121409) have been very good at uploading raw sequencing data to well-established databases.

In the vast majority of cases you will be able to find publically available sequencing data on the [INSDC](https://www.insdc.org/) association of databases, namely the [EBI's European Nucleotide Archive](https://www.ebi.ac.uk/ena/) (ENA), and [NCBI](https://www.ncbi.nlm.nih.gov/sra) or [DDBJ's](https://www.ddbj.nig.ac.jp/dra/index-e.html) Sequence Read Archives (SRA). However, you may in some cases find ancient metagenomic data on institutional FTP servers, domain specific databases (e.g. [OAGR](https://oagr.org)), [Zenodo](https://zenodo.org), [Figshare](https://figshare.com), or [GitHub](https://github.com).

But while the data is publically available, we need to ask whether it is 'FAIR'.

#### Finding Ancient Metagenomic Data

[FAIR principles](http://dx.doi.org/10.1038/sdata.2016.18) were defined by researchers, librarians, and industry in 2016 to improve the quality of data uploads - primarily by making data uploads more 'machine readable'. FAIR standards for:

- Findable
- Accessible
- Interoperable
- Reproducible

And when we consider ancient metagenomic data, we are pretty close to this. Sequencing data is in most cases accessible (via the public databases like ENA, SRA), interoperable and reproducible because we use field standard formats such as FASTQ or BAM files. However _Findable_ remains an issue.

This is because the _metadata_ about each data file is dispersed over many places, and very often not with the data files themselves.

In this case I am referring to metadata such as: What is the sample's name? How old is it? Where is it from? Which enzymes were used for library construction? What sequencing machine was this library sequenced on?

To find this information about a given data file, you have to search many places (main text, supplementary information, the database itself), for different types of metadata (as authors report different things), and also in different formats (text, tables, figures.

This very heterogenous landscape makes it difficult for machines to index all this information (if at all), and thus means you cannot search for the data you want to use for your own reserch in online search engines.

#### AncientMetagenomeDir

This is where the SPAAM community project [AncientMetagenomeDir](https://github.com/spaam-community/AncientMetagenomeDir) comes in. AncientMetagenomeDir is a resource of lists of metadata of all publishing and publically available ancient metagenomes and microbial genome-level enriched samples.

By aggregating and standardising metadata and accession codes of ancient metagenomic samples, the project aims to make it easier for people to find comparative data for their own projects, as well as help track the field over time and facilitate meta analyses.

Currently the project is split over three main tables: host-associated metagenomes (e.g. ancient microbiomes), host-associated single-genomes (e.g. ancient pathogens), and environmental metagenomes (e.g. lakebed cores or cave sediment sequences).

The repository already contains more than a thousand samples and span the entire globe and as far back as hundreds of thousands of years.

To make the lists of samples and their metadata as accessible and interoperable as possible, we utilise simple text (TSV - tab separate value) files - files that can be opened by pretty much all spreadsheet tools (e.g., Microsoft Office excel, LibreOffice Calc) and languages (R, Python etc.).

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/ancientmetagenomedir-example.png">

Criticially, by standardising the recorded all metadata across all publications this makes it much easier for researchers to filter for particular time periods, geographical regions, or sample types of their interest - and then use the also recorded accession numbers to efficiently download the data.

At their core all different AncientMetagenomeDir tables must have at 6 minimum metadata sets:

- Publication information (doi)
- Sample name(s)
- Geographic location (e.g. country, coordinates)
- Age
- Sample type (e.g. bone, sediment, etc.)
- Data Archive and accessions

Each table then has additional columns depending on the context (e.g. what time of microbiome is expected for host-associated metagenoes, or species name of the genome that was reconstructed).

The AncientMetagenomeDir project already has 3 releases, and will continued to be regularly updated as the community continues to submit new metadata of samples of new publications as they come out.

#### Further Improving Metadata Reporting in Ancient Metagenomics

However, for researchers, sample-level metadata likely will not include all the information that is needed to include and process public data in their own projects.

The SPAAM community have been busy over the last few months extending the types of metadata included in the AncientMetagenomeDir project, to include library level metadata.

This metadata includes things such as whether a given set of data files contain sequencing data sequenced on which platform, whether the libraries have undergone damage treatment in the lab, or whether the uploaded data contains all or only mapped reads.

We have also started a new project - a MIxS checklist currently entitled 'MINAS' - which we aim to make _the_ standard metadata reporting sheet for all ancient metagenomics and even for any ancient DNA sample. Such a checklist would be interegrated into services such as the ENA or SRA, and therefore would standardise metadata _alongside_ the raw data, and make ancient metagenomic data much more _findable_ with search engines.

Finally, to make it easier for researchers who are not familiar with sequencing database infrastucture, we are in the process of building a new tool (something already in a usable state) called [AMDirT](https://github.com/SPAAM-community/AMDirT). This allows a web browser-based GUI to filter and select data, and produce scripts for you to download all the selected data (without having to go to the databases themselves).

This is something we are going to try out now!

#### Running AMDirT

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-title.png">

First, we will need to activate a conda environment, and then install the latest development version of the tool for you.

> ⚠️ this tutorial will require a web-browser! Make sure to run on your local laptop/PC or on a server with X11 forwarding

Open your terminal, and run the following two commands:

```bash
conda activate git-eager
pip install --upgrade --force-reinstall git+https://github.com/SPAAM-community/AMDirT.git@dev
```

Once that (hopefully) installs correctly, we can load the tool by running

```bash
AMDirT filter
```

Your web browser should now load, and you should see a two panel page.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-firstpage.png">

Under **Select a table** use the dropdown menu to select 'ancientsinglegenome-hostassociated'.

You should then see a table, pretty similar what you are familiar with with spreadsheet tools such as Microsoft Excel or LibreOffice calc.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-projectfilter.png">

To navigate, you can scroll down to see more rows, and press <kbd>shift</kbd> and scroll to see more columns, or use click on a cell and use your arrow keys (<kbd>⬆</kbd>,<kbd>⬇</kbd>,<kbd>⬅</kbd>,<kbd>➡</kbd>) to move around the table.

You can reorder columns by clicking on the column name, and also filter by pressing the little 'burger' icon that appears on the column header when you hover over a given column.

As an exercise, we will try filtering to a particular set of samples, then generate some download scripts, and download the files.

First, filter the **project_name** column to 'Kocher2021'.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-projectfilter2.png">

Then scroll to the right, and filter the **geo_loc_name** to 'United Kingdom'.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-geofilter.png">

You should be left with 4 rows.

Finally, scroll back to the first column and tick the boxes of these four samples.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-tickbox.png">

Once you've selected the samples you want, you can press **Validate selection**. You should then see a series loading-spinner, and new buttons should appear!

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/2c-intro-to-ancientmetagenomedir/amdirt-validated.png">

You should have three main buttons:

- **Download Curl sample download script**
- **Download nf-core/eager input TSV**
- **Download Citations as BibText**

The first button is for generating a download script that will allow you to immediately download all sequencing data of the samples you selected. The second button is a pre-configured input file for use in the nf-core/eager ancient DNA pipeline, and finally, the third button generates a text file with (in most cases) all the citations of the data you downloaded, in a format accepted by most reference/citation managers.

It's important to note you are not necessarily restricted to [Curl](https://curl.se/) for downloading the data, or [nf-core/eager](https://nf-co.re/eager) for running the files. AMDirT aims to add support for whatever tools or pipelines requested by the community. For example, an already supported download alternative is with the [nf-core/fetchNGS](https://nf-co.re/fetchngs) pipeline. You can select these using the drop-down menus on the left hand-side.

Press the three buttons to make sure you download the files. And once this is done, you can close the tab of the web browser, and in the terminal you can press <kbd>ctrl</kbd> + <kbd>c</kbd> to shutdown the tool.

#### Inspecting AMDirT Output

Lets look at the files that AMDirT has generated for you.

First you should `cd` into the directory that your web browser downloaded the files into (e.g. `cd ~/Downloads/`), then look inside the directory. You should see the following three files

```bash
$ ls
ancientMetagenomeDir_curl_download_script.sh
ancientMetagenomeDir_citations.bib
ancientMetagenomeDir_eager_input.csv
```

We can simple run `cat` on each file to look inside. If you run `cat` on the curl download script, you should see a series of `curl` commands with the correct ENA links for you for each of the samples you wish to download.

```bash
$ cat ancientMetagenomeDir_curl_download_script.sh
#!/usr/bin/env bash
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/009/ERR6053619/ERR6053619.fastq.gz -o ERR6053619.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/008/ERR6053618/ERR6053618.fastq.gz -o ERR6053618.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/005/ERR6053675/ERR6053675.fastq.gz -o ERR6053675.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/006/ERR6053686/ERR6053686.fastq.gz -o ERR6053686.fastq.gz
```

By providing this script for you, AMDirT facilitates fast download of files of interest by replacing the one-by-one download commands for each sample with a _single_ command!

```bash
$ bash ancientMetagenomeDir_curl_download_script.sh
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/009/ERR6053619/ERR6053619.fastq.gz -o ERR6053619.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/008/ERR6053618/ERR6053618.fastq.gz -o ERR6053618.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/005/ERR6053675/ERR6053675.fastq.gz -o ERR6053675.fastq.gz
curl -L ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR605/006/ERR6053686/ERR6053686.fastq.gz -o ERR6053686.fastq.gz
```

Running this command should result in progress logs of the downloading of the data of the four selected samples!

Once the four samples are downloaded, AMDirT then facilitates fast processing of the data, as the _eager_ script can be given directly to nf-core/eager as input. Importantly by including the library metadata (mentioned above), researchers can leverage the complex automated processing that nf-core/eager can perform when given such relevant metadata.

```bash
$ cat ancientMetagenomeDir_eager_input.csv
Sample_Name	Library_ID	Lane	Colour_Chemistry	SeqType	Organism	Strandedness	UDG_Treatment	R1	R2	BAM
I0157	ERR6053618	0	4	SE	Homo sapiens	double	unknown	ERX5692504_ERR6053618.fastq.gz	NA	NA
I0161	ERR6053619	0	4	SE	Homo sapiens	double	unknown	ERX5692505_ERR6053619.fastq.gz	NA	NA
OAI017	ERR6053675	0	4	SE	Homo sapiens	double	half	ERX5692561_ERR6053675.fastq.gz	NA	NA
SED009	ERR6053686	0	4	SE	Homo sapiens	double	half	ERX5692572_ERR6053686.fastq.gz	NA	NA
```

Finally, we can look into the `citations file` which will provide you with the citation information of all the downloaded data and AncientMetagenomeDir itself.

> ⚠️ the contents of this file is reliant on indexing of publications on CrossRef. In some cases not all citations will be present, so this should be double checked!

```bash
$ cat ancientMetagenomeDir_citations.bib

@article{Fellows_Yates_2021,
	doi = {10.1038/s41597-021-00816-y},
	url = {https://doi.org/10.1038%2Fs41597-021-00816-y},
	year = 2021,
	month = {jan},
	publisher = {Springer Science and Business Media {LLC}},
	volume = {8},
	number = {1},
	author = {James A. Fellows Yates and Aida Andrades Valtue{\~{n}}a and {\AA}shild J. V{\aa}gene and
	Becky Cribdon and Irina M. Velsko and Maxime Borry and Miriam J. Bravo-Lopez and Antonio Fernandez-Guerra
	and Eleanor J. Green and Shreya L. Ramachandran and Peter D. Heintzman and Maria A. Spyrou and Alexander
	Hübner and Abigail S. Gancz and Jessica Hider and Aurora F. Allshouse and Valentina Zaro and Christina Warinner},
	title = {Community-curated and standardised metadata of published ancient metagenomic samples with {AncientMetagenomeDir}},
	journal = {Scientific Data}
}
```

This file can be easily loaded into most reference managers and then have all the citations quickly added to your manuscripts.

#### Git Practise

A critical factor of AncientMetagenomeDir is that it is community-based. The community curates all new submissions to the repository, and this all occurs with Git.

The data is hosted and maintained on GitHub - new publications are evaluated on issues, submissions created on branches, made by pull requests, and PRs reviewed by other members of the community.

You can see the workflow in the image below from the AncientMetageomeDir [publication](https://doi.org/10.1038/s41597-021-00816-y), and read more about the workflow on the AncientMetagenomeDir [wiki](https://github.com/SPAAM-community/AncientMetagenomeDir/wiki)

<!-- INSERT IMAGE  HERE-->

This means we can also use this repository to practise git!

Your task (with `git` terms removed):

1. Make a 'copy' the [jfy133/AncientMetagenomeDir](https://github.com/jfy133/AncientMetagenomeDir) repository to your account
2. 'Download' the copied repo to your local machine
3. 'Change' to the `dev` branch
4. Modify ‘ancientsinglegenome-hostassociated_samples.tsv’
   - Click [here](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/data/2022/ancientmetagenomedir_example.tsv) to get some example data to copy in to the end of the TSV file
5. 'Send' back to Git(Hub)
6. Open a 'request' adding changes to the original repo
   - Make sure to put 'Summer school' in the title of the 'Request'

<details>
    <summary>Click me to reveal the correct terminology</summary>

1. **Fork** the [jfy133/AncientMetagenomeDir](https://github.com/jfy133/AncientMetagenomeDir) repository to your account
2. **Clone** the copied repo to your local machine
3. **Switch** to the `dev` branch
4. Modify ‘ancientsinglegenome-hostassociated_samples.tsv’
   - Click [here](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/data/2022/ancientmetagenomedir_example.tsv) to get some example data to copy in to the end of the TSV file
5. **Commit** and **Push** back to your **Fork** on Git(Hub)
6. Open a **Pull Request** adding changes to the original jfy133/AncientMetagenomeDir repo
   - Make sure to put 'Summer school' in the title of the pull request

</details>

#### Summary

- Reporting of metadata messy! Consider when publishing your own work!
  - Use AncientMetagenomeDir as a template
- Use AncientMetagenomeDir and AMDirT (beta) to rapidly find public ancient metagenomic data
- Contribute to AncientMetagenomeDir with git
  - Community curated!

</div>

</details>

---

## Practical 2D: Introduction to nf-core/eager

**Instructors**: Megan Michel and James Fellows Yates

**Abstract**: Analyses in the field of ancient DNA are growing, both in terms of the number of samples processed and in the diversity of our research questions and analytical methods. Computational pipelines are a solution to the challenges of big data, helping researchers to perform analyses efficiently and in a reproducible fashion. Today we will introduce nf-core/eager, one of several pipelines designed specifically for the preprocessing, analysis, and authentication of ancient next-generation sequencing data.

In this practical session we will learn how to perform basic analyses with nf-core/eager, starting from raw data and performing preprocessing, alignment, and genotyping of several _Yersinia pestis_-positive samples. We will gain an appreciation of the diversity of analyses that can be performed within nf-core eager, as well as where to find additional information for customizing your own nf-core/eager runs. Finally, we will learn how to use nf-core/eager to evaluate the quality and authenticity of our ancient samples. After this session, you will be ready to strike out into the world of nf-core/eager and build your own analyses from scratch!

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQ96Xk7UUc71fwdjxCEgxPoGPLiO6xKRLAH5scnGnZrFm3WK5AEndp9mpwzWJQeD4SLjKhWU6BGs92t/embed?start=true&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/raw/main/docs/assets/slides/2022/2d-intro-to-nfcoreeager/SPAAM%20Summer%20School%202022%20-%202D%20-%20Introduction%20to%20nf-core_eager.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/qDjkUfcGmmo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>

<div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The conda environment .yaml file for this practical session can be downloaded from here: https://doi.org/10.5281/zenodo.6983130. See instructions on page.

For this session we will be analyzing two ancient individuals that were positive for _Yersinia pestis_, the etiological agent of plague. Four libraries from these two samples were published in [Yu _et al._ 2020](https://pubmed.ncbi.nlm.nih.gov/32437661/) and [Andrades Valtueña _et al._ 2022](https://pubmed.ncbi.nlm.nih.gov/35412864/). Since the data are too large to be hosted on GitHub, we have provided a script for downloading them directly from NCBI.

To access this data, clone the _wss-summer-school_ repo from github. For help on how to do this, see our tutorial **Introduction to Git(Hub)**.

Once you have successfully cloned the repository, navigate to the directory `/wss-summer-school/docs/assets/data/2022/eager_tutorial`. This is the directory in which we will perform the following analyses.

First, use the curl script provided to download fastq files from NCBI:

```
cd data
bash ancientMetagenomeDir_curl_download_script.sh
cd ..
```

Once this process executes successfully, you are ready to proceed with the rest of the tutorial!

#### Introduction

A **pipeline** is a series of linked computational steps, where the output of one process becomes the input of the next. Pipelines are critical for managing the huge quantities of data that are now being generated regularly as part of ancient DNA analyses. Today we will discuss one option for managing computational analyses of ancient next-generation sequencing datasets, nf-core/eager [@]. Keep in mind that other tools, like the Paleomix pipeline, can also be used for similar applications.

#### What is nf-core/eager?

nf-core/eager is a computational pipeline specifically designed for preprocessing and analysis of ancient DNA data. It is a reimplementation of the previously published EAGER (Efficient Ancient Genome Reconstruction) pipeline [(Peltzer _et al._ 2016)](https://pubmed.ncbi.nlm.nih.gov/27036623/) using **Nextflow**. The nf-core/eager pipeline was designed with the following aims in mind:

1. **Portability**- In order for our analyses to be reproducible, others should be able to easily implement our computational pipelines. nf-core/eager is highly portable, providing easy access to pipeline tools and facilitating use across multiple platforms. nf-core eager utilizes Docker, Conda, and Singularity for containerization, enabling distrubition of the pipeline in a self-contained bundle containing all the code, packages, and libraries needed to run it.
2. **Reproducibility**- nf-core/eager uses custom configuration profiles to specify both HPC-level parameters and analyses-specific options. These profiles can be shared alongside your publication, making it easier for others to reproduce your methodology!
3. **New Tools**- Finally, nf-core/eager includes additional, novel methods and tools for analysis of ancient DNA data that were not included in previous versions. This is especially good news for folks interested in microbial sciences, who can take advantage of new analytical pathways for metagenomic analysis and pathogen screening.

#### Steps in the pipeline

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/megan_walkthrough/docs/assets/slides/2022/2d-intro-to-nfcoreeager/eager2_metromap_complex.png">

A detailed description of steps in the pipeline is available as part of nf-core/eager's extensive documentation. For more information, check out the usage documentation [here](https://nf-co.re/eager/2.4.5/usage).

Briefly, nf-core/eager takes standard input file types that are shared across the genomics field, including raw fastq files, aligned reads in bam format, and a reference fasta. nf-core/eager can perform preprocessing of this raw data, including adapter clipping, read merging, and quality control of adapter-trimmed data. Note that input files can be specified using wildcards OR a standardized tsv format file; the latter facilitates streamlined integration of multpile data types within a single EAGER run! More on this later.

nf-core/eager facilitates mapping using a variety of field-standard alignment tools with configurable parameters. An exciting new addition in nf-core/eager also enables analysis of off-target host DNA for all of you metagenomics folks out there. Be sure to check out the functionality available for metagenomic profiling (blue route in the 'tube map' above).

nf-core/eager incorporates field-standard quality control tools designed for use with ancient DNA so that you can easily evaluate the success of your experiments. Multiple genotyping approaches and additional analyses are available depending on your input datatype, organism, and research questions. Importantly, all of these processes generate data that we need to compile and analyze in a coherent way. nf-core eager uses [MultiQC](https://multiqc.info/). to create an integrated html report that summarizes the output/results from each of the pipeline steps. Stay tuned for the practical portion of the walkthrough!

#### How to build an EAGER command: A practical introduction

For the practical portion of the walkthrough, we will utilize sequencing data from four aDNA libraries, which you should have already downloaded from NCBI. If not, please see the **Preparation** section above.

These four libraries come from from two ancient individuals, GLZ002 and KZL002. GLZ002 comes from the Neolithic Siberian site of Glazkovskoe predmestie adn was radiocarbon dated to 3081-2913 calBCE. KZL002 is an Iron Age individual from Kazakhstan, radiocarbon dated to 2736-2457 calBCE. Both individuals were infected with the so-called 'Stone Age Plague' of _Yersinia pestis_, and libraries from these individuals were processed using hybridization capture to increase the number of _Y. pestis_ sequences available for analysis.

Our aims in the following tutorial are to:

1. Preprocess the fastq files by trimming adapters and merging paired-end reads
2. Align reads to the _Y. pestis_ reference and compute the endogenous DNA percentage
3. Filter the aligned reads to remove host DNA
4. Remove duplicate reads for accurate coverage estimation and genotyping
5. Merge data by sample and perform genotyping on the combined dataset
6. Review quality control data to evaluate the success of the previous steps

Let's get started!

First, activate the conda environment that we downloaded during setup:

`conda activate git-eager`

Next, download the latest version of the nf-core/eager repo (or check for updates if you have a previously-installed version):

`nextflow pull nf-core/eager`

Finally, we will build our eager command:

```bash
nextflow run nf-core/eager 	// Tells nextflow to execute the EAGER pipeline
-r 2.4.5 -ds1l	// Specifies which pipeline and Nextflow versions to run for reproducibility
-profile conda	// Profiles configure your analysis for specific computing environments/analyses
--fasta ../reference/GCF_001293415.1_ASM129341v1_genomic.fna	// Sprecify reference in fasta format
--input ancientMetagenomeDir_eager_input.tsv	// Specify input in tsv format or wildcards
--run_bam_filtering --bam_unmapped_type fastq	// Filter unmapped reads and save in fastq format
--run_genotyping --genotyping_tool ug --gatk_ug_out_mode EMIT_ALL_SITES	// Run genotyping with the GATK UnifiedGenotyper
--run_bcftools_stats	// Generate variant calling statistics
```

For full parameter documentation, click [here](https://nf-co.re/eager/2.4.5/parameters).

And now we wait...

#### Top Tips for EAGER success

1. Screen sessions

Depending on your input data, infrastructre, and analyses, running nf-core/eager can take hours or even days. To avoid crashed due to loss of power or network connectivity, try running nf-core/eager in a screen or tmux session:

`screen -R eager`

2. Multiple ways to supply input data

In this tutorial, a tsv file to specify our input data files and formats. This is a powerful approach that allows nf-core eager to intelligently apply analyses to certain files only (e.g. merging for paired-end but not single-end libraries). Check out the contents of our tsv input file using the following command:

`cat ancientMetagenomeDir_eager_input.tsv`

Inputs can also be specified using wildcards, which can be useful for fast analyses with simple input data types (e.g. same sequencing configuration, file location, etc.).

```
nextflow run nf-core/eager -r 2.4.5 -ds1l -profile conda --fasta ../reference/GCF_001293415.1_ASM129341v1_genomic.fna
--input "data/*fastq.gz" <...>
```

See the online nf-core/eager documentation for more details.

3. Get your MultiQC report via email

If you have GNU mail or sendmail set up on your system, you can add the following flag to send the MultiQC html to your email upon run completion:

`--email "your_address@something.com"`

4. Check out the EAGER GUI

For folks who might be less comfortable with the command line, check out the nf-core/eager [GUI](https://nf-co.re/launch?id=1664901787_8f819102c461)! The GUI also provides a full list of options with short explanations for those interested in learning more about what the pipeline can do.

5. When something fails, all is not lost!

When individual jobs fail, nf-coreager will try to automatically resubmit that job with increased memory and CPUs (up to two times per job). When the whole pipeline crashes, you can save time and computational resources by resubmitting with the `-resume` flag. nf-core/eager will retrieve cached results from previous steps as long as the input is the same.

6. Monitor your pipeline in real time with the Nextflow Tower

Regular users may be interested in checking out the Nextflow Tower, a tool for monitoring the progress of Nextflow pipelines in real time. Check [here](https://help.tower.nf/22.2/) for more information.

</div>

</details>

---

### Resources

- nf-core/eager pipeline documentation: [https://nf-co.re/eager](https://nf-co.re/eager)
- nf-core/eager parameter documentation: [https://nf-co.re/eager/2.4.4/parameters](https://nf-co.re/eager/2.4.4/parameters)
- nf-core/eager GUI: [https://nf-co.re/eager/launch](https://help.tower.nf/22.2/)
- nf-core tower documentation: [https://help.tower.nf/22.2/](https://help.tower.nf/22.2/)

### Readings

- Fellows Yates, James A., Thiseas C. Lamnidis, Maxime Borry, Aida Andrades Valtueña, Zandra Fagernäs, Stephen Clayton, Maxime U. Garcia, Judith Neukamm, and Alexander Peltzer. 2021. “Reproducible, Portable, and Efficient Ancient Genome Reconstruction with Nf-Core/eager.” PeerJ 9 (March): e10947. [https://doi.org/10.7717/peerj.10947](https://doi.org/10.7717/peerj.10947).
- Peltzer, Alexander, Günter Jäger, Alexander Herbig, Alexander Seitz, Christian Kniep, Johannes Krause, and Kay Nieselt. 12/2016. “EAGER: Efficient Ancient Genome Reconstruction.” Genome Biology 17 (1). [https://doi.org/10.1186/s13059-016-0918-z](https://doi.org/10.1186/s13059-016-0918-z).
- Schubert, Mikkel, Luca Ermini, Clio Der Sarkissian, Hákon Jónsson, Aurélien Ginolhac, Robert Schaefer, Michael D. Martin, et al. 2014. “Characterization of Ancient and Modern Genomes by SNP Detection and Phylogenomic and Metagenomic Analysis Using PALEOMIX.” Nature Protocols 9 (5): 1056-82. [https://doi.org/10.1038/nprot.2014.063](https://doi.org/10.1038/nprot.2014.063).
- Orlando, Ludovic, Robin Allaby, Pontus Skoglund, Clio Der Sarkissian, Philipp W. Stockhammer, María C. Ávila-Arcos, Qiaomei Fu, et al. 2021. “Ancient DNA Analysis.” Nature Reviews Methods Primers 1 (1): 1-26. [https://doi.org/10.1038/s43586-020-00011-0](https://doi.org/10.1038/s43586-020-00011-0).
- Warinner, Christina, Alexander Herbig, Allison Mann, James A. Fellows Yates, Clemens L. Weiß, Hernán A. Burbano, Ludovic Orlando, and Johannes Krause. 2017. “A Robust Framework for Microbial Archaeology.” Annual Review of Genomics and Human Genetics 18 (1): 321-56.[https://doi.org/10.1146/annurev-genom-091416-035526](https://doi.org/10.1146/annurev-genom-091416-035526).

### Questions to think about

1. Why is it important to use a pipeline for genomic analysis of ancient data?
2. How can the design of the nf-core/eager pipeline help researchers comply with the FAIR princples for management of scientific data?
3. What metrics do you use to evaluate the success/failure of ancient DNA sequencing experiments? How can these measures be evaluated when using nf-core/eager for data preprocessing and analysis?

## Roundtable: Project organisation

**Chairs**: Alexander Hübner and James Fellows yates

We will discuss the various ways how to structure analysis folders for your research in a manner that promotes portability and reproducibility. Participants can ask for advice and suggestions from the instructors for their specific research projects.

### Resources

- [https://github.com/paleobiotechnology/analysis-project-structure](https://github.com/paleobiotechnology/analysis-project-structure)
