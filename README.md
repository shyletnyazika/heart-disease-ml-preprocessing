# Heart Disease Prediction — AnalystLab Africa Data Science Internship

**Progression: Week 2 (Preprocessing) → Week 3 (Advanced Analysis & Statistical Validation) → Week 4 (Modelling, upcoming)**

## Project Overview
This project analyzes the Heart Disease Prediction dataset to support a healthcare provider's goal of identifying patients likely to develop heart disease using routine clinical measurements. The project has progressed through data preprocessing (Week 2), advanced statistical analysis and feature engineering (Week 3), and will conclude with predictive model development (Week 4).

## Dataset
[Heart Disease Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) (Kaggle) — 918 patients, 12 original clinical features. Target: `HeartDisease` (1 = disease, 0 = no disease).

## Tools & Libraries
Python, Google Colab, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn. See `requirements.txt`.

## Repository Contents

### Week 2 — Preprocessing
| File | Description |
|---|---|
| `notebooks/Heart_Disease_Preprocessing_Week2.ipynb` | Data cleaning, encoding, scaling, outlier detection |
| `data/heart_cleaned_correct.csv` | Cleaned dataset (missing values fixed, NOT yet encoded/scaled) |
| `data/heart_ml_ready.csv` | Fully encoded and scaled dataset |
| `reports/Week2_Business_Understanding_Report.docx` | Business problem, objective, target variable |
| `reports/Week2_Data_Preprocessing_Report.docx` | Full preprocessing decisions and justification |

### Week 3 — Advanced Analysis & Statistical Validation
| File | Description |
|---|---|
| `notebooks/Heart_Disease_Week3_Advanced_Analysis.ipynb` | 13 visualizations, 5 statistical tests, 3 engineered features, feature evaluation |
| `data/heart_week3_refined.csv` | Final refined dataset with engineered features — foundation for Week 4 |
| `reports/Week3_Project_Continuity_Summary.docx` | How Week 3 builds on Weeks 1–2 |
| `reports/Week3_Statistical_Analysis_Summary.docx` | 5 hypothesis tests with full statistical interpretation |
| `reports/Week3_Feature_Engineering_Documentation.docx` | 3 new engineered features, fully documented |
| `reports/Week3_Feature_Evaluation_Selection_Summary.docx` | Correlation + Random Forest importance evaluation |
| `reports/Week3_Business_Insights_Recommendations_Report.docx` | Executive summary, findings, recommendations, limitations |
| `reports/Week3_Data_Dictionary.docx` | Updated field reference including engineered features |

## Key Findings (Week 3)

**Statistically validated predictors** (all p < 0.0001): MaxHR, Sex, ChestPainType, Oldpeak, ExerciseAngina.

**Most important engineered feature:** `HighRiskSymptomCount` (composite of ASY chest pain + exercise angina + elevated Oldpeak) — correlation of 0.62 with the target, and the 2nd most important feature in a preliminary Random Forest model, outperforming any of its individual source variables.

**Notable pattern:** Asymptomatic (ASY) chest pain patients showed the highest heart disease rate (79%) of any chest pain category — a clinically important, counterintuitive finding.

**Dataset limitation:** Gender imbalance (725 male vs 193 female patients) — flagged for careful evaluation in Week 4 model performance.


## About Me
Final-year Medical Analytics and Informatics student at the University of Zimbabwe, currently a Data Science Intern at AnalystLab Africa.

[Connect with me on LinkedIn](https://www.linkedin.com/in/shylet-nyazika-04585329b/)
