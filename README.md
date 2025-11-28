# ADA Final Project: County-Level Insurance Coverage and Chlamydia Incidence in Missouri (2022)

## Project Description
This repository contains the dataset and R Markdown code used for my **Advanced Data Analysis (ADA) Final Project**. The project evaluates whether county-level uninsurance is associated with chlamydia incidence rates in Missouri and examines whether this relationship differs by race, rurality, or gender composition. All analyses were conducted using R version 4.4.2.

## Files Included
- `ada_project.csv`: County-level dataset used in the analysis  
- `agyei_ada_markdown.Rmd`: Full R Markdown file containing all data cleaning, descriptive analysis, regression models, maps, and results  
- `README.md`: This file  

## Data Source
Data were obtained from the **2022 County Health Rankings & Roadmaps** dataset (University of Wisconsin Population Health Institute).  
Variables analyzed include:
- **Outcome:** Chlamydia incidence rate per 100,000  
- **Exposure:** % uninsured adults  
- **Covariates:** % with some college, income ratio, % unemployed  
- **Effect modifiers tested:** % non-Hispanic Black, % rural population, % female  

## What the Code Does
The R Markdown script (`Agyei_ADA_Markdown.Rmd`) performs the following steps:
- Imports and cleans the dataset
- Renames and prepares variables for analysis
- Generates descriptive statistics and **Table 1**
- Creates Missouri county maps using `tigris` and `sf`
- Fits Poisson and Negative Binomial regression models
- Conducts interaction analyses for race, rurality, and gender
- Computes Incidence Rate Ratios (IRRs) and 95% CIs
- Exports formatted regression tables for presentation
- Produces all figures, maps, and outputs included in the final project

## How to Run the Code
1. Clone or download this repository.  
2. Open `Agyei_ADA_Markdown.Rmd` in RStudio.  
3. Install required packages:

```r
install.packages(c("tidyverse", "janitor", "broom", "MASS",
                   "pscl", "sf", "tigris", "gtsummary",
                   "flextable", "officer"))
