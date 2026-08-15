# Heart Failure Survival Analysis

This project analyzes survival patterns among patients with heart failure using the **Heart Failure Clinical Records Dataset** from the UCI Machine Learning Repository.

The analysis applies statistical survival analysis techniques to identify clinical factors associated with mortality risk and understand differences in patient survival over time.

## Project Goals

- Explore and understand the structure of the dataset
- Perform exploratory data analysis (EDA)
- Estimate survival probabilities using the **Kaplan-Meier estimator**
- Compare survival distributions using the **Log-Rank test**
- Identify mortality risk factors using the **Cox Proportional Hazards model**
- Interpret statistical findings in a clinical context

## Dataset

The dataset contains clinical records for **299 patients with heart failure**.

It includes demographic characteristics, clinical measurements, comorbidities, and patient survival information.

### Key Variables

| Variable | Description |
|---|---|
| `age` | Age of the patient |
| `anaemia` | Whether the patient has anaemia |
| `creatinine_phosphokinase` | Level of creatinine phosphokinase in the blood |
| `diabetes` | Whether the patient has diabetes |
| `ejection_fraction` | Percentage of blood leaving the heart during each contraction |
| `high_blood_pressure` | Whether the patient has high blood pressure |
| `platelets` | Platelet count in the blood |
| `serum_creatinine` | Level of serum creatinine in the blood |
| `serum_sodium` | Level of serum sodium in the blood |
| `sex` | Gender of the patient |
| `smoking` | Whether the patient smokes |
| `time` | Follow-up period in days |
| `DEATH_EVENT` | Mortality indicator (1 = died, 0 = survived) |

**Source:** [UCI Machine Learning Repository – Heart Failure Clinical Records](https://archive.ics.uci.edu/ml/datasets/Heart+Failure+Clinical+Records)

## Methodology

### 1. Data Preprocessing

- Loaded and inspected the dataset
- Checked data types and missing values
- Examined descriptive statistics
- Prepared variables for survival analysis

### 2. Exploratory Data Analysis

EDA was performed to understand:

- Distribution of clinical variables
- Mortality patterns
- Relationships between clinical indicators and mortality
- Differences between patient groups

### 3. Kaplan-Meier Survival Analysis

The **Kaplan-Meier estimator** was used to estimate the probability of survival over time.

Survival curves were examined for different patient characteristics to identify differences in survival patterns.

### 4. Log-Rank Test

The **Log-Rank test** was used to statistically compare survival distributions between groups.

For example, survival curves can be compared between patients with and without:

- Diabetes
- High blood pressure
- Anaemia
- Smoking history
- Low vs. high ejection fraction

### 5. Cox Proportional Hazards Model

A **Cox Proportional Hazards regression model** was fitted to investigate the relationship between clinical characteristics and mortality risk.

The model provides **hazard ratios (HRs)** that quantify how changes in explanatory variables are associated with the hazard of death.

## Results

The analysis indicates that several clinical characteristics are associated with differences in survival outcomes.

In particular:

- **Lower ejection fraction** is associated with increased mortality risk.
- **Higher serum creatinine** is associated with poorer survival outcomes.
- Differences in survival patterns can also be observed across several patient characteristics and comorbidities.

The final notebook contains the statistical results, survival curves, hazard ratios, and visualizations generated during the analysis.

> **Note:** The results section should be updated with the exact hazard ratios, p-values, confidence intervals, and Kaplan-Meier/log-rank results obtained from the final analysis.

## Project Structure

```text
Heart_Failure_Project/
│
├── heart_failure_project.ipynb
├── heart_failure_clinical_records_dataset.csv
├── requirements.txt
└── README.md
