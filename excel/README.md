# Excel Files Description

This folder contains spreadsheet-based calculations supporting the analysis, validation, and robustness assessment of the proposed d-set ranking framework.

## Files Included

1. **1. Bi-monthly d-set calculations.xlsx**
   - Contains the primary computations for generating product rankings based on bi-monthly aggregated data.
   - Includes intermediate steps for IVIF parameter construction, aggregation, and final ranking.

2. **2. Perturbation 5.xlsx**
   - Implements a 5% perturbation to input parameters.
   - Used to assess sensitivity of ranking outcomes under minor variations.

3. **3. Perturbation 10.xlsx**
   - Implements a 10% perturbation to input parameters.
   - Evaluates ranking stability under moderate variations.

4. **4. Perturbation 15.xlsx**
   - Implements a 15% perturbation to input parameters.
   - Assesses robustness under relatively larger deviations.

5. **5. Rank Comparison.xlsx**
   - Computes Spearman’s rank correlation coefficient and Kendall’s tau.
   - Compares rankings from:
     - Bi-monthly baseline results
     - Perturbation scenarios (5%, 10%, 15%)
   - Used to evaluate consistency and robustness of the ranking framework.

## Purpose

These Excel files are used to:
- Generate baseline rankings using the proposed d-set methodology  
- Conduct perturbation-based sensitivity analysis  
- Evaluate ranking stability using correlation measures  
- Provide transparency for intermediate and validation computations  

## Usage

- Start with **1. Bi-monthly d-set calculations.xlsx** to obtain baseline rankings  
- Use **2–4. Perturbation files** to observe the effect of controlled variations  
- Use **5. Rank Comparison.xlsx** to evaluate agreement between baseline and perturbed rankings  

## Notes

- These spreadsheets complement the main analysis and are provided for transparency and reproducibility.  
- All computations align with the methodology described in the manuscript.  
- No identifying information is included to maintain compliance with double-blind review requirements.