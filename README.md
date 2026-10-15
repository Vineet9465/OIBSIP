# Data Cleaning — Titanic Passenger Dataset
**Oasis Infobyte — Data Analytics Internship (Level 1, Task 3)**
**Author:** Vineet Pandey

## Objective
Turn a real-world dataset with missing values, outliers and inconsistent formats into a clean, analysis-ready dataset, and document every decision.

## Dataset
Titanic passenger data: 891 passengers, 12 columns (`titanic.csv`).

## Steps Performed
1. **Data quality report:** nulls per column, duplicates, data types and value-range checks.
2. **Missing data:**
   - `Age` (177 missing): filled with the median age of each Pclass and Sex group
   - `Embarked` (2 missing): filled with the most common port
   - `Cabin` (687 missing, 77%): dropped, after keeping a `Has_Cabin` flag
3. **Duplicates:** checked, and none were found (repeated tickets are families or groups, so they were kept).
4. **Standardisation:** trimmed text, `Sex` to Male/Female, port codes to port names, and a clean `Title` column extracted from `Name`.
5. **Outliers (IQR method):** `Age` retained (real ages), `Fare` capped into a new column `Fare_Capped`, 15 zero fares flagged with `Zero_Fare`.
6. **Data types:** `PassengerId` as text, group columns as category, flags as integers.
7. **Before vs after summary table**, then the cleaned data saved to `titanic_cleaned.csv`.

## Before vs After

| Measure | Before | After |
|---|---|---|
| Rows | 891 | 891 |
| Columns | 12 | 15 |
| Total null values | 866 | 0 |
| Columns with nulls | 3 | 0 |
| Duplicate rows | 0 | 0 |
| Columns with correct data type | 8 / 12 | 15 / 15 |

## Tech Stack
Python, pandas, numpy, matplotlib, seaborn, Jupyter Notebook

## Files
- `Data_Cleaning.ipynb`: full cleaning notebook (executed, with charts and written justifications)
- `titanic.csv`: original raw dataset
- `titanic_cleaned.csv`: cleaned dataset
- `README.md`: this file

## How to Run
1. Install dependencies: `pip install pandas numpy matplotlib seaborn jupyter`
2. Open `Data_Cleaning.ipynb` in Jupyter, VS Code or Google Colab, with `titanic.csv` in the same folder.
3. Run all cells top to bottom. The cleaned file is written to `titanic_cleaned.csv`.
