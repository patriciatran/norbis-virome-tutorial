# Viral Omics Tutorial

**Contact**: Patricia Tran :school: University of Wisconsin-Madison :email: ptran5@wisc.edu

If you have questions about this tutorial please contact Patricia. If you have questions about the technicalities of VIBRANT, bugs, suggestions for the program itself, etc. please contact Kris Kieft (kieft@wisc.edu) 

:star: **Welcome to the tutorial page for the Viral omics bioinformatics session of the [NORBIS Summer School 2021](https://norbis.w.uib.no/activities/summerschool/)!** :star:

## Learning Outcomes:
After completion of the NORBIS summer school, the participants will:

- Improved knowledge of biological background of NORBIS related fields.
- Knowledge about data types and methods for bioinformatic analysis in NORBIS related fields.

After completion of this virome workshop day the participants will:
- Have a better idea of what can they achieve using VIBRANT in their research
- Grasp a understanding that VIBRANT is one tool of of a rich ecosystem of tools that can be used to expand virome research
- Be able to discuss the use of bioinformatics tools for virome research, either in their field of study or generally in science.

## Before we start! ##
During this interactive tutorial, please use these icons at the lower right portion of your Zoom screen in order to let me know whether things are going well, yes (green icon), no (red icon), notify me to slow down (grey icon) or speed up (blue icon). Additionally, please feel free to post your questions in the chat and one of my colleagues will be available to answer questions in the chat as well.

<img src="https://github.com/patriciatran/norbis-virome-tutorial/blob/main/ZoomIcons.png" width=30% height=30%>


## Prerequisites
A basic knowledge of the command line will be beneficials, and knowledge of commands such as `cd`, `ls`, `mkdir`, `mv`, `cp`, `head`, `tail`, as well as an understanding of file directory structure will be beneficial. 

If you'd like to brush up on those skills, I recommand this free tutorial from [DataCarpentry: Introduction to the Command line for Genomics](https://datacarpentry.org/shell-genomics/) prior to the day of the workshop.

## Installation
To follow along this tutorial, you will need to install [VIBRANT] `v.1.2.1` (https://github.com/AnantharamanLab/VIBRANT), which is freely available at the link here. Detailed instructions on installing VIBRANT are found on its own github page, posted [here](https://github.com/AnantharamanLab/VIBRANT#requirements-).

The program VIBRANT has already been installed on the server for this summer school.
You can access it by

[TBA]

## File descriptions & Flow of the tutorial

For this tutorial, we will use a total of 3 scenarios. First, I will walk you through how to use VIBRANT using the command line through a live coding session. Additionally, we will go over the general input and output files. We will then compare how the outputs differ in the 3 scenarios, and then discuss these through guided discussions in breakout groups of 7-8 students per grouup. Finally, we will regroup in the main virtual room to debrief. 



### File descriptions in the `Datasets` Folder:

In the folder `Datasets` of this github page, you will find 5 fasta files with the file extension `.fasta.`, `.faa`, `fna`. the README.txt file in the `datasets` folder describes what these datasets are. 

:dna: Lactococcus lactis: Complete bacterial genome with 5 prophages

:dna: LBVG: Lake Biwa Viral Genomes, curated viruses from a metagenome

:dna: Microviridae: Example of running proteins, single genome

:dna: mixed_example: Some short scaffolds, some non-viruses, some viruses

:dna: Podoviridae: Example of running nucleotides, single genome, encodes an AMG

As you can see, each of these 5 examples constitute a slightly different situation where VIBRANT can be used. 

For the live-demonstration, I will show you how to run it on `Lactococcus_lactis.fasta` but please change the `input file` name for the file that you are assigned, as you follow along. We will beginby splitting the group, and each group will be assigned one of these 4 files. Each person in each group can follow along and run VIBRANT on their respective sequence. 

Later in the defriefing section, each group will go through their output files and discuss them with one of the instructors . Then we will regroup and share our points as a class and answer any additional questions you may have.

## Option 1: Running VIBRANT from command-line.
### Exercises and discussion questions

### Discussion questions & things to keep in mind as you go through the 3 scenarios

#### Live demonstration
For the live demo, we will use `Lactococcus_lactis.fasta`, which is the genome of Lactococcus lactis. We will use VIBRANT to identify phages in this one genome. The genome has XX mbp and contains XX contigs.

```
/slowdata/data4/VIBRANT/VIBRANT_v1.2.1/VIBRANT_run.py -i Lactococcus_lactis.fasta -t 2 -folder Lactococcus_lactis.fasta_vibrant_folder
```

where:

`-i` is the input file, a nucleotide or amino acid file in `fasta` format

`-t` is the number of threads, this you can edit depending on your machine

`-folder` is the name of the output folder where you want your results to be created.

To view more options that `VIBRANT` has, type `VIBRANT_run.py -h`.


## Option 2: Running VIBRANT on Cyverse
If for whatever reason you prefer to run the analysis using the cloud, Cyverse is a good option. The most updated version is 1.2.0, which is compared to the newest version 1.2.1. You can read about the difference between the two versions [here](https://github.com/AnantharamanLab/VIBRANT#updates-for-v121-mar-13-2020-). 

1. Create a Cyverse Account
2. From the home page, under My Services, click "Launch" on the Discovery environment tab.
3. Click Launch again.
4. On the left hand side bar, click on "Apps". It looks like a grid.
5. In the search bar, type "VIBRANT". There will be version `1.0.1` and `1.2.0`. Select `1.2.0`.
6. In the Analysis Info, type "NORBIS Tutorial Scenario 1", click next.
7. Use the drop down menu to input the first fasta file from Scenario 1. 
8. For the parameters, choose "nucleotide", 4 parralell runs, and keep the base pair and ORF as default (1000 and 4 respectively). Do not select "virome". Click next.
9. Keep the Advanced settings as default. Click Next.
10. On the "review and launch" tab, you can click "Launch Analysis". If you want to do this in advance but not run it now, click on "Save as Quick Launch".
11. Repeat step 6 to 10 for Scenario 2 and 3. Don't forget to rename the analysis to "NORBIS Tutorial Scenario 2" and "NORBIS Tutorial Scenario 3" instead.
12. To view your results, on the left-hand side bar, click on the second icon "Data". Under the folder "Analysis" will be your result files. 

## Debriefing

## Additional resources & Further Readings
### Other tools in virome research
CheckV: [Paper](https://www.nature.com/articles/s41587-020-00774-7) and [Tool](https://bitbucket.org/berkeleylab/CheckV)

VirSorter: [Paper](https://peerj.com/articles/985/) and [Tool](https://github.com/simroux/VirSorter)

### Examples of litterature citing VIBRANT

https://www.sciencedirect.com/science/article/pii/S193131282030456X

https://www.nature.com/articles/s41467-021-23698-5

https://www.sciencedirect.com/science/article/pii/S1931312821001487


### Applications of VIBRANT 
