# Credit Risk Mini Project (loan.csv)

## Goal
Explore origination-time factors related to loan default.

## Data
- File: data/loan.csv
- Key fields used: loan_amnt, funded_amnt, term, int_rate, grade, sub_grade, annual_inc, dti, fico_range_low/high, revol_util, open_acc, total_acc, home_ownership, purpose, emp_length, loan_status

## Target Definition
- default_flag = 1 if loan_status in {Charged Off, Default}
- default_flag = 0 if loan_status == Fully Paid
- All other statuses excluded

## Cleaning
- term -> term_clean (months, numeric)
- int_rate -> int_rate_clean (%, numeric)
- revol_util -> revol_util_clean (%, numeric)
- emp_length -> emp_length_years (0–10)
- fico_mid = (fico_range_low + fico_range_high) / 2
