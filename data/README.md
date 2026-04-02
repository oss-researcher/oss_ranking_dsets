# Data Description

This folder contains the dataset used for evaluating and ranking open-source software (OSS) products based on maintenance performance.

## File Included
- `01-09-2023 to 31-08-2024.csv`

## Data Source
The dataset is derived from the Bugzilla repository and represents bug-related activity for selected OSS products.

## Time Period
- Start Date: 01 September 2023  
- End Date: 31 August 2024  

## Description
The dataset contains aggregated bug lifecycle information for multiple OSS products over the specified time period. The data captures maintenance-related activity and is used as input to the d-set-based multi-criteria decision-making framework.

## Key Attributes
Each record includes:
- Product name  
- Number of New bugs (N)  
- Number of Fixed bugs (F)  
- Number of Assigned bugs (A)  
- Number of Reopened bugs (R)  i.e. Fixed or Verified status.

## Usage
This dataset is used to:
1. Construct interval-valued intuitionistic fuzzy (IVIF) parameters  
2. Generate d-set representations  
3. Derive product rankings based on maintenance performance  

## Notes
- The dataset reflects the most recent available state of each bug at the time of data extraction.  
- Historical state transitions were not available and are therefore not included.  
- The data is pre-processed to align with the requirements of the proposed evaluation framework.  

## Reproducibility
This file serves as input to the analysis scripts provided in the `/code` directory.

All identifying information has been removed to ensure compliance with double-blind review requirements.
