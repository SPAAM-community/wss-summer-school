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

### Walkthrough

---

<details>
    <summary>Click me to view the walkthrough</summary>

<div style="border-style: none none none solid;border-left-color:#74d1f6;border-left-width=2px;padding:10px">

#### Mapping to a Reference Genome

One way of reconstructing genomic information from DNA sequencing reads is mapping/aligning them to a reference genome. This allows for identification of differences between the genome from your sample and the reference genome. This information can be used for example for comparative analyses such as in phylogenetics. For a detailed explanation of the read alignment problem and an overview of concepts for solving it, please see [https://doi.org/10.1146/annurev-genom-090413-025358](https://doi.org/10.1146/annurev-genom-090413-025358).

In this session we will map two samples to the _Yersinia pestis_ (plague) genome using different parameter sets. We will do this "manually" in the sense that we will use all necessary commands one by one in the terminal. These commands usually run in the back when you apply DNA sequencing data processing pipelines.

##### Preparation

The data and conda environment `.yaml` file for this practical session can be downloaded from here: [https://doi.org/10.5281/zenodo.6983119](https://doi.org/10.5281/zenodo.6983119). See instructions on page.

We will open a terminal and then navigate to the working directory of this session:

```bash
cd /<path>/<to>/4b-genome-mapping/
```

Then, we need to activate the conda environment of this session. By this all the necessary tools can be accessed in the current terminal session:

```bash
conda activate microbial-genomics
```

We will be using the Burrows-Wheeler Aligner
(Li et al. 2009 – [http://bio-bwa.sourceforge.net](http://bio-bwa.sourceforge.net)). There are
different algorithms implemented for different types of data (e.g. different read lengths).
Here, we use BWA backtrack (_bwa aln_), which is well suitable for Illumina sequences up to 100bp.
Other algorithms are _bwa mem_ and _bwa sw_ for longer reads.

##### Reference Genome

For mapping we need a reference genome in FASTA format. Ideally we use a genome from the same species that our data relates to or, if not available, a closely related species. The selection of the correct reference genome is highly relevant. E.g. if the chosen genome differs too much from the organism the data relates to, it might not be possible to map most of the reads.
Reference genomes can be retrieved from comprehensive databases such as [NCBI](https://www.ncbi.nlm.nih.gov/).

In your directory, you can find 2 samples and your reference.
As a first step we will index our reference genome (make sure you are inside your directory).

The first index we will generate is for _bwa_.

```bash
bwa index YpestisCO92.fa
```

The second index will be used by the genome browser we will apply to our results later on:

```bash
samtools faidx YpestisCO92.fa
```

We need to build a third index that is necessary for the genotyping step, which comes later after mapping:

```bash
picard CreateSequenceDictionary R=YpestisCO92.fa
```

##### Mapping Parameters

We will be using _bwa aln_, but we need to specify parameters.
For now we will concentrate on the "seed length" and the "maximum edit distance". We will use the default setting for all other parameters during this session. The choice of the right parameters depend on many factors such as the type of data and the specific use case. One aspect is the mapping sensitivity, i.e. how different a read can be from the chosen reference and still be mapped. In this context we generally differentiate between _strict_ and _lenient_ mapping parameters.

As many other mapping algorithms _bwa_ uses a so-called "seed-and-extend" approach. I.e. it initially maps the first _N_ nucleotides of each read to the genome with relatively few mismatches and thereby determines candidate positions for the more time-intensive full alignment.

A short seed length will generate more such candidate positions and therefore mapping will take longer, but it will also be more sensitive, i.e. there can be more differences between the read and the genome. Long seeds are less sensitive but the mapping procedure is faster.

In this session we will use the following two parameter sets:

**Lenient**

Allow for more mismatches → -n 0.01

Short seed length → -l 16

**Strict**

Allow for less mismatches → -n 0.1

Long seed length → -l 32

We will be working with pre-processed files (`sample1.fastq.gz`, `sample2.fastq.gz`), i.e. any quality filtering and removal of sequencing adapters is already done.

We will map each file once with lenient and once with strict parameters.
For this, we will make 4 separate directories, to avoid mixing up files:

```bash
mkdir sample1_lenient sample2_lenient sample1_strict sample2_strict
```

##### Mapping Sample1

Let’s begin with a lenient mapping of sample1.

Go into the corresponding folder:

```bash
cd sample1_lenient
```

Perform the _bwa_ alignment, here for sample1, and specify lenient mapping parameters:

```bash
bwa aln -n 0.01 -l 16 ../YpestisCO92.fa ../sample1.fastq.gz > reads_file.sai
```

Proceed with writing the mapping in _sam_ format ([https://en.wikipedia.org/wiki/SAM\_(file_format)](<https://en.wikipedia.org/wiki/SAM_(file_format)>)):

```bash
bwa samse -r '@RG\tID:all\tLB:NA\tPL:illumina\tPU:NA\tSM:NA' ../YpestisCO92.fa reads_file.sai ../sample1.fastq.gz > reads_mapped.sam
```

Note that we have specified the sequencing platform (Illumina) by creating a so-called "Read Group" (`-r`).
This information is used later during the genotyping step.

Convert SAM file to binary format (BAM file):

```bash
samtools view -b -S reads_mapped.sam > reads_mapped.bam
```

For processing of _sam_ and _bam_ files we use _SAMtools_ (Li et al. 2009 – [http://samtools.sourceforge.net/](http://samtools.sourceforge.net/)).

`-b` specifies to output in BAM format.
(`-S` specifies input is SAM, can be omitted in recent versions.)

Now we sort the _bam_ file → Sort alignments by leftmost coordinates:

```bash
samtools sort reads_mapped.bam > reads_mapped_sorted.bam
```

The sorted bam file needs to be indexed → more efficient for further processing:

```bash
samtools index reads_mapped_sorted.bam
```

Deduplication → Removal of reads from duplicated fragments:

```bash
samtools rmdup -s reads_mapped_sorted.bam reads_mapped_sorted_dedup.bam
```

```bash
samtools index reads_mapped_sorted_dedup.bam
```

Duplicated reads are usually a consequence of amplification of the DNA fragments in the lab. Therefore, they are not biologically meaningful.

We have now completed the mapping procedure.
Let's have a look at our mapping results:

```bash
samtools view reads_mapped_sorted_dedup.bam | less -S
```

(exit by pressing <kbd>q</kbd>)

We can also get a summary about the number of mapped reads. For this we use the _samtools idxstats_ command ([http://www.htslib.org/doc/samtools-idxstats.html](http://www.htslib.org/doc/samtools-idxstats.html)):

```bash
samtools idxstats reads_mapped_sorted_dedup.bam
```

##### Genotyping

The next step we need to perform is genotyping, i.e. the identification of all SNPs that differentiate the sample from the reference.
For this we use the _Genome Analysis Toolkit (GATK)_ (DePristo et al. 2011 – [http://www.broadinstitute.org/gatk/](http://www.broadinstitute.org/gatk/))

It uses the reference genome and the mapping as input and produces an output in _Variant Call Format (VCF)_ ([https://en.wikipedia.org/wiki/Variant_Call_Format](https://en.wikipedia.org/wiki/Variant_Call_Format)).

Perform genotyping on the mapping file:

```bash
gatk3 -T UnifiedGenotyper -R ../YpestisCO92.fa -I reads_mapped_sorted_dedup.bam --output_mode EMIT_ALL_SITES -o mysnps.vcf
```

Let’s have a look…

```bash
cat mysnps.vcf | less -S
```

(exit by pressing <kbd>q</kbd>)

##### Mapping and Genotyping for the other Samples/Parameters

Let's now continue with mapping and genotyping for the other samples and parameter settings.

###### Sample2 Lenient

```bash
cd ..
cd sample2_lenient

bwa aln -n 0.01 -l 16 ../YpestisCO92.fa ../sample2.fastq.gz > reads_file.sai

bwa samse -r '@RG\tID:all\tLB:NA\tPL:illumina\tPU:NA\tSM:NA' ../YpestisCO92.fa reads_file.sai ../sample2.fastq.gz > reads_mapped.sam

samtools view -b -S reads_mapped.sam > reads_mapped.bam

samtools sort reads_mapped.bam > reads_mapped_sorted.bam

samtools index reads_mapped_sorted.bam

samtools rmdup -s reads_mapped_sorted.bam reads_mapped_sorted_dedup.bam

samtools index reads_mapped_sorted_dedup.bam

gatk3 -T UnifiedGenotyper -R ../YpestisCO92.fa -I reads_mapped_sorted_dedup.bam --output_mode EMIT_ALL_SITES -o mysnps.vcf
```

###### Sample1 Strict

```bash
cd ..
cd sample1_strict

bwa aln -n 0.1 -l 32 ../YpestisCO92.fa ../sample1.fastq.gz > reads_file.sai

bwa samse -r '@RG\tID:all\tLB:NA\tPL:illumina\tPU:NA\tSM:NA' ../YpestisCO92.fa reads_file.sai ../sample1.fastq.gz > reads_mapped.sam

samtools view -b -S reads_mapped.sam > reads_mapped.bam

samtools sort reads_mapped.bam > reads_mapped_sorted.bam

samtools index reads_mapped_sorted.bam

samtools rmdup -s reads_mapped_sorted.bam reads_mapped_sorted_dedup.bam

samtools index reads_mapped_sorted_dedup.bam

gatk3 -T UnifiedGenotyper -R ../YpestisCO92.fa -I reads_mapped_sorted_dedup.bam --output_mode EMIT_ALL_SITES -o mysnps.vcf
```

###### Sample2 Strict

```bash
cd ..
cd sample2_strict

bwa aln -n 0.1 -l 32 ../YpestisCO92.fa ../sample2.fastq.gz > reads_file.sai

bwa samse -r '@RG\tID:all\tLB:NA\tPL:illumina\tPU:NA\tSM:NA' ../YpestisCO92.fa reads_file.sai ../sample2.fastq.gz > reads_mapped.sam

samtools view -b -S reads_mapped.sam > reads_mapped.bam

samtools sort reads_mapped.bam > reads_mapped_sorted.bam

samtools index reads_mapped_sorted.bam

samtools rmdup -s reads_mapped_sorted.bam reads_mapped_sorted_dedup.bam

samtools index reads_mapped_sorted_dedup.bam

gatk3 -T UnifiedGenotyper -R ../YpestisCO92.fa -I reads_mapped_sorted_dedup.bam --output_mode EMIT_ALL_SITES -o mysnps.vcf
```

##### Comparing Genotypes

In order to combine the results from multiple samples and parameter settings we need to agregate and comparatively analyse the information from all the _vcf_ files.
For this we will use the software
_MultiVCFAnalyzer_ ([https://github.com/alexherbig/MultiVCFAnalyzer](https://github.com/alexherbig/MultiVCFAnalyzer)).

It produces various output files and summary statistics and can integrate gene annotations for SNP effect analysis as done by the program _SnpEff_ (Cingolani et al. 2012 - [http://snpeff.sourceforge.net/](http://snpeff.sourceforge.net/)).

Run _MultiVCFAnalyzer_ on all 4 files at once.
First `cd` one level up (if you type `ls` you should see your 4 directories, reference, etc.):

```bash
cd ..
```

Then make a new directory…

```bash
mkdir vcf_out
```

…and run the programme:

```bash
multivcfanalyzer NA YpestisCO92.fa NA vcf_out F 30 3 0.9 0.9 NA sample1_lenient/mysnps.vcf sample1_strict/mysnps.vcf sample2_lenient/mysnps.vcf sample2_strict/mysnps.vcf
```

Let’s have a look in the ‘vcf_out’ directory (`cd` into it):

```bash
cd vcf_out
```

Check the parameters we set earlier:

```bash
less -S info.txt
```

(exit by pressing <kbd>q</kbd>)

Check results:

```bash
less -S snpStatistics.tsv
```

(exit by pressing <kbd>q</kbd>)

The file content should look like this:

```bash
SNP statistics for 4 samples.
Quality Threshold: 30.0
Coverage Threshold: 3
Minimum SNP allele frequency: 0.9
sample	SNP Calls (all)	SNP Calls (het)	coverage(fold)	coverage(percent)
refCall	allPos	noCall	discardedRefCall	discardedVarCall	filteredVarCall	unhandledGenotype
sample1_lenient	213	0	16.38	92.69
4313387	4653728	293297	46103	728	0	0
sample1_strict	207	0	16.33	92.71
4314060	4653728	293403	45633	425	0	0
sample2_lenient	1274	0	9.01	83.69
3893600	4653728	453550	297471	7829	0	4
sample2_strict	1218	0	8.94	83.76
3896970	4653728	455450	295275	4815	0	0
```

First we find the most important parameter settings and then the table of results.
The first column contains the dataset name and the second column the number of called SNPs. The genome coverage and the fraction of the genome covered with the used threshold can be found in columns 4 and 5, respectively. For example, sample1 had 207 SNP calls with strict parameters. The coverage is about 16-fold and about 93% of the genome are covered 3 fold or higher (The coverage threshold we set was 3).

##### Exploring the Results

For visual exploration of mapping results so-called "Genome Browsers" are used.
Here we will use the _Integrative Genomics Viewer (IGV)_ ([https://software.broadinstitute.org/software/igv/](https://software.broadinstitute.org/software/igv/)).

To open IGV, simply type the following command and the app will open:

```bash
igv
```

Note that you cannot use the terminal while IGV is open. If you want to use it anyways, open a second terminal via the bar on the bottom.

Load your reference (`YpestisCO92.fa`):

_→ Genomes → Load Genome from File_

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_load_genome.png" width=400>

Load your _bam_ files (do this 4 times, once for each mapping):

_→ File → Load from File_

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_load_bam.png" width=200>

Try to explore the mapping results yourself. Here are some questions to guide you. Please also have a look at the examples below.

What differences do you observe between the samples and parameters?

Differences in number of mapped reads, coverage, number of SNPs

Do you see any global patterns?

Which sample is more affected by changing the parameters?

Which of the two samples might be ancient, which is modern?

Let’s examine some SNPs.
Have a look at `snpTable.tsv`.

Can you identify SNPs that were called with lenient but not with strict parameters or vice versa?

Let’s check out some of these in IGV.
Do you observe certain patterns in these genomic regions?

##### Examples

Please find here a few examples for exploration. To get a better visualization we have loaded here only `sample2_lenient` (top track) and `sample2_strict` (bottom track):

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_example_intro.png">

You can see all aligned reads in the current genomic region as stacks of grey arrows. In the middle of the image you see brown dashes in all of the reads. This is a SNP.
You also see sporadically green or red dashes in some reads but not all of them at a given position. These sporadic differences are DNA damage such as we typically find it for ancient DNA.

For jumping to a specific coordinate you need to enter it into the coordinate field at the top:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_coordinate_example.png">

E.g. if you enter `12326942` after the colon in the coordinate field and hit enter, you will jump to the same position as in the screenshot above.

Let's have a look at some positions.

For example position `36472`:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_SNP_36472.png">

In the middle of the image you see a SNP (`T`) that was called with strict parameters (bottom) but not with lenient parameters (top). But why would it not be called in the top track? It is not called because there are three reads that cover the same position, but do not contain the `T`. We can see that these reads have other difference to the reference at other positions. That's why they are not mapped with strict parameters. It is quite likely that they originate from a different species. This example demonstrates that sensitive mapping parameters might actually lead to a loss of certain SNP calls.

Does this mean that stricter parameters will always give us a clean mapping? Let's have a look at position `219200`:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_SNP_219200.png">

You might need to zoom out a bit using the slider in the upper right corner.

So, what is going on here? We see a lot of variation in most of the reads. This is reduced a bit with strict mapping parameters (bottom track) but the effect is still quite pronounced. Here, we see a region that seems to be conserved in other species as well, so we have a lot of mapping from other organisms. We can't compensate that with stricter mapping parameters and we would have to apply some filtering on genotype level to remove this variation from our genotyping. Removing false positive SNP calls is important as it would interfere with downstream analysis such as phylogenomics.

Such regions can be fairly large. For example, see this 20 kb region around position `224750`:

<img src="https://github.com/SPAAM-community/wss-summer-school/raw/main/docs/assets/slides/2022/4b-intro-to-mapping/IGV_SNP_224750.png">

##### Conclusions

- Mapping DNA sequencing reads to a reference genome is a complex procedure that requires multiple steps.
- Mapping results are the basis for genotyping, i.e. the detection of differences to the reference.
- The genotyping results can be aggregated from multiple samples and comparatively analysed e.g. in the context of phylogenomics.
- The chosen mapping parameters can have a strong influence on the results of any downstream analysis.
- This is particularly true when dealing with ancient DNA samples as they tend to contain DNA from multiple organisms. This can lead to mismapped reads and therefore incorrect genotypes, which can further influence downstream analyses.

</details>

</div>

---

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
