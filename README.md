# Heart Failure Survival Analysis

This project focuses on understanding survival patterns among patients suffering from heart failure. Using the **Heart Failure Clinical Records Dataset** from the UCI Machine Learning Repository, the analysis applies statistical survival analysis techniques to identify clinical factors associated with mortality risk.

---

## Project Goals

- Explore the structure and characteristics of the dataset
- Perform exploratory data analysis (EDA)
- Apply **Kaplan-Meier survival analysis** to estimate survival probabilities
- Use **Log-Rank tests** to compare survival between patient groups
- Fit a **Cox Proportional Hazards model** to identify significant predictors of mortality
- Interpret statistical findings in the context of patient survival and clinical risk

---

## Dataset Description

The dataset contains clinical records of **299 patients with heart failure**, collected from the UCI Machine Learning Repository.

Each observation contains demographic characteristics, clinical measurements, comorbidities, and information about patient survival.

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

**Dataset Source:**  
https://archive.ics.uci.edu/ml/datasets/Heart+Failure+Clinical+Records

---

## Methodology

### 1. Data Preprocessing

The dataset was first inspected and prepared for analysis.

Steps included:

- Checking the structure and data types
- Identifying missing values
- Examining descriptive statistics
- Preparing variables for survival analysis

### 2. Exploratory Data Analysis

Exploratory analysis was conducted to understand the distribution of clinical characteristics and their relationship with mortality.

Visualizations and summary statistics were used to examine:

- Patient demographics
- Clinical measurements
- Comorbidities
- Mortality patterns
- Differences between patient groups

### 3. Kaplan-Meier Survival Analysis

The **Kaplan-Meier estimator** was used to estimate the probability of survival over the follow-up period.

Survival curves were generated to examine differences in survival between groups based on selected clinical and demographic characteristics.

### 4. Log-Rank Test

The **Log-Rank test** was used to statistically compare survival distributions between groups.

Examples of comparisons include patients with and without:

- Diabetes
- High blood pressure
- Anaemia
- Smoking history

Survival groups can also be defined using clinical thresholds such as ejection fraction or serum creatinine.

### 5. Cox Proportional Hazards Model

A **Cox Proportional Hazards regression model** was fitted to investigate the relationship between patient characteristics and mortality risk.

The model produces **hazard ratios (HRs)**, which indicate the relative change in the hazard of death associated with explanatory variables.

---

## Results

The analysis suggests that several clinical characteristics are associated with differences in survival outcomes.

Key findings include:

- **Lower ejection fraction** is associated with a higher risk of mortality.
- **Higher serum creatinine levels** are associated with poorer survival outcomes.
- Differences in survival patterns can be observed across several clinical characteristics and comorbidities.
- The Cox Proportional Hazards model provides a way to quantify the relationship between these factors and mortality risk while accounting for different follow-up times.

The Jupyter Notebook contains the detailed statistical results, survival curves, hypothesis tests, hazard ratios, and visualizations generated during the analysis.

> **Note:** Specific hazard ratios, p-values, confidence intervals, and test statistics should be added once the final model results have been finalized.

---

## Project Structure

```text
Heart_Failure_Project/
├── heart_failure_project.ipynb
├── heart_failure_clinical_records_dataset.csv
├── requirements.txt
└── README.md
