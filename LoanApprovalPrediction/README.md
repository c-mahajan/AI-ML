# Loan Approval ML Project (End-to-End)

An end-to-end machine learning project for predicting **loan approval status** from applicant and financial features.  
This repository demonstrates a complete workflow: data loading, preprocessing, model training, evaluation, and inference-ready pipeline.

---

## 1) Project Overview

Loan approval is a binary classification problem where the model predicts whether a loan application should be approved based on historical records.

### Objectives
- Build a robust, reproducible ML pipeline.
- Compare multiple classification models.
- Optimize model quality using validation and tuning.
- Save the best model for future inference/deployment.

### Business Value
- Faster and more consistent underwriting decisions.
- Reduced manual review overhead.
- Better risk control via data-driven predictions.

---

## 2) Problem Statement

Given applicant profile and financial attributes (e.g., income, dependents, loan amount, credit history), predict:

- **Target**: `Loan_Status`  
  - `Y` = Approved  
  - `N` = Not Approved

This is treated as a **supervised binary classification** task.

---

## 3) Repository Structure

```text
E2E Project/
├─ loan_approval_ml_project.ipynb   # Main notebook: EDA, preprocessing, training, evaluation
├─ README.md                        # Project documentation
├─ requirements.txt                 # Python dependencies (if present)
├─ data/                            # Raw/processed datasets (if present)
├─ models/                          # Saved trained models (if present)
└─ src/                             # Reusable scripts/modules (if present)
```

> If your folder structure differs, update this section accordingly.

---

## 4) Dataset

Typical columns used in loan approval datasets:
- `Gender`
- `Married`
- `Dependents`
- `Education`
- `Self_Employed`
- `ApplicantIncome`
- `CoapplicantIncome`
- `LoanAmount`
- `Loan_Amount_Term`
- `Credit_History`
- `Property_Area`
- `Loan_Status` (target)

### Common Data Issues Handled
- Missing values in numeric/categorical columns
- Categorical feature encoding
- Class imbalance
- Outliers/skewed financial variables

---

## 5) ML Workflow (Notebook Summary)

The notebook generally follows this pipeline:

1. **Import Libraries**
   - `pandas`, `numpy`, `matplotlib`, `seaborn`
   - `scikit-learn` modules for preprocessing/modeling/evaluation

2. **Data Loading**
   - Read dataset into DataFrame
   - Inspect shape, columns, datatypes

3. **EDA**
   - Distribution checks
   - Correlation/relationship analysis
   - Approval patterns by key attributes

4. **Data Preprocessing**
   - Missing value imputation
   - Encoding categorical variables
   - Feature scaling (as needed)
   - Train/test split

5. **Model Training**
   - Baseline + candidate models (commonly):
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - XGBoost/Gradient Boosting (if used)

6. **Evaluation**
   - Accuracy
   - Precision, Recall, F1-score
   - ROC-AUC (if applicable)
   - Confusion Matrix
   - Cross-validation

7. **Model Selection**
   - Compare candidate models
   - Choose best-performing model based on validation metrics

8. **Model Persistence**
   - Save preprocessing + model pipeline using `joblib`/`pickle` for inference

---

## 6) Results

> Replace the placeholders with exact notebook values.

- **Accuracy:** **96.60%** (825 correct predictions out of 854 samples)
- **Precision:** 97.42% (Of all approved predictions, 97.42% were actually approved)
- **Recall:** 93.50% (Of all actual approvals, 93.50% were correctly identified)
- **F1-Score:** 0.9542 (Harmonic mean of precision and recall)
- **ROC-AUC:** 0.9932 (Excellent discrimination ability)

### Example Interpretation
- Higher recall helps reduce false rejections of good applicants.
- Balanced precision-recall reduces both risky approvals and missed opportunities.

---

## 7) How to Run

## Prerequisites
- Python 3.9+ (recommended)
- Jupyter Notebook / VS Code with Python + Jupyter extensions

## Setup (Windows PowerShell)
```powershell
# Create virtual environment
python -m venv .venv

# Activate
.\.venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt
```

## Run Notebook
```powershell
jupyter notebook loan_approval_ml_project.ipynb
```

Or open in VS Code and run all cells.

---

## 8) Reproducibility

To ensure reproducibility:
- Fix random seeds (`random_state`)
- Keep preprocessing inside a single sklearn pipeline
- Track package versions in `requirements.txt`
- Save trained artifacts with version tags

---

## 9) Inference Example (Template)

```python
import joblib
import pandas as pd

# Load saved pipeline
model = joblib.load("models/loan_approval_pipeline.joblib")

# Single applicant example
sample = pd.DataFrame([{
    "Gender": "Male",
    "Married": "Yes",
    "Dependents": "1",
    "Education": "Graduate",
    "Self_Employed": "No",
    "ApplicantIncome": 5000,
    "CoapplicantIncome": 1500,
    "LoanAmount": 150,
    "Loan_Amount_Term": 360,
    "Credit_History": 1.0,
    "Property_Area": "Urban"
}])

pred = model.predict(sample)[0]
print("Approved" if pred in [1, "Y"] else "Not Approved")
```

---

## 10) Future Improvements

- Hyperparameter optimization (Optuna/GridSearchCV/RandomizedSearchCV)
- Better handling of class imbalance (SMOTE/class weights)
- Explainability with SHAP/LIME
- Drift monitoring for production
- API + UI deployment (FastAPI/Streamlit)

---

## 11) Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook
- Joblib / Pickle

---

## 12) Author

- **Name**: `Chetan Mahajan`
- **Project**: Loan Approval ML (E2E)

---

## 13) Quick Checklist Before Publishing

- [ ] Replace placeholder metrics with actual notebook results  
- [ ] Confirm final model name and saved artifact path  
- [ ] Add exact dataset source and citation  
- [ ] Add `requirements.txt` with pinned versions  
- [ ] Include screenshots/plots from EDA and model evaluation  
