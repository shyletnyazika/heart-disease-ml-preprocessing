# Heart Disease Prediction — Feature Engineering & Data Preprocessing

**AnalystLab Africa — Data Science Internship Programme | Week 2**

## Overview
This project prepares the Heart Disease Prediction dataset for machine learning, following a full preprocessing pipeline: data cleaning, feature engineering, feature encoding, feature scaling, outlier detection, and feature selection. The goal is to transform raw clinical data into a machine-learning-ready dataset while documenting every preprocessing decision made along the way.

## Dataset
[Heart Disease Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) (Kaggle) — 918 patients, 12 clinical features. Target variable: `HeartDisease` (1 = disease, 0 = no disease).

## Tools Used
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- Google Colab

## Files in This Repository
| File | Description |
|---|---|
| `Heart_Disease_Preprocessing_Week2.ipynb` | Full notebook — data inspection, cleaning, feature engineering, encoding, scaling, outlier detection, feature selection, and 6+ visualisations |
| `heart_cleaned.csv` | Dataset after cleaning (missing values handled, duplicates removed) — before encoding/scaling |
| `heart_ml_ready.csv` | Final machine-learning-ready dataset — encoded and scaled |
| `Week2_Business_Understanding_Report` | Business problem, project objective, target variable, and expected impact |
| `Week2_Data_Preprocessing_Report` | Full explanation of every preprocessing decision and justification |

## Key Preprocessing Decisions
- **Hidden missing data:** `Cholesterol` and `RestingBP` contained biologically impossible zero values (172 and 1 rows respectively) — treated as missing and filled with the column median.
- **Feature engineering:** created an `AgeGroup` feature; renamed two columns for clarity.
- **Encoding:** Label Encoding for binary categorical fields, One-Hot Encoding for multi-category fields.
- **Scaling:** StandardScaler applied to all continuous numeric features.
- **Outliers:** identified via IQR method (41 in RestingBP, 41 in Cholesterol, 16 in Oldpeak) and deliberately retained, since extreme clinical values are medically meaningful rather than data errors.
- **Feature selection:** correlation analysis identified `ST_Slope`, `ExerciseInducedAngina`, `Oldpeak`, and `MaxHR` as the strongest predictors of heart disease.

## About Me
Final-year Medical Analytics and Informatics student at the University of Zimbabwe, currently a Data Science Intern at AnalystLab Africa.

[Connect with me on LinkedIn](https://www.linkedin.com/in/shylet-nyazika-04585329b/)
