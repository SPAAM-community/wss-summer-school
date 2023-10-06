# Day Five

## Lecture 5A: Evolutionary Biology

**Instructors**: Sebastian Duchene

**Abstract**: Pathogen genome data are an invaluable source of information about the evolution and spread of these organisms. This talk will focus on molecular phylogenetic methods and the insight that they can reveal from improving our understanding of ancient evolution to the epidemiological dynamics of current outbreaks.

The first section will introduce phylognenetic trees and a set of core terms and concepts for their interpretation. Next, it will focus on some of the most popular approaches to inferring phylogenetic trees; those based on genetic distance, maximum likelihood, and Bayesian inference. These methods carry important considerations regarding the process that generated the data, computational capability, and data quality, all of which will be discussed here. Finally, we will direct our attention to examples of analyses of ancient and modern pathogens (e.g. Yersinia pestis, Hepatitis B virus, SARS-CoV-2) and critically assess appropriate choice of models and methods.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vT3-tOQI6WIaZ6nUt-23Dl03me7tuyTkSCq-tad2KRrs5MqF92Ufsr3p1Ddsa5U_3Zr_7rDW5SnYOiS/embed?start=false&loop=true&delayms=3000" frameborder="0" width="1058" height="624" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5a-intro-to-evobio/SPAAM%20Summer%20School%202022%20-%205A%20-%20Evolutionary%20Biology%20and%20Phylogenetics.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/V5VG4aEBeWA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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

