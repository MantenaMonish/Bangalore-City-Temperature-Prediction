# 🌡️ Bangalore Temperature Prediction (1990–2022)

A data science project that uses historical weather data from Bangalore to predict **maximum daily temperatures (`tmax`)** using multiple machine learning models.

---

## Project Overview

This project explores the relationship between average temperature, minimum temperature, and precipitation to forecast the **maximum temperature**. It includes:

- Data Cleaning and Imputation
- Exploratory Data Analysis (EDA)
- Model Training using:
  - Linear Regression
  - Support Vector Regression (SVR)
  - K-Nearest Neighbors (KNN)
  - Decision Tree
  - Random Forest
  - XGBoost
- Performance Evaluation
- Visualization of Predictions

---

## Dataset

- File: `Bangalore_1990_2022_BangaloreCity.csv`
- Columns:
  - `time` – Date
  - `tavg` – Average daily temperature
  - `tmin` – Minimum temperature
  - `tmax` – Maximum temperature (target)
  - `prcp` – Precipitation

---

## EDA & Preprocessing

- Missing values imputed using **mode** for each column.
- Correlation Analysis:
  - `tmax` is strongly correlated with `tavg` and `tmin`
- Visualizations:
  - Heatmap of feature correlations
  - Pairplot for relationships between features

---

## Models Used

| Model                | MSE (Lower is Better) |
|----------------------|------------------------|
| Linear Regression     | ~1.83                 |
| SVR (RBF Kernel)      | ~1.78                 |
| KNN (k=10)            | ~1.89                 |
| Random Forest         | ~1.98                 |
| Decision Tree (depth=5) | ~1.85              |
| XGBoost               | ~1.78 (Best)          |

**XGBoost** gave the best prediction performance on unseen data.

---

## Results Visualization

- Line plot comparing actual vs predicted values for the first 10 test samples.
- Heatmap and pairplots for feature insights.

---

![image alt](https://github.com/MantenaMonish/Spectacles_Detection_Deep_Learning-/blob/a4e1cf8e9670fab74bc6a9b33128ae717a6132ff/Images/glasses.png)

## 🚀 How to Run

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
