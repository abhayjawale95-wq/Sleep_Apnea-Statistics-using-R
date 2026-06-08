# Sleep Apnea Statistical Analysis

A statistical analysis of sleep apnea patient data using Python, covering 
descriptive statistics, hypothesis testing, and predictive modeling.

## Overview

This project applies a full statistical workflow to a healthcare dataset 
containing sleep, physiological, and lifestyle variables. The goal was to 
identify patterns and clinical associations relevant to sleep apnea severity 
and hypertension.

## Dataset

Synthetic sleep apnea patient dataset (`sm.csv`) containing variables including:
- Sleep Duration, Sleep Quality Score
- BMI, Age, Gender
- AHI Events Per Hour
- Sleep Apnea Severity (None / Mild / Moderate / Severe)
- Hypertension, Alcohol Consumption

## Methods Applied

| Method | Purpose |
|---|---|
| Descriptive Statistics | Mean, median, mode, standard deviation across key variables |
| Missing Value Imputation | Mode-based imputation for categorical Sleep Apnea Severity |
| Z-Score Analysis | Outlier detection for Sleep Duration and AHI Events |
| Pearson Correlation | Relationship between sleep duration and sleep quality score |
| Chi-Squared Test | Association between Gender and Hypertension |
| Shapiro-Wilk Test | Normality check prior to parametric testing |
| Independent T-Test | Sleep duration difference between hypertensive vs. non-hypertensive patients |
| Linear Regression | BMI and Age as predictors of AHI Events Per Hour |
| Logistic Regression | Predicting Hypertension using BMI, Age, and AHI |

## Key Findings

- BMI and Age are significant predictors of AHI Events Per Hour; each unit 
  increase in BMI corresponds to 0.68 additional AHI events
- No statistically significant association found between Gender and Hypertension 
  (p = 0.1852)
- Logistic Regression revealed a class imbalance issue, highlighting the 
  limitation of accuracy as a sole performance metric in imbalanced clinical datasets
- No confirmed outliers in Sleep Duration based on the ±3 Z-score threshold

## Libraries Used

- `pandas`, `numpy` — data manipulation
- `scipy.stats` — hypothesis testing
- `sklearn` — regression modeling
- `matplotlib` — visualization

## Author

Abhay Sunil Jawale  
Master of Business Analytics — DePaul University  
[LinkedIn] www.linkedin.com/in/abhay-jawale-12344b1a8
