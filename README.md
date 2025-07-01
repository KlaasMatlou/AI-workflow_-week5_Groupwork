# AI-workflow

# AI Development Workflow Project – Predicting Patient Readmission Risk

##  Project Overview

This project applies the **AI Development Workflow** to a real-world healthcare problem: predicting the likelihood of patient readmission within 30 days of hospital discharge. The solution is designed for use by hospitals to improve patient care, reduce costs, and allocate healthcare resources more effectively.

This repository includes:
- Problem definition and planning documentation
- Python code for data preprocessing, model development, evaluation
- Ethical reflection and workflow diagram
- Jupyter Notebook with reproducible analysis

---

## Problem Statement

**Objective*: Build a predictive model to identify patients at high risk of being readmitted within 30 days of hospital discharge.

**Stakeholders*:
- **Healthcare Providers*: Need insights to prevent avoidable readmissions.
- **Hospital Administrators*: Want to reduce operational costs and optimize patient flow.

**Key Performance Indicator (KPI)*: Achieve a minimum of 80% recall for positive (readmission) cases to ensure high-risk patients are not missed.

---

## Data Sources

1. **Electronic Health Records (EHRs)**: Patient history, diagnoses, procedures, medications.
2. **Demographics Data**: Age, gender, location, insurance type, socioeconomic status.

> ⚠Note: For demonstration, we use a public dataset from [Kaggle: Hospital Readmission Dataset](https://www.kaggle.com/datasets).

---

## Data Preprocessing

Steps:
- Handle missing and inconsistent values
- Feature engineering (e.g., number of previous admissions)
- One-hot encoding for categorical variables
- Normalization of continuous variables
- Train-validation-test split (70-15-15)

---

## Model Development

**Chosen Model*: Logistic Regression (interpretable, fast, suitable for healthcare)

**Why Not Deep Learning?*
- Limited data availability
- Emphasis on interpretability over raw accuracy

**Hyperparameters Tuned*:
- `C`: Inverse regularization strength
- `solver`: Optimization algorithm used for model training

---

## Evaluation

**Metrics Used*:
- **Precision*: To minimize false alarms
- **Recall*: To identify actual readmissions
- **F1-Score*: To balance precision and recall

*Sample Confusion Matrix (Hypothetical)*:

|            | Predicted Yes | Predicted No |
|------------|----------------|--------------|
| Actual Yes | 40             | 10           |
| Actual No  | 20             | 130          |

- **Precision*: 0.67
- **Recall*: 0.80
- **F1-score*: 0.73

---

##  Deployment Plan

- Integrate model into the hospital’s Electronic Medical Record (EMR) system.
- Automatically flag high-risk patients at discharge.
- Alerts sent to case managers or care coordinators.
- Schedule monthly model retraining for concept drift handling.

---

## Ethical Considerations

### Potential Bias:
- Historical data may reflect disparities in care across different races or income levels.
- Underrepresented populations may receive inaccurate predictions.

### Mitigation Strategy:
- Use tools like IBM AI Fairness 360.
- Reweigh datasets to balance representation.
- Evaluate fairness metrics during model testing.

---

## Workflow Diagram

![AI Development Workflow Diagram](diagram.png)

> This diagram illustrates the AI workflow: from problem definition to model monitoring.

---

## Reflection

- Biggest Challenge: Ensuring fairness while maintaining model performance.
- Future Improvements:
  - Gather more diverse, real-world hospital data.
  - Deploy multiple models and choose dynamically based on patient profiles.

---

##  Tools & Technologies

- Python 3.x
- Jupyter Notebooks
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
- draw.io or Canva 

