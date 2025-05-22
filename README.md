# The Impact of Total Parenteral Nutrition (TPN) on ICU Patient Survival: A Survival Analysis Using MIMIC-IV

## Overview

This project investigates the effect of Total Parenteral Nutrition (TPN) on ICU patient survival using real-world data from the MIMIC-IV database. TPN is a critical nutritional intervention for patients unable to tolerate enteral feeding. While historically associated with risks, this study evaluates its impact using survival modeling and multivariable regression.

---

## Type of Analysis

- Survival Analysis (Kaplan-Meier Curves)
- Multivariable Cox Proportional Hazards Regression
- Subgroup and Sensitivity Analyses
- Real-world data modeling with MIMIC-IV

---

## Objectives

- Assess the association between TPN and ICU survival outcomes  
- Evaluate survival differences using time-to-event methods  
- Identify clinical predictors of mortality among TPN and non-TPN patients  
- Provide real-world evidence to inform ICU nutrition protocols

---

## Dataset

- **Source**: MIMIC-IV (v3.1), a publicly available ICU database  
- **Sample**: Adult ICU patients (≥18 years)  
- **Exposure**: TPN administration (item IDs: 225916, 225917, 225918)  
- **Outcomes**:
  - Primary: ICU mortality  
  - Secondary: ICU length of stay (LOS)

---

## Methodology

- Retrospective cohort study using Python  
- Binary classification for TPN exposure  
- Descriptive statistics and baseline characteristic comparison  
- Kaplan-Meier survival curves and log-rank test  
- Multivariable Cox regression adjusting for:
  - Age, Gender, Comorbidities (sepsis, AKI, cancer, etc.)
  - Laboratory indicators (Albumin, BUN, Creatinine)  
- Proportional hazards tested via Schoenfeld residuals  
- Sensitivity analysis: excluded LOS > 95th percentile

---

## Results

- **Kaplan-Meier Analysis**: TPN recipients showed significantly higher ICU survival (p = 4.21 × 10⁻²⁸)  
- **Multivariable Cox Model**:  
  - TPN associated with a 30% reduction in ICU mortality  
  - HR = 0.70 (95% CI: 0.65–0.75, p < 0.005)  
- **Subgroup Cox Model**: Confirmed survival benefit within TPN-only cohort  
- ICU LOS was longer in TPN patients, likely due to survivorship rather than harm

---

## Key Findings

- TPN was independently associated with improved ICU survival  
- Age, AKI, and sepsis were stronger mortality predictors than gender or race  
- Modern ICU protocols likely mitigate historical risks of TPN (e.g., infections, hyperglycemia)

---

## Clinical Implications

- Early, individualized TPN can be life-saving when enteral feeding is not feasible  
- Structured protocols and predictive tools can further optimize safety and effectiveness  
- Future applications may include AI-guided TPN initiation strategies

---

## Tools & Technologies

- Python 3.10  
- `lifelines` (survival modeling)  
- `pandas`, `seaborn`, `matplotlib`  
- PostgreSQL (data extraction from MIMIC-IV)

---

## Skills Demonstrated

- Real-world data extraction and cohort definition  
- Advanced survival analysis using time-to-event methods  
- Multivariable modeling and hazard ratio interpretation  
- ICU nutrition outcome research  
- Health informatics and reproducible analytics

---

## Author

**Alanoud Alturki**  
Health Data Analyst | Health Informatics Specialist | Pharmacist  
MS in Health Informatics · MS in Health Data Analysis · PhD Student  
[LinkedIn](https://www.linkedin.com/in/alanoud-alturki-5601b2b5)

---

## License

This project is forresearch purposes only. Data is derived from the publicly available, de-identified MIMIC-IV database.
