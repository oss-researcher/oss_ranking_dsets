# README.md

This code takes approx. 8 seconds to execute.

## Overview

This project implements a **multi-criteria ranking framework using fuzzy d-sets** to evaluate and rank open source software products based on bug-related attributes across multiple temporal windows.

The workflow includes:
- Data preprocessing and aggregation  
- Temporal window construction and the aggregated overall baseline (R1–R6 and R_star)  
- Min–max normalization  
- d-set computation  
- Ranking generation  
- Rank comparison using Spearman and Kendall correlations  
- Execution time tracking  

---

## Important Notes

---

### 1. `View()` is Disabled

- All `View()` calls are **disabled in the first code block** of the script.
- This ensures smooth, non-interactive execution and reproducibility.
- To enable for debugging, toggle the first block manually.

---

### 2. Data Placement

All input CSV files must be placed in:

../data/

Ensure:
- File names match those used in the script
- Data structure is consistent for fields under study (Product,Status,Resolution,Updated)

---

### 3. Output Directory

All generated outputs (final and intermediate) are written to:

../output/

Directory gets created if doesn't exist and files get overwritten if exist.

---

## File Structure

### Intermediate Files

These files are either generated during preprocessing to verify the steps :

- bimonthly_all.csv: Baseline aggregated dataset (bi-monthly) used for R_star  
- half_monthly.csv: Main dataset split into half-month temporal windows  
- half_month_data.csv: Preprocessed half-month dataset used for window calculations  

---

### d-set Computation Outputs

- R1_calc.csv: d-set results for temporal window R1  
- R2_calc.csv: d-set results for temporal window R2  
- R3_calc.csv: d-set results for temporal window R3  
- R4_calc.csv: d-set results for temporal window R4  
- R5_calc.csv: d-set results for temporal window R5  
- R6_calc.csv: d-set results for temporal window R6  
- R_star_calc.csv: Baseline d-set results using bi-monthly data (results can be compared with excel calculations given in ../excel/) 

---

### Ranking & Comparison Outputs

- rank_compare.csv: Consolidated ranking comparison across R1–R6 and R_star  
- rank_correlations.csv: Pairwise Spearman and Kendall correlations with p-values  

---

## Execution Time Tracking

The script measures execution time using:

- start_time at the beginning  
- end_time at the end  
- Total execution time reported in seconds  

---

## Required R Packages

Install required packages:

install.packages(c(
  "dplyr",
  "tidyr",
  "purrr",
  "janitor",
  "lubridate"
))

---

## Execution Instructions

### Clean Run (Recommended)

rm(list = ls())
gc()
source("OSS_ranking_dset.Rmd")

---

## Workflow Summary

1. Load and clean dataset  
2. Generate half-month and bi-monthly datasets  
3. Construct temporal windows (R1–R6, R_star)  
4. Apply normalization  
5. Compute d-set scores  
6. Generate rankings  
7. Compare rankings  
8. Export results  

---

## Reproducibility Guidelines

- Always start with a clean environment  
- Keep input data unchanged  
- Avoid manual edits to intermediate files  
- Ensure consistent file paths  
- Keep View() disabled during final runs  

---

## Common Issues

- File not found → Missing CSV in ../data/  

---

## Notes on Intermediate Files

Intermediate files (e.g., half_month_data.csv, half_monthly.csv):

- Support traceability  
- Enable validation of preprocessing steps  
- Help debug temporal window construction  

Do not manually modify these files.

---

## Rendered HTML Report

The file `OSS_ranking_dset.html` is the knitted HTML output generated from `OSS_ranking_dset.Rmd`.

- It contains the complete rendered analysis, including methodology, intermediate results, tables, and final rankings.
- It is provided for direct viewing without requiring code execution.

To regenerate the HTML report:

```r
rmarkdown::render("OSS_ranking_dset.Rmd", output_format = "html_document")
```

----

## Summary

This repository provides a fully reproducible pipeline for dependency-aware, multi-criteria ranking using fuzzy d-sets across temporal windows, with clear intermediate outputs and validation through rank correlations.
