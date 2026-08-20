# Heart Disease Prediction — Weeks 2 & 3
**AnalystLab Africa | Data Science Internship Programme**
**Intern:** Mairame Samba Niang

##  Overview

This repository documents the continuing Heart Disease Prediction project for the AnalystLab Africa Data Science Internship Programme, from Week 2 (data preprocessing) through Week 3 (advanced exploratory analysis, statistical validation, and feature engineering), building toward Week 4 (predictive modelling).

**Business scenario:** Junior Data Scientist at AnalystLab Africa Consulting, preparing a validated, high-quality dataset to help predict whether a patient is likely to develop heart disease.

##  Project Progression

### Week 2 — Feature Engineering & Data Preprocessing
Cleaned the raw dataset (hidden missing values, outliers), engineered and validated features, encoded and scaled variables. See `Heart_Disease_Preprocessing.ipynb`, `Business_Understanding_Report_Week2.docx`, `Data_Preprocessing_Report.docx`.

### Week 3 — Advanced Data Exploration, Statistical Analysis & Feature Engineering
Built on the Week 2 cleaned dataset (no re-cleaning performed) to run 29 visualisations, 5 formal statistical hypothesis tests, 5 new engineered features, a full feature evaluation/selection pass, and produced the final modelling-ready dataset for Week 4. See `Heart_Disease_Advanced_Analysis.ipynb` and the reports below.

##  What This Project Covers (Week 3)

- **Advanced EDA:** 29 numbered visualisations across univariate, bivariate, and multivariate analysis.
- **Statistical Analysis:** 5 hypothesis tests (Independent T-Test, Chi-Square, ANOVA, Mann-Whitney U, Pearson Correlation) — each with research question, objective, method justification, H₀/H₁, test statistic, p-value, decision, interpretation, and business implication.
- **Feature Engineering:** 5 new features (AgeGroup, CholesterolRiskLevel, BPCategory, ST_DepressionCategory, CombinedRiskScore).
- **Feature Evaluation & Selection:** correlation-based redundancy analysis with an individually justified decision for every feature.
- **Final Modelling Dataset:** cleaned, encoded, scaled, and validated — ready for Week 4.

##  Key Findings

- 4 of 5 statistical tests were significant (p < 0.001): MaxHR, ChestPainType, ST_Depression, and Age are all formally validated predictors of heart disease.
- One test (ANOVA: Cholesterol across ST_Slope) was **not** significant (p ≈ 0.058) — reported honestly as a negative result.
- The engineered `CombinedRiskScore` achieved the strongest correlation with the target (r ≈ 0.72) of any feature in the dataset.
- Four binned/categorical engineered features were found redundant with their source numeric variables and excluded from the final ML dataset (kept only in the reporting dataset for interpretability).

##  Repository Structure

```
├── Heart_Disease_Preprocessing.ipynb        # Week 2 notebook
├── heart.csv                                # Original dataset
├── heart_cleaned.csv                        # Week 2 cleaned dataset
├── heart_ml_ready.csv                       # Week 2 ML-ready dataset
├── Business_Understanding_Report_Week2.docx
├── Data_Preprocessing_Report.docx
│
├── week3/                                   # Week 3 — Advanced Analysis, Statistics & Feature Engineering
│   ├── Heart_Disease_Advanced_Analysis.ipynb
│   ├── heart_final_ml_dataset.csv           # Final modelling dataset
│   ├── heart_week3_reporting_dataset.csv    # Human-readable dataset with engineered categories
│   ├── Project_Continuity_Summary.docx
│   ├── Statistical_Analysis_Report.docx
│   ├── Feature_Engineering_Documentation.docx
│   ├── Feature_Evaluation_Selection_Summary.docx
│   ├── Business_Insights_Report.docx
│   ├── Data_Dictionary.docx
│   └── requirements.txt
│
├── requirements.txt
└── README.md
```

## 🛠️ Tools & Libraries

Python 3 — Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn — see `requirements.txt`.

## ▶️ How to Run

```bash
git clone https://github.com/mairamesniang12/analystlab-week2-heart-disease-analysis.git
cd analystlab-week2-heart-disease-analysis
pip install -r requirements.txt
jupyter notebook Heart_Disease_Advanced_Analysis.ipynb
```

## 📊 Dataset Source

[Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

##  License

MIT License.

---
*Part of the AnalystLab Africa Data Science Internship Programme — Batch D.*
