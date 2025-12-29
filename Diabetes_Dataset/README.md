# Diabetes Prediction Using Linear Regression

## 📌 Project Overview
This project focuses on building and evaluating a **Linear Regression model** to predict diabetes outcomes using clinical and demographic attributes. The objective is to understand how key health indicators such as glucose levels, BMI, age, and insulin contribute to diabetes risk, while also demonstrating a complete end-to-end **data preprocessing → modeling → evaluation workflow**.

This repository contains:
- A Jupyter Notebook with data preprocessing and modeling steps
- Exploratory analysis of diabetes-related features
- A regression-based predictive model
- Performance evaluation and interpretation of results

---

## 📂 Dataset Description
The dataset contains medical predictor variables and a target variable indicating diabetes outcome.

### Columns
| Column Name   | Description |
|--------------|------------|
| pregnancies  | Number of times the patient was pregnant |
| glucose      | Plasma glucose concentration |
| diastolic    | Diastolic blood pressure (mm Hg) |
| triceps      | Triceps skin fold thickness (mm) |
| insulin      | 2-hour serum insulin (mu U/ml) |
| bmi          | Body Mass Index (weight in kg / height in m²) |
| dpf          | Diabetes Pedigree Function (genetic influence) |
| age          | Age of the patient (years) |
| diabetes     | Target variable indicating diabetes presence |

---

## 🔧 Technologies Used
- **Python**
- **Pandas** – data manipulation
- **NumPy** – numerical computations
- **Matplotlib / Seaborn** – data visualization
- **Scikit-learn** – model building and evaluation
- **Jupyter Notebook**

---

## 🧪 Methodology

### 1. Data Loading
- Imported the dataset into a Pandas DataFrame
- Performed initial inspection using `.head()`, `.info()`, and `.describe()`

### 2. Data Preprocessing
- Identified and handled missing or zero-valued medical attributes
- Checked feature distributions and data consistency
- Separated features (`X`) and target variable (`y`)

### 3. Exploratory Data Analysis (EDA)
- Analyzed relationships between glucose, BMI, age, and diabetes outcome
- Identified potential multicollinearity and data skewness
- Visualized feature correlations using heatmaps

### 4. Model Building
- Implemented **Linear Regression** using Scikit-learn
- Split data into training and testing sets
- Trained the model on the training dataset

### 5. Model Evaluation
- Evaluated performance using:
  - R² Score
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
- Interpreted regression coefficients to understand feature impact

---

## 📊 Results & Insights
- Glucose level and BMI emerged as strong predictors of diabetes
- Age and genetic predisposition (DPF) showed moderate influence
- Linear Regression provided a baseline predictive framework, suitable for interpretability but limited for complex non-linear patterns

---

## 🚀 Future Improvements
- Replace Linear Regression with classification models (Logistic Regression, Random Forest, XGBoost)
- Perform feature scaling and normalization
- Address class imbalance if present
- Add cross-validation for robust evaluation
- Deploy the model as a simple API or dashboard
