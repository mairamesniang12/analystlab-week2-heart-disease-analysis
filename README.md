# Heart Disease Prediction — Feature Engineering & Data Preprocessing
**AnalystLab Africa | Data Science Internship Programme — Week 2**
**Intern:** Mairame Samba Niang 

##  Overview

This is the Week 2 deliverable of the AnalystLab Africa Data Science Internship Programme. Building on the Week 1 exploratory analysis, this project prepares the **Heart Failure Prediction dataset** for machine learning, cleaning, encoding, scaling, and engineering features ahead of Week 3's model development.

**Business scenario:** Junior Data Scientist at AnalystLab Africa Consulting, preparing a dataset to help predict whether a patient is likely to develop heart disease.

##  Business Questions Answered

1. Which features are most relevant to the prediction problem?
2. Which variables require encoding?
3. Which variables require scaling or normalization?
4. Are there any redundant or highly correlated features?
5. How should missing values and outliers be handled?
6. What preprocessing techniques improve dataset quality?
7. Is the dataset ready for machine learning?

## 🔑 Key Findings & Decisions

- Discovered **172 hidden missing values** in `Cholesterol` and 1 in `RestingBP`, encoded as physiologically impossible zeros rather than `NaN` imputed with the median.
- Engineered a new feature, `HR_Reserve` (heart rate reserve) then **removed it** after correlation analysis revealed it was highly redundant with `MaxHR` (r ≈ -0.93), demonstrating a full feature-selection workflow rather than keeping every engineered feature by default.
- Applied **Label Encoding** (binary variables), **Ordinal Encoding** (`ST_Slope`, which has a natural order), and **One-Hot Encoding** (nominal categories).
- Applied **RobustScaler** to continuous features, chosen specifically for its resilience to the outliers detected via the IQR method.
- Random Forest feature importance confirmed `ST_Slope`, chest pain type, `ST_Depression`, and `MaxHR` as the strongest predictors consistent with established cardiology risk factors.

## 📁 Repository Structure

```
├── Heart_Disease_Preprocessing.ipynb          # Main analysis notebook
├── heart.csv                                  # Original dataset
├── heart_cleaned.csv                          # Cleaned dataset (human-readable)
├── heart_ml_ready.csv                         # Final machine-learning-ready dataset
├── Business_Understanding_Report_Week2.docx
├── Data_Preprocessing_Report.docx
├── data/                                      # Supporting data files
└── README.md
```

## 🛠️ Tools & Libraries

- Python 3 — Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- Jupyter Notebook

## ▶️ How to Run

```bash
git clone https://github.com/mairamesniang12/analystlab-week2-heart-disease-analysis.git
cd analystlab-week2-heart-disease-analysis
pip install pandas numpy matplotlib seaborn scikit-learn notebook
jupyter notebook Heart_Disease_Preprocessing.ipynb
```

## 📊 Dataset Source

[Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

## 📜 License

MIT License — see [LICENSE](./LICENSE).

---
*Part of the AnalystLab Africa Data Science Internship Programme — Batch D.*
