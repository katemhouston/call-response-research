# Analysis

This folder contains scripts that perform statistical analysis on the cleaned and processed emergency response data.

## Purpose

The goal of this stage is to: ##UPDATE
- Test for significant differences in response time patterns across priorities, agencies, and capacities
- Generate results to support the research questions

## Folder Contents

- `stats_tests_priority.ipynb`: Performs an ANOVA and t-tests to compare response times between CAHOOTS and EPD across different priorities.
- `stats_tests_capacity.ipynb`: Performs Levene’s tests, t-tests, and Kolmogorov-Smirnov tests to compare response times between full and available capacities for EPD and CAHOOTS.

## Input Files

Expected to be located in `../data/`:
- `cleaned_data.csv`: Output from the cleaning stage
- `busy_log.csv`: Contains call start/end times and overlap info for CAHOOTS
- `epd_with_capacity.csv`: Contains call start/end times and overlap info for EPD
- 
## Output Files

Saved to `../results/`:
- `results_priority.csv`: DataFrame containing test statistics and p-values from **priority** analysis
- `results_capacity.csv`: DataFrame containing test statistics and p-values from **capacity** analysis
- *(Optional)* any figures or plots generated

## How to Run

Run each Jupyter notebook, in any order:

- `stats_tests_priority.ipynb`
- `stats_tests_capacity.ipynb`
