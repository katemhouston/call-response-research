# Analysis

This folder contains scripts that perform statistical analysis on the cleaned and processed emergency response data.

## Purpose

The goal of this stage is to:
- Test for significant differences in response time patterns across call priorities, responding agencies (CAHOOTS vs EPD), and CAHOOTS capacity status (available vs full)
- Generate statistical results to support the main research questions and interpretations

### `stats_tests_priority.ipynb`
- Compares response times across call priority levels (1–9, P)
- Tests include ANOVA and t-tests (overall and per-priority)
- Normalizes data for fair comparison
- Output: `priority_results.csv`

### `stats_tests_capacity.ipynb`
- Tests whether CAHOOTS’ availability (full vs available) impacts response times for both CAHOOTS and EPD
- Includes Levene’s test, t-tests, and KS tests
- Output: `capacity_results.csv`
  
## Input Files

Located in `../data/`:
- `cleaned_data.csv`: Output from the cleaning stage
- `busy_log.csv`: Contains call start/end times and overlap info for CAHOOTS
- `epd_with_capacity.csv`: Contains call start/end times and overlap info for EPD

## Output Files

Saved to `../results/`:
- `results_priority.csv`: DataFrame containing test statistics and p-values from **priority** analysis
- `results_capacity.csv`: DataFrame containing test statistics and p-values from **capacity** analysis

## How to Run

Run each Jupyter notebook, in any order:

- `stats_tests_priority.ipynb`
- `stats_tests_capacity.ipynb`

This project uses the following Python packages:

- pandas
- numpy
- scipy
- matplotlib
- seaborn

Standard library modules used:
- datetime (for timestamp parsing and operations)
- re (regular expressions for string cleaning)
