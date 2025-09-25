# phage-genomics-pipelines
Protocols and step-by-step guides for genome sequencing analysis, including quality control, assembly, annotation, and downstream analysis.
# Bacteriophage Genome Sequencing and Analysis Protocol

This repository contains step-by-step protocols for sequencing, assembling, and analyzing bacteriophage genomes. The example below describes the workflow used for one of our phage projects.

---

## 1. Sequencing

**Platform:** Illumina MiSeq  
**Mode:** Paired-end (301 bp × 2)  
**Provider:** Hokkaido System Science Co., Ltd., Hokkaido, Japan  
**Raw Data Accession Number:** [PRJNA1101219](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1101219)

---

## 2. Genome Assembly

**Tool:** SPAdes (version 3.11)  
**Method:** De novo assembly  
**Coverage:** Average 153×  

```bash
spades.py -1 sample_R1.fastq -2 sample_R2.fastq -o spades_output

---

## 3. Gene Prediction

Tool: RASTtk web server
URL: https://rast.nmpdr.org/

Accessed: 1 December 2022

Open reading frames (ORFs) were determined using RASTtk.

---

## 4. Functional Annotation

Tools:

BLASTP (Protein Basic Local Alignment Search Tool)

HHPred Web Server (https://toolkit.tuebingen.mpg.de
)
Accessed: 23 December 2022

The functions of ORFs were annotated by comparison with known protein databases.
