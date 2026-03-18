# FYP Pneumonia Length of Stay Analysis

This project contains an R-based statistical analysis of pneumonia patient data, with a focus on identifying factors associated with hospital length of stay (LOS).

The workflow covers data cleaning, feature engineering, exploratory analysis, statistical testing, and predictive modeling using generalized linear models and negative binomial regression.

## Project Objective

The main objective of this project is to study how demographic factors, comorbidities, and medical procedures relate to the length of stay of pneumonia patients in hospital.

## Methods Used

This project includes:

- data cleaning and preprocessing
- handling diagnosis and procedure code columns
- feature engineering from diagnosis and treatment records
- creation of binary clinical indicators
- exploratory statistical analysis
- chi-square testing for association
- multicollinearity checking
- Poisson, quasi-Poisson, and negative binomial regression
- model comparison using AIC, BIC, RMSE, log-likelihood, and pseudo R-squared
- basic decision tree analysis
- visualization using `ggplot2`

## Dataset Overview

The dataset was imported from an Excel file and includes patient-level hospital records. Variables appear to include:

- patient demographic information
- discharge status
- age
- sex
- length of stay
- diagnosis codes
- procedure codes

From these fields, additional variables were engineered to represent conditions and treatments such as:

- hypertension
- diabetes
- stroke
- obesity
- smoking
- COPD
- ischemic heart disease
- kidney failure
- pleural effusion
- depression
- anxiety
- dementia
- epilepsy
- COVID
- chest X-ray
- abdominal X-ray
- intubation
- respiratory therapy
- CT scan

## Workflow Summary

The analysis pipeline follows these general steps:

1. Load and filter the raw dataset.
2. Count diagnosis and procedure entries for each patient.
3. Combine diagnosis columns into a single diagnosis text field.
4. Combine procedure columns into a single treatment text field.
5. Create binary indicators based on diagnosis and procedure codes.
6. Recode selected variables into factors and grouped categories.
7. Split the data into training and test sets.
8. Explore relationships between categorical predictors.
9. Fit and compare count-data regression models.
10. Evaluate model fit and visualize results.

## Main Packages Used

- `tidyverse`
- `readxl`
- `dplyr`
- `tidyr`
- `MASS`
- `car`
- `caret`
- `corrplot`
- `rpart`
- `rpart.plot`
- `performance`
- `pscl`
- `AER`

## Model Notes

The project compares several count-data models for LOS, including:

- Poisson regression
- quasi-Poisson regression
- negative binomial regression

Based on the comments in the analysis, the negative binomial model appears to provide the best fit, especially because overdispersion is present in the data.

## Files

- `*.Rmd` or analysis notebook:
  Main analysis script containing preprocessing, modeling, and evaluation steps.

- `data.xlsx`:
  Source dataset used in the analysis.
  Im not uploading this one.

## Important Note on Data Privacy

Im just showing the working of my project, there's no data being uploaded to the public.

