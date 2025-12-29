# HR Analytics — Data Preprocessing for Employee Attrition (hr_data.csv)

## Overview
This project focuses on preparing an HR dataset (`hr_data.csv`) for building a **predictive model** to solve the **employee retention / attrition** problem.

The notebook performs:
- Data loading and validation checks
- Missing-value analysis and imputation
- Feature inspection and visualization
- Categorical encoding (one-hot encoding)
- Export of a clean dataset for modeling

> Output: `hr_data_processed.csv`

---

## Business Problem
Organizations want to understand which factors correlate with employees leaving and prepare data that can support a predictive model.

**Target column**
- `left`  
  - Interpreted as: **1 = employee left**, **0 = employee stayed**
  - Initial values in the notebook are treated as `yes/no` and converted to binary.

---

## Dataset Columns
Original columns in `hr_data.csv`:
- `satisfaction_level`
- `last_evaluation`
- `number_project`
- `average_montly_hours`
- `time_spend_company`
- `work_accident`
- `left`
- `promotion_last_5years`
- `is_smoker`
- `department`
- `salary`

---

## Quick Data Validation
The notebook checks:
- Column names after loading
- First rows preview
- Row count comparisons (file vs dataframe)
- Target distribution visualization (`left`)

---

## Missing Values Analysis
The notebook calculates missing values per column.

### Missing values (count)
- `average_montly_hours`: **368**
- `time_spend_company`: **151**
- `is_smoker`: **14764**
- All other columns: **0**

### Missing values (%)
- `average_montly_hours`: **~2.45%**
- `time_spend_company`: **~1.01%**
- `is_smoker`: **~98.43%**

**Decision**
- `is_smoker` is dropped due to extremely high missingness.

---

## Preprocessing Steps

### 1) Drop low-quality feature
- Dropped: `is_smoker` (≈98% missing)

### 2) Impute `time_spend_company` with median
- Strategy: fill missing values with the column median  
- Rationale: robust to outliers and keeps a realistic central tendency

⚠️ **Important Note (Bug Fix Needed)**
In the notebook, the code uses:
```python
df['time_spend_company'] = df['time_spend_company'].fillna(median_value, inplace=True)
