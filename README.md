# Whole-Genome Sequencing Analysis of *Mycobacterium tuberculosis* H37Rv

> Genome-wide Variant Identification and Functional Annotation using a Reference-Based WGS Pipeline

![Poster](poster/WGS_Mtb_Poster.png)

---

## Overview

This mini project demonstrates a complete **Whole-Genome Sequencing (WGS) variant analysis workflow** for *Mycobacterium tuberculosis* H37Rv using publicly available genomic data. The analysis focuses on identifying genomic variants, annotating their functional consequences, and exploring mutations associated with antimicrobial resistance (AMR).

This project was developed as part of my **Bioinformatics Learning Portfolio** to practice bacterial genome analysis using commonly adopted open-source tools.

---

## Project Objectives

The objectives of this project were to:

- Perform quality assessment and filtering of sequencing reads.
- Align sequencing reads to the *M. tuberculosis* H37Rv reference genome.
- Detect genomic variants (SNPs and InDels).
- Annotate variants using SnpEff.
- Investigate coding and non-coding mutations.
- Identify variants located in antimicrobial resistance-associated genes.
- Summarize the biological significance of the detected variants.

---

## Workflow

```text
Raw FASTQ
      │
      ▼
Quality Control (FastQC)
      │
      ▼
Read Filtering (fastp)
      │
      ▼
Reference Alignment (BWA-MEM)
      │
      ▼
SAM/BAM Processing (SAMtools)
      │
      ▼
Variant Calling (FreeBayes)
      │
      ▼
Variant Annotation (SnpEff)
      │
      ▼
Biological Interpretation
```

---

# Tools Used

| Step | Software |
|------|----------|
| Quality Control | FastQC |
| Read Filtering | fastp |
| Alignment | BWA-MEM |
| BAM Processing | SAMtools |
| Variant Calling | FreeBayes |
| Variant Annotation | SnpEff |

---

# Dataset

| Item | Description |
|------|-------------|
| Organism | *Mycobacterium tuberculosis* H37Rv |
| Data Type | Whole Genome Sequencing (WGS) |
| Reference Genome | H37Rv |
| Annotation | SnpEff |
| Variant File | Annotated Variant File |

---

# Results Summary

The analysis identified:

- **1,147 annotated genomic variants**
- Coding and non-coding mutations
- Missense, synonymous, upstream/downstream, frameshift and stop-gained variants
- Multiple mutations in genes associated with antimicrobial resistance

Representative resistance-associated genes include:

- **rpoB**
- **katG**
- **embB**
- **pncA**
- **rpsL**
- **gyrA**

Representative coding variants include:

| Gene | Protein Change |
|------|----------------|
| recF | p.Ile245Thr |
| gyrA | p.Glu21Gln |
| gyrA | p.Ser95Thr |
| gyrA | p.Gly668Asp |

---

# Biological Interpretation

The genomic profile suggests:

- Genome-wide variation is dominated by SNPs.
- Missense mutations are the predominant coding variant class.
- Mutations were detected in several clinically important antimicrobial resistance genes.
- The detected mutation profile is consistent with a **probable multidrug-resistant tuberculosis (MDR-TB)** isolate.
- WGS provides valuable information for molecular characterization and resistance prediction.

---

# Key Findings

- 1,147 annotated genomic variants detected.
- SNPs were the dominant mutation type.
- Missense substitutions represented the major coding-region variants.
- Variants were identified in major resistance-associated genes (*rpoB, katG, embB, pncA, rpsL,* and *gyrA*).
- WGS successfully characterized genome-wide variation in *M. tuberculosis*.

---

# Limitations

- Genomic predictions do not replace phenotypic Drug Susceptibility Testing (DST).
- Not every detected mutation necessarily alters phenotype.
- Functional validation is required for novel variants.
- Clinical interpretation should integrate genomic, laboratory, and epidemiological evidence.

---

# Future Work

- Perform lineage analysis.
- Conduct phylogenetic comparison with global isolates.
- Integrate AMR prediction tools (TB-Profiler, Mykrobe).
- Compare WGS predictions with phenotypic DST.
- Explore structural variants and pan-genome analysis.

---

# Author

**Asma Mujahidah**

Bioinformatics Learning Portfolio

June 2026

---

# References

1. World Health Organization. *Global Tuberculosis Report 2024*. WHO, Geneva.

2. Walker TM, Kohl TA, Omar SV, et al. Whole-genome sequencing for prediction of *Mycobacterium tuberculosis* drug susceptibility and resistance. *Lancet Infectious Diseases*. 2015;15(10):1193–1202.

3. Coll F, McNerney R, Guerra-Assunção JA, et al. A robust SNP barcode for typing *Mycobacterium tuberculosis* complex strains. *Nature Communications*. 2014;5:4812.

4. Cingolani P, Platts A, Wang LL, et al. A program for annotating and predicting the effects of single nucleotide polymorphisms, SnpEff. *Fly*. 2012;6(2):80–92.

5. Li H. Aligning sequence reads with BWA-MEM. arXiv:1303.3997.

6. Danecek P, Bonfield JK, Liddle J, et al. Twelve years of SAMtools and BCFtools. *GigaScience*. 2021;10(2):giab008.

7. Garrison E, Marth G. Haplotype-based variant detection from short-read sequencing. FreeBayes. arXiv:1207.3907.

---

## License

This project is intended for **educational and portfolio purposes only**.
The biological interpretation presented here should **not** be considered clinical or diagnostic evidence without additional laboratory validation.
