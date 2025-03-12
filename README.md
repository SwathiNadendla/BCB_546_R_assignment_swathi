SNP Genotype Data Processing and Visualization

Overview

This project involves the inspection, processing, and visualization of SNP genotype data from maize and teosinte samples. The workflow includes data extraction, transformation, filtering, sorting, and visualization.

Requirements

The script requires the following R packages:

readr

dplyr

tidyr

ggplot2

stringr

Ensure these packages are installed before running the script.

Input Files

fang_et_al_genotypes.txt: Contains genotype information.

snp_position.txt: Contains SNP position details.


always check working directory or set it properly where the files are actually located 

Workflow

Part 1: Data Inspection & Processing

Read Input Files:

Genotype and SNP position files are read into R.

Converted to CSV format for easier inspection.

I have converted them to CSV for easier visualisation by importing the tables whether it has all necessary columns or sorting is done properly or not 

Extract Relevant Columns:

Only SNP_ID, Chromosome, and Position are retained from the SNP position file.


Separate Maize and Teosinte Data:

Groups maize and teosinte samples based on predefined group identifiers.

Process and Transpose Data:

Filters and transposes genotype data for each group.

Merges with SNP position information.

Identify Unknown and Multiple Matches:

Extracts and saves SNPs with unknown or multiple chromosome assignments.

Sort and Save Chromosome Data:

Data is sorted in ascending and descending order for each chromosome.

Replaces missing data (?/?) with -/- and saves an edited version.

Part 2: Data Visualization

Convert Position to Numeric & Filter Invalid Entries:

Excludes multiple, unknown, and NA chromosomes.

Combine Genotype and Position Data:

Reshapes genotype data into long format and joins with SNP positions.

Classify Genotype Types:

Categorizes SNPs into Homozygous, Heterozygous, and Missing.

Generate Visualizations:

Genotype Frequency Distribution:

Stacked bar plot showing proportions of different genotype types across groups.

SNP Position Boxplot:

Displays SNP position distributions across chromosomes.

SNP Density Plots:

Faceted density plots showing SNP distributions per chromosome.

Per-Sample Summary Statistics:

Bar plot showing proportions of homozygous, heterozygous, and missing sites per sample.

Output Files

Processed SNP data (joined_maize_snp.csv, joined_teosinte_snp.csv, etc.).

Sorted SNP files per chromosome (maize_chr1_asc.csv, maize_chr1_desc.csv, etc. till 10 same for teosinte).

Edited versions of descending sorted files with missing values replaced (edited_maize_chr1_desc.csv, etc.).

Visualization plots.

Usage

Run the script in R after ensuring the required files are in the working directory. Modify file paths as needed before execution

I was able to run the entire script again through the code Provided without any errors and generated plots 

For any issues or questions, feel free to reach out
swathi79@iastate.edu


