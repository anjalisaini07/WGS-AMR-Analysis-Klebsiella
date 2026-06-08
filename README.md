# WGS-AMR-Analysis-Klebsiella
Comparative whole genome sequencing and antimicrobial resistance profiling of carbapenem-resistant *Klebsiella pneumoniae* isolates using Galaxy-based bioinformatics workflows including FastQC, Trimmomatic, BWA-MEM2, FreeBayes, BCFtools, and ABRicate for variant analysis and resistome characterization.

## Project Overview

This project focuses on comparative population genomics and antimicrobial resistance (AMR) profiling of carbapenem-resistant *Klebsiella pneumoniae* isolates from India, Turkey, and the United States using whole genome sequencing (WGS) and bioinformatics analysis on the Galaxy platform.

The study combined:

* A complete WGS analysis workflow for the Indian isolate using raw paired-end Illumina sequencing reads
* Comparative antimicrobial resistance profiling of assembled genomes from Turkey and the USA using ABRicate and the ResFinder database

All analyses were performed using the Galaxy platform with reproducible workflow tracking and history retention.

---

## Workflow Diagram

---

## Tools and Technologies

* Galaxy Platform
* FastQC
* Trimmomatic
* BWA-MEM2
* SAMtools
* FreeBayes
* BCFtools
* ABRicate

---

## Dataset Information

### Indian Isolate

* *Klebsiella pneumoniae* ATCC BAA-2146
* Raw paired-end reads:

  * IndiaR1.gz
  * IndiaR2.gz
* Source: NCBI SRA

### Reference Genome

* *Klebsiella pneumoniae* MGH 78578
* Used for BWA-MEM2 alignment and variant calling

### Turkish Isolate

* turkey_GCF_000240185.1_ASM24018v2_genomic.fna
* Used for comparative AMR profiling

### U.S. Isolate

* usa_GCF_000597905.1_ASM59790v1_genomic.fna
* Used for comparative AMR profiling

---

## Workflow Summary
```markdown
![WGS Workflow](workflow/wgs_workflow_diagram.png)
```


### Indian Isolate WGS Workflow

1. Raw read quality assessment using FastQC
2. Adapter trimming using Trimmomatic
3. Alignment to reference genome using BWA-MEM2
4. BAM sorting using SAMtools
5. Variant calling using FreeBayes
6. Variant statistics generation using BCFtools

### Comparative AMR Profiling

7. AMR gene detection using ABRicate with the ResFinder database

---

## Key Results

### Quality Control Results

* Raw reads:

  * 3,016,254 paired-end sequences
  * 301 bp read length
  * ~907.8 Mbp total bases

* Post-trimming:

  * 2,981,740 retained sequences
  * Improved sequence quality
  * Adapter contamination removed

---

## Variant Statistics (India Isolate)

| Variant Type   | Count  |
| -------------- | ------ |
| Total Variants | 30,261 |
| SNPs           | 25,955 |
| MNPs           | 3,852  |
| Indels         | 358    |
| Other Variants | 142    |

---

## Comparative Resistome Analysis

| Isolate | Major Carbapenemase | Total Resistance Genes | Resistome Complexity |
| ------- | ------------------- | ---------------------- | -------------------- |
| India   | blaNDM-1            | 23                     | Very High (MDR)      |
| Turkey  | blaKPC-2            | 17                     | High (MDR)           |
| USA     | blaKPC-3            | 6                      | Moderate             |

Shared resistance gene detected in all isolates:

* fosA6

---

## AMR Profiling Results

### India Isolate

### Turkey Isolate

### USA Isolate

---

## Biological Significance

This study demonstrates the application of whole genome sequencing and comparative genomics in:

* Detection of antimicrobial resistance genes
* Variant analysis
* Comparative resistome profiling
* Genomic surveillance of multidrug-resistant bacterial pathogens

The results highlight geographic variation in carbapenem resistance mechanisms among global *Klebsiella pneumoniae* isolates.

---

## Project Structure

```text
Project/
├── README.md
├── workflow/
├── results/
└── reports/
```

---

## Future Scope

* Functional annotation using SnpEff
* MLST sequence typing
* Plasmid analysis
* Phylogenomic analysis
* Integration with phenotypic resistance data

---

## Author

Anjali Saini
M.Sc. Bioinformatics
Maharshi Dayanand University, Rohtak