<iframe width="560" height="630" src="https://www.youtube.com/embed/eg-0S5S7EpM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>
        <div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.6983184](https://doi.org/10.5281/zenodo.6983184). See instructions on page.

Change into the session directory

```bash
cd /<path>/<to>/5b-phylogenomics/
```

The data in this folder should contain an alignment (snpAlignment_session5.fasta) and a txt file with the ages of the samples that we are going to be working with in this session (`samples.ages.txt`)

Load the conda environment.

```bash
conda activate phylogenomics-functional
```

#### Basic concepts in phylogenomics

Before we start building trees, we are going to recap a few basic concepts in phylogenomics.

##### What is a phylogenetic tree

The Oxford Dictionary defines phylogenetics as "the branch of biology that deals with phylogeny, especially with the deduction of the historical relationships between groups of organisms".

When we are building/computing a phylogeny we are inferring the relationship between organisms based on a set of homologous characters, which are characters that have been inherited from a common ancestor. Those characters can be morphological, which is common in paleontological studies, or molecular characters, which in our case they will be DNA sequences.

To display the relationships between the organism we use phylogenetic trees, which are composed of different elements.

##### Parts of a phylogenetic tree: Nodes and Branches

A phylogenetic tree has different parts:

- The **tips**, which can also be called **leaves**, represent the sampled "individuals". Each of the sequences that you used to reconstruct a tree will be displayed in your tree as tips. In the example, we used sequences A,B,C,D and E, and those appear at the tips of the tree.
- A **node** in the tree represents an ancestor (or ancestral sequences) shared by one or more tips. In the tree we see different nodes displayed, the most rightwards ones represent the ancestors between A and B; and C and D, and if we move toward the left we will see a node representing the ancestor of A,B,C and D, and the most leftwards node represent the common ancestor of all the sequences in our tree.
- **Branches** are the part of the tree that connects each node to other nodes or to the leaves. These represent evolutionary paths between nodes/leaves. The length of these branches is called **branch length** and it can represent different measures depending on the algorithm that you use to infer the phylogenetic tree, such as the number of changes (in the case of for example Maximum Parsimony tree, see Character-based phylogenetic methods), genetic/evolutionary distance (for Neighbour-Joining, see distance-based phylogenetic methods, or for Maximum Likelihood method, see Character-based phylogenetic methods), or the time between two taxa or nodes (for example, trees inferred by BEAST, see Bayesian phylogenetic inference using _BEAST2_).

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/1.png">

##### Types of trees: Ultrametric vs. non-ultrametric

We can have different types of trees depending on how the distance to the root (represents the ancestor shared by all the taxa in the tree):

- In **ultrametric trees** the distance from the root to any of the tips in the tree is the **same**. One typical example of ultrametric tree will be a tree where the branch length represents time and all of our tips were samples in the present.
- In **non-ultrametric trees** the distance from the root to the tips differ from tip to tip. We will find this type of tree when we use algorithms where the branch lengths are calculated based on genetic distance/number of changes.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/2.png">

#### The start: DNA sequence alignment

##### DNA sequence aligment

For this course, our start would be a DNA sequence alignment, however phylogenies can be built using any other source of information that contain homologous characters, such as phenotypic characters inherited from the same ancestor, protein sequences, etc.

We start by collecting the DNA sequences of our organisms/individuals of interest, and now we need to make sure that the positions are homologous, which means that they were inherited from the same ancestor, to ensure that they share the same evolutionary history. A way to ensure that our positions are homologous is by **aligning** our DNA sequences.

There are different ways to produce an alignment from our sequences, and this will depend on the type of data that you have:

- Multiple Sequence Alignment (MSA) can be computed from complete genomes. This can be achieved with _MAFFT_ or _Clustal Omega_. However, this will be computationally expensive to perform on large genomes.
- Reference based alignment: this consists of aligning your reads to a reference genome, and it was covered during the _Practical 4B: Genome mapping_.

> _Note_: for large genomic datasets, we often use Single Nucleotide Polymorphims (SNPs) alignments, i.e. alignments that contain only variable genomic positions. This is to reduce the computational time since the variable positions are the most informative for reconstructing phylogenetic trees.

##### DNA sequence alignment

In this practical session, we will be working with an alignment produced as you learned in the _Practical 4B:Genome mapping_.

We are going to start by exploring the alignment in _MEGA_. So open the _MEGA_ desktop application and load the alignment by clicking on File -> Open A File/Session -> Select the _snpAligment_session5.fasta_.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/3.png">

It will you ask what you want to do with the alignment. In _MEGA_ you can also produce an alignment, however, since our sequences are already aligned we will press on _Analyze_.

Then we will select _Nucleotide Sequences_ since we are working with a DNA alignment. Note that _MEGA_ can also work with Protein Sequences as well as Pairwise Distance Matrix (which we will cover shortly). In the same window, we will change the character for _Missing Data_ to **N** and click in _OK_.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/4.png">

A window would open up asking if our alignment contains protein encoding sequences, and we will select _No_.

> 🛈: If you had protein encoding sequences, you would have selected Yes. This will allow you to treat different positions with different evolutionary modes depending on their codon position. One can do this to take in account that the third codon position can change to different nucleotides without resulting in a different amino acid, while position one and two of the codon are more restricted.

To explore the alignment, you will then click on the box with _TA_

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/5.png">

You will see an alignment containing sequences from the bacterial pathogen _Yersinia pestis_. Within the alignment, we have our sequences of interest (VLI092, CHC004, KZL002) that date between 5000-2000 years Before Present (BP), and we want to know how they relate to the rest of the _Yersinia pestis_ genomes in the alignment.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/6.png">

What do you think the dots represent?

- They represent positions that are same as the reference

What are the Ns in the sequences?

- They represent positions where we have missing data. We told _MEGA_ to encode missing positions as _N_

How many sequences are we analysing?

- We are analysing 33 sequences.

#### Distance-based phylogenetic methods

Distance-based methods calculate the tree from a pairwise distance matrix. The distances in the pairwise distance matrix can represent either:

- Number of differences between to sequences
- p-distance that is calculated as number of differences / total number of sites

For any of the phylogenetic methods, we can also take into account that different sites may evolve differently depending on their nucleotide composition. To take this into account, you will need to use **substitution models**. By applying different evolutionary models, one can take into account multiple consecutive mutations as well as different probabilities to observe a specific mutation given the specific character in this position. There are tools that allow you to choose the substitution model that it is more fitting to you specific alignment, such as jModelTest, ModelGenerator, etc.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/7.png">

##### Calculate a pairwise distance matrix

To calculate a pairwise distance matrix, one will have to check the number of differences between all the possible pair combination between the sequences in the alignment, and in the case of a p-distance normalise the number of differences by the total number of sites. All this differences will be then stored in a matrix.

_MEGA_ also provides a function to calculate Pairwise Distances, for that you will have to click into the Distance symbol, and select _Compute Pairwise Distances_, the output will be a matrix with all the pairwise distances. This will be the first step you will do if you wanted to compute a distance-based phylogeny with methods such as UPGMA or Neighbour-Joining. We will be covering the second method.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/8.png">

##### Calculating a Neighbour-Joining tree

In the slide you have an example on how a small Neighbour-Joining (NJ), with 6 taxa is calculated.

In essence, this method will be grouping taxa that have the shortest distance together first, and will be doing this iteratively until all the taxa/sequences included in your alignment have been placed in a tree.
Luckily, you won't have to do this by hand since _MEGA_ allows you to build a NJ tree.

##### Let's make our own NJ tree

For that go back to _MEGA_ and click on the _Phylogeny_ symbol and then select _Construct Neighbour Joining Tree_. In the window that would pop up, you will then chance the _Model/Method_ to _p-distance_ since we want to normalise by the total number of sites shared by sequences. Then press _OK_ and a window with the calculated phylogenetic tree will pop up.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/9.png">

Since the tree is not easily visualised in _MEGA_, we will export it in newick format (an "standarised" format to write a tree in a computer-readable form) and explore our tree in _FigTree_. This tool has a better interface for visually manipulating trees and allows us to interact with the phylogenetic tree.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/10.png">

To do that you will click on _File_, then _Export current tree (Newick)_ and click on _Branch Lengths_ to include those in the newick annotation. When you press _OK_, a new window with the tree in newick format will pop up and you will then press _File_ -> _Save_ and saved it as _NJ_tree.nwk_ (If you are doing this for your own project, please give your files informative names).

As said above, we will explore own NJ tree in _FigTree_. Open the software and then open the NJ tree by clicking on _File_ -> _Open_ and selecting the file with the NJ tree _NJ_tree.nwk_

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/11.png">

So, which type of tree is this?
Before you answer this question, let me introduce you to another type of trees

##### Type of trees: Rooted vs Unrooted trees

- An _unrooted_ tree does not contain a root. It displays the relationships between our sequences but not the direction in time. In the example, we can not tell if human or chimpanzee or gorilla are more ancestral to each other.
- A _rooted_ tree does contain a root. This root can be calculated based on the inclusion of an outgroup, a known sequenced to be older than any of the taxa in our tree, or by computational methods that can place the root by various methods, being one of such methods the Mid Point Rooting. A rooted tree represents the relationships and the direction in time. By rooting our example tree with the outgroup, we now can tell that gorilla is ancestral to both human and chimpanzees.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/12.png">
##### Let's make our own NJ tree

So if we go back to our question, which type of tree is this?

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/13.png">

Even though a root is displayed by default, this is actually an unrooted tree.
We know that _Yersinia pseudotuberculosis_ (labelled here as _Y. pseudotuberculosis_) is an outgroup to _Yersinia pestis_. You can reroot the tree by selecting _Y.pseudotuberculosis_ and pressing _Reroot_.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/14.png">

Now we have the correct tree.

How many leaves/tips has our tree?

- That's right, it is 33, the same number of sequences that was in our original SNP alignment.

Is it an ultrametric tree?

- No, we can see that root to tip distance is different between taxa. The branch lengths in the NJ tree will represent genetic distance between the different taxa.

Where are our taxa of interest? (KZL002, GZL002, CHC004 and VLI092)

- They all fall ancestral to the rest of _Yersinia pestis_ in this tree.

Do they form a clade?

- All the genomes have a common ancestor and form a single branch, meaning that they form a clade.

Which type of clade?

- To answer this question, let's look at what types of clades we can have in a phylogenetic tree

##### Types of Clades

- A **Monophyletic clade** is a group of taxa that contain all the taxa that share a common ancestor.
- A **Paraphyletic clade** is a group of taxa including all the taxa with a common recent ancestor except one or more taxa. In the example, since A is missing from the clade selected, it won't be anymore a paraphyletic clade rather than a monophyletic. Another common example of paraphyletic clade would be selecting all the reptiles but excluding birds.
- A **Polyphyletic clade** is a group of taxa from different monophyletic clades.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/15.png">

##### Lets make our own NJ tree

Now regarding our question, which type of clade form KZL002, GZL002, CHC004 and VLI092?

Since they all share a common ancestor,they form a monophyletic clade.

Until now we have learned how to explore a SNP alignment, the different part of the a phylogenetic tree and how to make a NJ tree. The NJ tree is based on pairwise distances, which is one of the simplest algorithms to build a tree and now you will see more complex algorithms for phylogenetic tree building.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/16.png">

#### Character-based phylogenetic methods: maximum parsimony and probabilistic approaches

Character-based methods are not based on pairwise distances but rather model the complete evolution of each character (e.g. DNA nucleotides at each position) along the phylogenetic tree.

One of these methods is maximum parsimony and it consists in choosing the tree that underlies an evolutionary history with the least number of character changes.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/17.png">

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/18.png">

Other types of character-based methods which are more commonly used today are probabilistic methods. In general, these are statistical techniques that are based on probabilistic models under which the data that we observe is generated following a probability distribution depending on a set of parameters which we want to estimate.

In a phylogenetic probabilistic model, the data is the sequence alignment and the parameters, are the substitution matrix and the phylogenetic tree. The probability of the data given the model parameters is called the likelihood.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/19.png">            
<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/20.png">

##### Maximum likelihood estimation and bootstrapping

One way we can make inferences from a probabilistic model is by finding the combination of parameters which maximises the likelihood. These parameter values are called maximum likelihood (ML) estimates. We are usually not able to compute the likelihood value for all possible combinations of parameters and have to rely on heuristic algorithms to find the maximum likelihood estimates.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/21.png">

The Maximum likelihood estimates are point estimates, i.e. single parameter values (for example, a tree), which does not allow to measure uncertainty. A classic method to measure the uncertainty of ML tree estimates is bootstrapping, which consists in repeatedly disturbing the alignment by masking sites from it and estimating a tree from each of these bootstrap alignments.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/22.png">

For each clade in the ML tree, a bootstrap support value is computed which corresponds to the proportion of bootstrap trees containing the clade. This gives an indication of how robustly the clade is supported by the data (i.e. whether it holds even after disturbing the dataset). Bootstrapping can be used to measure the topology uncertainty of trees estimated with any inference method.

Here is a command to estimate an ML phylogenetic tree using _RAxML_ (you may find the list of parameters in the _RAxML_ manual):

```bash
raxmlHPC-PTHREADS -m GTRGAMMA -T 3 -f a -x 12345 -p 12345 -N autoMRE -s snpAlignment_session5.fasta -n full_dataset.tre
```

Once the analysis has been completed, you can open the tree using _Figtree_ (RAxML_bipartitions… file, change “label” to “bootstrap support” at the prompt).

The tree estimated using this model is a substitution tree (branch lengths represent genetic distances in subst./site), and it is not oriented in time: this is an unrooted tree (displayed with a random root in Figtree). You can reroot the tree in _Figtree_ using _Y. pseudotuberculosis_ as an outgroup (click on the branch leading to Y. pseudo and then “Reroot”).

Where do our genomes of interest from the LNBA period fall (VLI092, GZL002, CHC004, KZL002), compared to the rest of Yersinia pestis diversity? Is that placement well-supported? (look at the bootstrap support value: click on the “Node Labels” box and open the drop-down menu, change “Node ages” to “bootstrap support”)

You can notice that the phylogeny is difficult to visualize due to the long branch leading to _Y. pseudotuberculosis_. Having a very distant outgroup can also have deleterious effects on the estimated phylogeny (due to long branch attraction). We can construct a new phylogeny after removing the outgroup (go back to the alignment in mega, unclick _Y.pseudotuberculosis_, and export in fasta format), and then reroot the tree based on our previous knowledge: place the root on the branch leading to the LNBA genomes.

Then, export the rooted tree: file > export trees > "save as currently displayed".

##### Estimating a time-tree using Bayesian phylogenetics

Now, we will try to use reconstruct a phylogeny in which the branch lengths do not represent a number of mutations but instead represent the time of evolution. To do so, we will use the sample ages (C14 dates) to calibrate the tree in time. This assumes a molecular clock hypothesis in which substitutions occur at a rate that is relatively constant in time so that the time of evolution can be estimated based on the number of substitutions.

###### Temporal signal testing

It is a good practice to assess if the genetic sequences that we analyse do indeed behave like molecular clocks before trying to estimate a time tree. A classic test to do this is called root-to-tip regression, which consists in verifying that the oldest a sequence is, the closer it should be to the root because there was less time for mutations to accumulate before this sequence was sampled. The correlation between sample age and distance to the root (root-to-tip regression) can be assessed using a rooted substitution tree and the program _tempest_:

- open tempest and load the re-rooted ML tree that we produced previously
- click on "import dates" in the "sample dates" tab, select the sample_age.txt file, and then change to "dates specified as years before the present"
- look at the root-to-tip regression: is there a positive correlation?

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/Tempest.png">

###### Bayesian phylogenetic inference using _BEAST2_

We will estimate a time tree from our alignment using Bayesian inference instead of maximum likelihood.

Bayesian inference is a type of inference which is based on a probability distribution that is different from the likelihood: the posterior probability. The posterior probability is the probability of the parameters given the data. The posterior distribution is easier to interpret than the likelihood because it contains all the information about the parameters: point estimates such as the median or the mean can be directly estimated from it, but also percentile intervals which can be used to measure uncertainty.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/23.png">

The Bayes theorem tells us that is proportional to the product of the likelihood and the "prior" probability of the data:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/equation.png">

Therefore, for Bayesian inference, we need to complement our probabilistic model with prior distributions for all the parameters. Because we want to estimate a time tree, we also add another parameter: the molecular clock (average substitution rate in time units).

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/24.png">

To characterize the full posterior distribution of each parameter, we would need in theory to compute the posterior probability for each possible combination of parameters. This is impossible, and we will instead use an algorithm called Markov chain Monte Carlo (MCMC) to approximate the posterior distribution. The MCMC is an algorithm which iteratively samples values of the parameters from the posterior distribution. Therefore, if the MCMC has run long enough, the (marginal) posterior distribution of the parameters can be approximated by a histogram of the sampled values.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/25.png">

The different components of the _BEAST2_ analysis can be set up in the program _BEAUti_:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/26.png">

- load the alignment in the "Partitions" tab
- set the sampling dates in the "Tip dates" tab
- choose the substitution model in the "Site model" tab
- choose the molecular clock model in the "Clock model" tab
- choose the prior distribution of parameters in the "Priors" tab
- set up the MCMC in the "MCMC" tab

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/27.png">
<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/28.png">
<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/29.png">
<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/30.png">
<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/31.png">

The ["taming the beast" website](https://taming-the-beast.org/tutorials/) has great tutorials to learn setting a _BEAST2_ analysis. In particular, the "Introduction to BEAST2", "Prior selection" and "Time-stamped data" are good starts.

Try running an analysis on the alignment without outgroup using the following:

- don't forget to specify the sample ages correctly
- use a GTR substitution matrix with a Gamma site model and 4 Gamma categories
- use a relaxed clock lognormal model with an initial value of 1E-4
- use a Bayesian Skyline Coalescent tree prior
- change the mean clock prior to a uniform distribution between 1E-6 and 1E-3 subst/site/year
- use 300M iterations for the MCMC chain, and log the parameters and trees each 10,000th iteration

Once the analysis is completed, assess the posterior distribution sampling and parameter estimates by loading the obtained log file into _Tracer_

First, look at the trace of the posterior to check if the MCMC has passed the burn-in phase, and if you have remove all burn-in iterations

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/32.png">

If so you can look at the trace and effective sample size (ESS) value of all parameters, to check that the MCMC has run long enough. The traces should look (more or less) like a "hairy caterpillar", and a rule of thumb is that all ESS values should be above 200. If this is not the case, you should run the MCMC longer (BEAST2 has a -resume option that you can use to extend the MCMC sampling without starting everything from the beginning).

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/33.png">

You can then look at the estimates of your parameter in the top-right panel (mean, median, 95% HPD interval, ...). Note that these are marginal estimates, i.e. integrated over all other parameters.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/34.png">

What is your estimate of the substitution (mean clock) rate?

You can then generate a maximum clade credibility (MCC) tree using _treeAnnotator_.

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5b-intro-to-phylogenomics/MCC.png">

What is your mean estimate for the age of the common ancestor of all _Yersinia pestis_ strains? To which parameter (displayed in beauti) does this corresponds?

</details>

---

### Resources

### Readings

### Questions to think about

## Practical 5C: Functional Genomics

**Instructors**: Irina Velsko and James Fellows Yates

**Abstract**: The value of microbial taxonomy lies in the implied biochemical properties of a given taxon. Historically taxonomy was determined by growth characteristics and cell properties, and more recently through genomic and genetic similarity. The genomic content of microbial taxa, specifically the presence or absence of genes, determine how those taxa interact with their environment, including all the biochemical processes they participate in, both internally and externally. Strains within any microbial species may have different genetic content and therefore may behave strikingly differently in the same environment, which cannot be determined through taxonomic profiling. Functionally profiling a microbial community, or determining all of the genes present independent of the species they are derived from, reveals the biochemical reactions and metabolic products the community may perform and produce, respectively. This approach may provide insights to community activity and environmental interactions that are hidden when using taxonomic approaches alone. In this session we will perform functional profiling of metagenomic communities to assess their genetic content and inferred metabolic pathways.

### Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTbQRU__-fDvsJ09fd1KeZxGRDrtLD8Ab0ZLagN-4s9CKDfv4ekJlyv4RdQBkBPFj4hdjhY1Un4dRAg/embed?start=false&loop=true&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

PDF version of these slides can be downloaded from [here](https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/5c-intro-to-functional-analysis/SPAAM%20Summer%20School%202022%20-%205C%20-%20Function%20Analysis.pdf).

<iframe width="560" height="630" src="https://www.youtube.com/embed/WcwmfiasBGM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>
        <div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.8412642](https://doi.org/10.5281/zenodo.8412642). See instructions on page.

Change into the session directory

```bash
cd /<path>/<to>/5c-functional-genomics/
```

Load the conda environment.

```bash
conda activate functional-profiling
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
