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




# 🧠 HR Data Preprocessing Pipeline for Predictive Analytics

> **End-to-end data preprocessing system for HR analytics, employee attrition modeling, and workforce intelligence.**

---

## 🔎 Project Summary

This project implements a **production-grade data preprocessing pipeline** designed to transform raw Human Resources (HR) data into a **machine-learning-ready dataset**.

The pipeline supports downstream use cases including:

- Employee attrition prediction  
- Workforce analytics  
- Performance forecasting  
- Engagement and retention modeling  
- People analytics dashboards  

The notebook demonstrates **real-world data engineering practices** such as data cleaning, missing value imputation, feature encoding, and dataset validation — all critical steps in building reliable predictive models.

---

## 🎯 Business Value

Most machine learning projects fail because of **poor data quality**, not poor models.

This project solves that problem by:

- Converting messy HR records into **structured analytical features**
- Enabling **accurate predictive modeling** for HR teams
- Reducing data preparation time for analysts and data scientists
- Providing a **repeatable preprocessing workflow** for enterprise use

This pipeline mirrors how **data engineers and analytics teams** prepare data in production environments.

---

## 🧩 Key Capabilities

### Data Engineering & Preparation
- Data ingestion from raw HR datasets  
- Schema validation and column inspection  
- Missing value detection and treatment  
- Group-wise numerical imputation  
- Feature standardization and formatting  

### Feature Engineering
- Categorical variable encoding (One-Hot Encoding)  
- Binary feature transformation  
- Boolean normalization  
- Dataset consistency checks  

### Machine Learning Readiness
- Outputs a **clean, structured dataset** optimized for:
  - Logistic Regression  
  - Random Forest  
  - XGBoost  
  - Gradient Boosting  
  - Neural Networks  

Final output: hr_data_processed.csv

---

## ⚙️ Technical Workflow

1. **Data Loading**
   - Reads raw HR data from CSV  
   - Performs exploratory inspection (`head`, `info`, `describe`)

2. **Data Cleaning**
   - Identifies null values and inconsistent entries  
   - Applies **group-based mean imputation** for numerical attributes  
   - Ensures zero missing values in final dataset  

3. **Feature Engineering**
   - Encodes categorical attributes using **One-Hot Encoding**
   - Converts boolean flags to binary indicators  
   - Prepares structured features for ML pipelines  

4. **Data Export**
   - Saves the finalized dataset for modeling and analytics workflows  

---

## 🛠️ Tech Stack

**Languages & Tools**
- Python  
- Jupyter Notebook  

**Libraries**
- Pandas — data wrangling, preprocessing, feature engineering  
- NumPy — numerical computing  
- Matplotlib & Seaborn — exploratory data analysis (EDA)  

**Core Skills Demonstrated**
- Data preprocessing  
- Data cleaning  
- Feature engineering  
- Missing value imputation  
- Categorical encoding  
- Machine learning pipeline preparation  
- HR analytics  
- Workforce analytics  
- Predictive modeling support  

---

## 🚀 Getting Started

### Clone the Repository
```bash
git clone https://github.com/your-username/hr-data-preprocessing.git
cd hr-data-preprocessing

### Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn

### Run the Notebook
```bash
HR_Data_Preprocessing.ipynb

### Output
hr_data_processed.csv
---

## 📈 Real-World Use Cases

### This preprocessing system can directly support:
- Employee attrition prediction models
- HR KPI dashboards
- Workforce planning analytics
- Talent retention strategies
- Organizational performance forecasting
- People operations reporting
