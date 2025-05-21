# Data Cleaning

This folder contains scripts for cleaning the raw CAD data and generating derived data files for analysis.

## Purpose

The goal of this stage is to:
- Clean and standardize raw call data
- Create separate busy log files for EPD and CAHOOTS calls
- Output structured CSV files for analysis

## Folder Contents

- `updated_data_cleaning.ipynb`: Loads raw data, fixes formatting issues, and outputs a cleaned version.
- `creating_busy_log_CAHOOTS.ipynb`: Creates a busy log for CAHOOTS from the cleaned dataset. 
- `creating_EPD_capacity_log.ipynb`: Creates a busy log for EPD from the cleaned dataset.

## Input Files

Located in `../data/`:
- `class_data_2014.csv`
- `class_data_2015.csv`
- `class_data_2016.csv`
- `class_data_2017.csv`
- `class_data_2018.csv`
- `class_data_2019.csv`
- `class_data_2020.csv`
- `class_data_2021.csv`
- `class_data_2022.csv`
- `class_data_2023.csv`
- `class_data_2024.csv`
- `class_data_2025.csv`

## Output Files

Saved to `../data/`:
- `cleaned_full_class_data.csv`: Cleaned and merged call data
- `busy_log.csv`: Contains call start/end times and overlap info for CAHOOTS
- `epd_with_capacity.csv`: Contains call start/end times and overlap info for EPD

## How to Run

Run the jupyter files in the following order:

1. updated_data_cleaning.ipynb
2. creating_busy_log_CAHOOTS.ipynb
3. creating_EPD_capacity_log.ipynb

## Dependencies

This project uses the following Python packages:

- pandas
- numpy
- scipy
- matplotlib
- seaborn

Standard library modules used:
- datetime (for timestamp parsing and operations)
- re (regular expressions for string cleaning)
