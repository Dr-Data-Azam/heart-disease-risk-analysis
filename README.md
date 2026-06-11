# Heart Disease Risk Analysis
**Author:** Sheikh Azam Uddin

An end-to-end statistical analysis examining how serum cholesterol profiles and lifestyle
factors relate to heart disease risk, using a dataset of 10,000 individuals.

## Overview

This project investigates the relationship between cholesterol levels (LDL, HDL), blood
pressure, smoking, and exercise habits on heart disease diagnosis. The analysis uses
logistic regression, chi-square tests, and a two-sample t-test, presented as a fully
reproducible R Markdown report.

## Skills Demonstrated

- **Reproducible reporting** with R Markdown (HTML / PDF / Word output, floating TOC)
- **Tidyverse** (`dplyr`, `ggplot2`) for data wrangling and visualization
- **Missing value imputation** — median for numerical, mode for categorical variables
- **Formatted tables** using `knitr::kable()`
- **Statistical analysis** — chi-square tests, Welch two-sample t-test, logistic regression
- **Data visualization** — bar charts, boxplots, correlation heatmap, odds ratio plot with
  confidence intervals

## Repository Structure

```
├── heart_disease_analysis.Rmd   # Main analysis — R Markdown source
├── heart_disease.csv            # Dataset (10,000 individuals, Kaggle)
└── README.md
```

## How to Reproduce

1. Clone this repository
2. Open `heart_disease_analysis.Rmd` in RStudio
3. Install required packages (one-time):
   ```r
   install.packages(c("dplyr", "ggplot2", "reshape2", "broom", "knitr"))
   ```
4. Click **Knit** to generate the report in HTML, PDF, or Word format

## Dataset

- **Source**: Kaggle — Heart Disease Dataset
- **Size**: 10,000 individuals
- **Outcome**: Heart Disease Status (Yes / No)
- **Predictors**: Blood pressure, cholesterol level, triglycerides, HDL/LDL cholesterol
  flags, smoking status, exercise habits, hypertension diagnosis

## Key Findings

- No predictor variables reached statistical significance at α = 0.05
- Exercise habits showed the largest (borderline) odds ratios, suggesting possible
  reverse causality or unmeasured confounding
- Cholesterol variables did not associate significantly with outcome — possibly due to
  variable encoding or sample limitations
- Future work could explore interaction terms, variable transformations, or LASSO
  regularization to improve predictive performance

## Rendered Report

**[View the full rendered report here](https://htmlpreview.github.io/?https://github.com/Dr-Data-Azam/heart-disease-risk-analysis/blob/main/heart_disease_analysis.html)**

The link above opens the complete report — all tables, visualizations, and statistical
output — directly in the browser. No R installation required.
