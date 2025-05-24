# 🏦 Loan Default Risk Analysis

**Course:** DATA 602 – Introduction to Data Analysis and Machine Learning  
**Term:** Spring 2025  
**Team Members:** Sai Bhargav K, Giridhar Sriram J, Jayanth R.  

---

## 📌 Project Overview

**Loan Default Risk Analysis** is a comprehensive machine learning project designed to predict the likelihood of a loan applicant defaulting, using structured financial and demographic data. This solution helps financial institutions make informed credit decisions, minimize risk exposure, and promote responsible lending practices.

---

## 📊 Dataset

We use the **Home Credit Default Risk** dataset from Kaggle, which contains over 307,000 application records and 122 features, including:

- **Demographics**: Age, gender, family size  
- **Financial Data**: Income, credit amount, annuity  
- **Credit History**: EXT_SOURCE scores  
- **Employment Info**: Occupation type, days employed  
- **Housing/Ownership Status**

Key data challenges handled:
- Class imbalance (8% default rate)
- High missing value ratios
- Skewed feature distributions
- Sparse and low-variance columns

---

## 🔍 Methodology

We followed the **CRISP-DM** process:

1. **Business Understanding**: Focused on predicting loan default risk for smarter credit decisions.
2. **Data Understanding & Preparation**:
   - Combined training/test datasets for consistent preprocessing
   - Imputed missing values using median strategy
   - Encoded categorical variables using Label and One-Hot Encoding
   - Feature engineering (`EXT_SOURCE_MEAN`, `EMPLOYED_FLAG`, etc.)
3. **Exploratory Data Analysis**:
   - Visualizations to understand default rates, skewness, and correlations
   - Identified key risk factors like age and income
4. **Modeling**:
   - Models: LightGBM, XGBoost, Random Forest, Logistic Regression, KNN, Decision Tree
   - Class balancing with SMOTE
   - Classification, Probability Ranking, and Explainability tasks
5. **Evaluation**:
   - ROC-AUC used as primary metric
   - 60/20/20 stratified split for train/validation/test
6. **Explainability**:
   - LIME for local instance-level explanations
   - Logistic Regression and Decision Trees for transparency

---

## 🏆 Model Performance

| Model              | AUC Score |
|-------------------|-----------|
| XGBoost           | 0.8201    |
| LightGBM          | 0.7707    |
| Logistic Regression | 0.7484  |
| Random Forest     | 0.7236    |
| KNN (subset)      | 0.5839    |
| Decision Tree     | ~0.75     |

---

## 🧠 Key Findings

- **Strongest predictors**: Age, income, external credit scores, bureau history
- **Tree-based models** performed best in classification and ranking tasks
- **SMOTE** improved minority class recall by balancing training data
- **LIME** supported ethical and explainable model usage

---

## ✅ Recommendations

- Use **XGBoost** or **LightGBM** for high-accuracy predictions
- Use **Logistic Regression** or **Decision Trees** in regulatory environments
- Enrich the dataset with time-series or repayment history
- Implement real-time scoring pipelines for production readiness
- Continuously retrain to reflect new economic and behavioral patterns

---

## 📁 Project Structure
```text
Loan-Default-Risk-Analysis/
│
├── README.md
├── .gitignore
│
├── docs/
│   └── Loan_Default_Executive_Summary.docx
│
├── presentation/
│   └── Loan_Default_PPT.pdf
│
├── notebooks/
│   └── Loan_Default_code.ipynb
│
└── data/
    └── dataset/



---

## 📄 Files Included

- `Loan_Default_code.ipynb`: Full pipeline with code, preprocessing, modeling, and evaluation
- `Loan_Default_Executive_Summary.docx`: Executive summary outlining objectives and results
- `Loan_Default_PPT.pdf`: Presentation deck showcasing visuals and model insights

---

## ⚠️ Assumptions & Limitations

- Assumes dataset is representative of typical loan applicants
- EXT_SOURCE scores are opaque and may vary across institutions
- No time-series or transaction-level data included
- Ensemble models, while accurate, limit interpretability despite LIME

---

## 🔍 Future Scope

- Integrate transaction logs for better prediction context
- Build an API interface for real-time loan risk scoring
- Explore fairness metrics to address demographic bias

---

## 📬 Contact

For queries, collaboration, or feedback, feel free to reach out  via GitHub or email.

---


