## Project 7: VCF Variant Extraction and PRS Analysis

Project Overview

This project focuses on analyzing genomic data to extract variants and compute Polygenic Risk Scores (PRS) using bcftools and PLINK2. The analysis highlights African population samples from chromosome-level data files, processes relevant variants, and visualizes PRS distributions.

Table of Contents

Commands Overview
Workflow Summary
Tools and Software
Data Files
PRS Computation
Visualization Outputs
1. Commands Overview

Key Tasks
Extract First 10 Variant IDs:
Filter chromosome 15 data to display the first 10 variant IDs.
Count Unique Samples:
Query and count distinct sample IDs from the VCF file.
Retrieve Total Number of Variants:
Compute the total number of records (variants) for chromosome 12.
2. Workflow Summary

The following steps summarize the workflow:

Variant Extraction:
Extract African-specific samples for chromosomes 1–22.
Save filtered VCF files.
Unique Sample Identification:
Process all VCF files to identify unique African samples.
PRS Analysis:
Download the PGS score table.
Extract rsID for relevant variants.
Filter overlapping variants between the PGS table and VCF data.
PRS Calculation:
Convert filtered VCF files to PLINK2 format.
Calculate PRS for all chromosomes.
Population Merging:
Merge PRS results with population metadata.
Filter data for African populations.
Visualization:
Generate density plots, boxplots, and violin plots for scaled PRS scores.
3. Tools and Software

bcftools: For VCF file filtering and querying.
PLINK2: For PRS calculations and genetic data processing.
Python Libraries:
pandas for data manipulation.
matplotlib and seaborn for data visualization.
subprocess for running system commands.
4. Data Files

Input Files:
VCF Files: Chromosome-level VCF files located at /storage/ice-shared/biol6150/Data/1000Genomes/.
PGS Table: PGS004696 Harmonized data for GRCh38 genome build.
Population File: kgp3_id_pop.tsv containing sample population metadata.
Output Files:
Filtered African-specific VCFs (1–22).
PRS results (per chromosome and combined).
Merged PRS results with population information.
Visualizations of PRS scores.
5. PRS Computation

Convert filtered VCF files to PLINK2 format.
Use extracted rsID and effect allele weights to compute PRS.
Scale PRS scores for consistency across chromosomes.
6. Visualization Outputs

Density Plots: Show the distribution of scaled PRS scores for African populations.
Violin Plots: Compare PRS distributions across African population groups.
Boxplots: Visualize chromosome-level variations in PRS.
Notes

The PGS file PGS004696 was selected due to its focus on coronary artery disease and relevance to African populations.
Software versions:
bcftools: 1.15 or later
plink2: Latest release
Python: 3.11 or later
References

PGS Catalog:
Score: PGS004696
Publication: PGP000602
